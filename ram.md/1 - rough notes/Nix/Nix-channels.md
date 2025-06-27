04-06-2025 15:56:19

Status :

Tags :

# NixOS Channel and System Management Guide

This document provides a comprehensive overview of managing NixOS channels and system generations, covering best practices, common commands, and troubleshooting tips.

## 1. Understanding Nix Channels

In NixOS, "channels" are essentially pointers to specific branches or releases of the `nixpkgs` repository. They define the set of packages and modules available to your system.

- **Stable Channels:** (e.g., `nixos-24.05`, `nixos-23.11`) These are point releases, thoroughly tested, and receive bug and security fixes for a period.
    
- **Unstable Channel:** (e.g., `nixos-unstable`) This channel tracks the `master` branch of `nixpkgs`. It's bleeding-edge, offering the newest software but potentially less stability.
    

## 2. Listing Your Current Channels

To see which Nix channels your system is currently subscribed to:

```
sudo nix-channel --list
```

**Example Output:**

```
nixos https://nixos.org/channels/nixos-24.05
unstable https://nixos.org/channels/nixos-unstable
```

This shows the alias (`nixos`, `unstable`) and the corresponding URL of each channel.

## 3. Adding and Removing Channels

You can manage your channel subscriptions.

### 3.1. Adding a New Channel

To add a channel, you need its URL and a local alias for it. You can find official channel URLs at [https://nixos.org/channels/](https://nixos.org/channels/ "null").

```
sudo nix-channel --add <CHANNEL_URL> <CHANNEL_NAME>
```

**Example: Adding the `nixos-unstable` channel:**

```
sudo nix-channel --add https://nixos.org/channels/nixos-unstable unstable
```

### 3.2. Removing a Channel

To remove a channel, use its alias.

```
sudo nix-channel --remove <CHANNEL_NAME>
```

**Example: Removing the `unstable` channel:**

```
sudo nix-channel --remove unstable
```

### 3.3. Switching Your Main System Channel (Upgrade)

This is how you upgrade your NixOS system from one stable release to another (e.g., from 24.11 to 25.05).

1. **Remove the old `nixos` channel:**
    
    ```
    sudo nix-channel --remove nixos
    ```
    
2. **Add the new stable channel, aliasing it as `nixos`:**
    
    ```
    sudo nix-channel --add https://nixos.org/channels/nixos-25.05 nixos
    ```
    
    (Replace `nixos-25.05` with the desired new stable release URL.)
    

## 4. Updating Channels

Adding/removing channels only changes your subscription list. To download the latest package definitions from the subscribed channels to your local Nix store:

```
sudo nix-channel --update
```

This updates the `nixexprs.tar.gz` for each channel, providing your system with the newest available package versions and module definitions.

## 5. Rebuilding Your System

After updating channels, you must rebuild your NixOS system to apply these changes. This generates a new system generation based on the updated channel data.

```
sudo nixos-rebuild switch
```

- `switch`: Activates the newly built configuration.
    
- You can also use `sudo nixos-rebuild switch --upgrade`, which is a convenient shortcut that first performs `sudo nix-channel --update` for root channels _before_ building and activating.
    

**Important for major upgrades:** Before rebuilding for a major stable release upgrade (e.g., 24.11 to 25.05), **always review the release notes for "Backward Incompatibilities"**. These will detail any changes you might need to make to your `/etc/nixos/configuration.nix` file.

## 6. Understanding Packages with Multiple Channels

When you have multiple channels (e.g., `nixos` and `unstable`), here's how packages are handled:

- **Channel Metadata is Stored:** The Nix store contains the definitions (Nix expressions) from each channel you subscribe to via `nix-channel --update`.
    
- **Packages are Not Duplicated by Default:** Nix's store is content-addressed. If a package (e.g., `firefox-125.0`) is byte-for-byte identical across different channels, it will only be stored once in the Nix store.
    
- **Disk Space Increase for Different Versions:** Disk space primarily increases when you install:
    
    - Different versions of the same package (e.g., `firefox-125` from `nixos` and `firefox-126` from `unstable`).
        
    - Packages unique to a specific channel.
        
    - Shared dependencies are still deduplicated across channels.
        

You can explicitly pull packages from different channels in your `configuration.nix`:

```
{ config, pkgs, ... }:

let
  # Import the unstable channel using its alias
  unstable = import <unstable> {
    config = config.nixpkgs.config; # Ensure consistent configuration
  };
in
{
  environment.systemPackages = with pkgs; [
    firefox # From your main 'nixos' channel
    git

    unstable.vscode # VS Code from the 'unstable' channel
  ];
}
```

## 7. Good Practice: Managing Deprecated Channels

It is **highly recommended** to update your main NixOS channel to the latest stable release and remove deprecated ones.

### Why Update?

- **Security Updates:** Deprecated channels cease to receive security fixes and bug patches. Running on an unsupported channel leaves your system vulnerable.
    
    - _Example:_ NixOS 24.11 "Vicuña" became deprecated upon the release of 25.05 "Warbler" and will stop receiving updates soon (e.g., June 30, 2025).
        
- **Access to Newer Software:** Latest stable channels provide updated package versions, new features, and improvements.
    
- **Community Support:** Help and troubleshooting are primarily available for current stable or unstable channels.
    
- **Clarity and Disk Space:** Keeping deprecated channels adds unnecessary clutter and minimal, though not substantial, disk usage.
    

### What "Deprecated" Means:

A channel marked "deprecated" means a newer, actively maintained stable version is available, and the deprecated one is nearing its End-of-Life (EoL) for updates.

## 8. Managing System Generations (Rollback & Deletion)

NixOS creates a new system "generation" every time you successfully run `nixos-rebuild switch`. This enables powerful rollback capabilities.

### 8.1. Listing All System Generations

```
sudo nixos-rebuild list-generations
```

Output provides: Generation number, build date, NixOS version, kernel, and indicates `current` (active) and `booted` generations.

### 8.2. Rolling Back to a Previous Generation

- **To the immediately previous generation:**
    
    ```
    sudo nixos-rebuild switch --rollback
    ```
    
- **To a specific generation number:**
    
    1. List generations (`sudo nixos-rebuild list-generations`) to find the target number.
        
    2. Switch:
        
        ```
        sudo nix-env --switch-generation <GENERATION_NUMBER> -p /nix/var/nix/profiles/system
        sudo /nix/var/nix/profiles/system/bin/switch-to-configuration switch
        ```
        
- **Temporary boot via GRUB:** Reboot, select "NixOS" -> "Old configurations" in the GRUB menu. To make it permanent after booting, run `sudo /run/current-system/bin/switch-to-configuration boot`.
    

### 8.3. Deleting NixOS Generations

Deleting generations helps free up disk space by removing unreferenced system states. You cannot delete the `current` or `booted` generation.

- **Delete specific generations:**
    
    ```
    sudo nix-env --delete-generations <GEN_NUM_1> <GEN_NUM_2> ... -p /nix/var/nix/profiles/system
    ```
    
    Example: `sudo nix-env --delete-generations 1 2 3 -p /nix/var/nix/profiles/system`
    
- **Delete all old generations (keep only current):**
    
    ```
    sudo nix-env --delete-generations old -p /nix/var/nix/profiles/system
    ```
    
- **Delete generations older than N days:**
    
    ```
    sudo nix-env --delete-generations <NUMBER>d -p /nix/var/nix/profiles/system
    ```
    
    Example: `sudo nix-env --delete-generations 30d -p /nix/var/nix/profiles/system`
    
- **Keep only the last N generations:**
    
    ```
    sudo nix-env --delete-generations +<NUMBER> -p /nix/var/nix/profiles/system
    ```
    
    Example: `sudo nix-env --delete-generations +5 -p /nix/var/nix/profiles/system`
    

### 8.4. Crucial: Garbage Collection

After deleting generation symlinks, you must run garbage collection to actually free up disk space.

```
sudo nix-collect-garbage -d
```

- `-d` (or `--delete-old`): Removes unreferenced paths from the Nix store.
    
- After garbage collection, run `sudo nixos-rebuild switch` to update your bootloader entries if they still show deleted generations.
    

This guide should serve as a solid reference for managing your NixOS channels and system history!

## References

- [NixOS Channels](https://nixos.org/channels/ "null")
    
- [NixOS Wiki: Nix channels](https://nixos.wiki/wiki/Nix_channels "null")
    
- [Nix Reference Manual: nix-channel](https://nixos.org/manual/nix/stable/command-ref/nix-channel.html "null")
    
- [Nix Reference Manual: nix-env --delete-generations](https://nixos.org/manual/nix/stable/command-ref/nix-env/delete-generations.html "null")
    
- [NixOS Blog: NixOS 25.05 released](https://nixos.org/blog/announcements/2025/nixos-2505/ "null")