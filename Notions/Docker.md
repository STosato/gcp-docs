# Docker
Docker is an open source platform for building, deploying, and managing containerized applications.

It enables developers to <u>package applications</u> into **containers**: standardized executable components combining:
- application source code
- the operating system (OS) libraries
-  dependencies 
Required to run that code in <u>any environment</u>.

> containers can be created without Docker, but the platform makes it easier, simpler, and safer to build, deploy and manage containers

Docker is essentially a **toolkit** that enables developers to build, deploy, run, update, and stop containers using simple commands and work-saving automation through a single API.

## How containers work
Containers are made possible by **process isolation** and **virtualization** capabilities built into the <u>Linux kernel</u>.

These capabilities enable multiple application components to **share the resources** of a single instance **of the host operating system** as (much) **same as hypervisor enables multiple virtual machines (VMs)** to share the CPU, memory and other resources of a single hardware server. 

As a result, container technology offers all the functionality and benefits of VMs - *including application isolation, cost-effective scalability, and disposability* - plus important additional advantages:
- **Lighter weight:** Unlike VMs, containers don’t carry the payload of an entire OS instance and hypervisor; they include only the OS processes and dependencies necessary to execute the code.
- **Greater resource efficiency**
- **Improved developer productivity**: Compared to VMs, containers are faster and easier to deploy, provision and restart. This makes them ideal for use in [[CI-CD]] pipelines and a better fit for development teams adopting Agile and DevOps practices.

## Docker tools and terms
### **DockerFile**
Every Docker container starts with a simple text file containing instructions for how to build the Docker container image. 

_DockerFile_ automates the process of Docker image creation.
It’s essentially a list of command-line interface (CLI) instructions that Docker Engine will run in order to assemble the image.

### **Docker images**
_Docker images_ contain executable application source code as well as all the tools, libraries, and dependencies that the application code needs to run as a container. 

When you run the Docker image, it becomes one **instance** (or multiple instances) of the container.

### **Docker containers**
Docker containers are the live, running instances of Docker images.

### **Docker daemon**
Docker daemon is a service running on your operating system. 

This service creates and manages your Docker images for you using the commands from the client, acting as the control center of your Docker implementation.

### **Docker registry**
A Docker registry is a scalable open-source storage and distribution system for docker images. The registry enables you to track image versions in repositories, using tagging for identification. This is accomplished using git, a version control tool.

## Docker deployment and orchestration
To monitor and manage container lifecycles in more complex environments, you’ll need to turn to a **container orchestration tool**. 
While Docker includes its own orchestration tool (called Docker Swarm), most developers choose [[Kubernetes]] instead.