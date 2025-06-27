16-06-2025 16:58:54

Status :

Tags :

## 2. Setting up new React Project

you can go to [nvm](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating) and follow the installation 

1. Install Node and npm using nvm

For Mac or linux
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```

For windows,

```bash
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```

if it doesn't work,

```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

Now you need to close and reopen the terminal to load nvm, then check and verify your installation

```bash
$ nvm --version  
0.38.0
```

Now nvm is ready to use. we will use nvm to manage Node.js versions, Nvm has a lot of subcommands such as install, use, uninstall, and more. We want to choose some essential subcommands and explain them.

2. Install a version of Node.js

First, you can get the list of available versions by `list-remote` or `ls-remote` subcommand.  `nvm list-remote` or `nvm ls-remote`. You can install a specific version by nvm with `install` subcommand.

```bash
nvm install <version> # like: 14.17.6
```

If you want to install the LTS version you can use `--lts` instead of version number.

```bash
nvm install --lts
```

Or you can install the latest version with `node` instead of version number.

```bash
nvm install node
```

Load a specific version of Node.js, after you install some versions of Node.js on your machine; So you can see the list of installed versions with `list` or `ls` subcommand.

```bash
nvm list # or nvm ls
```

If you want to load a specific version, use `use` subcommand. With this subcommand, you can load Node.js by version number or `--lts` flag.

```bash
nvm use <version>
```

Or use the LTS version

```bash
nvm use --lts
```

Or use the latest version

```bash
nvm use node
```

3. Uninstall a Node.js version

Finally, If you want to uninstall a version of Node.js, you can use `uninstall` subcommand for that.
First, you need to switch to another version with `use` then you can uninstall that.

```bash
nvm uninstall <version>
```

4. check if the installation was successful 

```bash
$ node -v
v22.14.0

$ npm -v
10.9.2
```

5. create a new vite project  

```bash
$ mkdir scrimba-react

$ cd scrimba-react/

$ mkdir section1

$ cd section1/

$ npm create vite@latest
Need to install the following packages:
create-vite@6.5.0
Ok to proceed? (y) y


> npx
> create-vite

│
◇  Project name:
│  reactFacts
│
◇  Package name:
│  reactfacts
│
◇  Select a framework:
│  React
│
◇  Select a variant:
│  JavaScript
│
◇  Scaffolding project in /home/ashwath/shells/node/scrimba-react/section1/reactFacts...
│
└  Done. Now run:

  cd reactFacts
  npm install
  npm run dev

npm notice
npm notice New major version of npm available! 10.9.2 -> 11.4.2
npm notice Changelog: https://github.com/npm/cli/releases/tag/v11.4.2
npm notice To update run: npm install -g npm@11.4.2
npm notice

[nix-shell:~/shells/node/scrimba-react/section1]$ cd reactFacts/

[nix-shell:~/shells/node/scrimba-react/section1/reactFacts]$ npm install

added 155 packages, and audited 156 packages in 11s

33 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

[nix-shell:~/shells/node/scrimba-react/section1/reactFacts]$ npm run dev

> reactfacts@0.0.0 dev
> vite


  VITE v6.3.5  ready in 302 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
```


## References


