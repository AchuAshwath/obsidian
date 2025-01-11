02-01-2025 17:09:41

Status : #baby 

Tags : [[Digital Leader]]

# Evolution of Computing

## Dedicated
- A physical server wholly utilized by a single customer. For google cloud it is single node clusters, bare metal machines.
- You have  to guess your capacity.
- You'll over play for an underutilized server.
- you cant vertically scale, but you need a manual migration.
- Replacing a server is very difficult.
- You are limited by  you Host Operating System.
- Multiple apps can result in conflicts in resource sharing. 

> Running multiple apps on this kind of machines is not a good practice

- You have a * **guarantee of security, privacy, and full utility of underlying resources** 

> * because its up to your skills on how to bring about security and  privacy.

#### why would you use a dedicated machine?
may be you're high performance computing where you need the machines close together so that you can choose what kind of virtualization you want to run.

## Virtual Machines

- You can run multiple Virtual Machines on one machine.
- **Hypervisor** is the software layer that lets you run the VMs.
- A physical server shared by multiple customers.
- You are to pay for a fraction of the server.
- You'll still over pay for underutilized Virtual Machine.
- You are limited by you Guest Operating System.
- Multiple apps on a single Virtual Machine can result in conflicts in resource sharing.
- Easy to export or import images for migration.
- Easy to Vertical or Horizontal scale.
## Containers
- Virtual Machine running in multiple containers.
- **Docker** **Daemon** is the name of the software layer that lets you run multiple containers.
- You can maximize the utilize of the available capacity which is more cost effective.
- Your container share the same underlying OS so container are more efficient than multiple VMs.
- Multiple apps can run side by side without being limited to the same OS requirements and will not cause conflicts during resource sharing.
- Container are really good but are lot a work to maintain.
## Functions
- Are managed VMs running containers. *aka* *Server-less* *Compute*.
- We don't have to worry about OS or anything, you just upload your code, choose the amount of memory and duration.
- Very cost effective, only pay for the time code is running, VMs only run where there is code to be executed.
- **Cold** **Starts** is a side effect of this setup, The virtual machine has to spin up.
- One of the best offerings at present.

![](https://www.whiteboxsolution.com/wp-content/uploads/2022/07/Picture3.png)
## References

[Google Cloud Digital Leader Certification Course 2024 - Pass the Exam!](https://youtu.be/cbcd6-m8sHg?si=5zzKOYu6k--3f1hHj)