# Installation of Docker

### This information is relevant for Linux Ubuntu 20.04.


---

<img src="materials/reduce_docker_image.jpg">

## Briefly about Docker

### Definition of Docker:

**Docker** - This is an open platform for automating the development, deployment, and execution of applications in containers. Docker containers provide isolated and portable runtime environments for applications, including all the necessary components such as code, runtime, and system tools.

### Advantages of using Docker:

- Simplified application deployment: Docker allows packaging an application and its dependencies into a container, ensuring consistency and portability of the environment across different development, testing, and production environments.

- Increased development efficiency: Docker simplifies the process of creating, testing, and deploying applications by allowing quick creation and destruction of containers, making the development and integration process more streamlined.

- Application isolation: Docker containers provide application isolation, avoiding conflicts between dependent components of an application and ensuring more reliable and secure execution of applications.

- Scalability and flexibility: Docker enables application scalability, resource management, and environment configuration, allowing quick adaptation to changing requirements of applications and infrastructure.

- Resource optimization: Docker allows optimizing server resource utilization as containers share the underlying operating system, reducing memory and computational resource consumption.

### The main components of Docker are:

- Docker Engine: This is the core component of Docker that allows you to create, run, and manage Docker containers on the host machine.

- Docker images: Docker images are portable packages that contain everything needed to run an application, including code, runtime environment, and dependencies. Docker images can be built from Dockerfiles or downloaded from Docker Hub or other Docker Registries.
- Docker Hub and Docker Registry: Docker Hub is a cloud-based repository where developers can find and download Docker images. Docker Registry is a local repository for Docker images that can be configured and used within an enterprise or organization to store and distribute Docker images within the local network.
- Docker Compose: Docker Compose is a tool for defining and managing multi-container applications in Docker. It allows you to define the configuration of an application in a docker-compose.yml file, which contains information about the containers, their settings, and connections between them.
- Docker Swarm: Docker Swarm is a built-in Docker tool for organizing and managing Docker clusters. It allows you to create and manage groups of Docker nodes (hosts), create services and tasks, distribute containers across nodes, scale applications, and provide high availability.
- Docker CLI: Docker Command Line Interface (CLI) is a command-line interface that allows you to interact with Docker Engine and manage containers, images, networks, and other Docker components.
- Docker APIs: Docker APIs are application interfaces that allow you to interact with Docker Engine and manage containers, images, and other Docker resources using RESTful API or other protocols.
- Docker Network: Docker Network is a mechanism for creating and managing networks of Docker containers, allowing containers to communicate and share data with each other, as well as connect to external networks and resources.

---

## Docker installation

### To install Docker on **Windows** and **macOS** operating systems

You can use Docker Desktop, the official Docker tool for Windows, which provides a graphical user interface and is easily installed through an installer. Download and install Docker Desktop from the [official Docker website.](https://www.docker.com/products/docker-desktop)

### To install Docker on a **Linux** operating system

You need to execute a series of commands, such as installing Docker Engine, adding a user to the docker group, configuring Docker to start automatically, and others. The installation process may vary depending on the specific Linux distribution. For example, to install Docker on Ubuntu, execute the following commands:
    
    $ sudo apt update

    $ sudo apt install docker.io

    $ sudo usermod -aG docker $USER

    $ sudo systemctl enable docker

    $ sudo systemctl start docker

---

## Checking Docker Installation

After installing Docker, you can run the command `docker --version` in the command line to verify that Docker Engine has been successfully installed and is running on your system. The output of the command should display the version of Docker Engine and other information about Docker. An example of the command output is shown below:\
<img src="materials/check_docker_inst.jpg">

---

## Installing Docker Compose:
Docker Compose is a tool that allows you to define and run multiple Docker containers along with their configurations in a single configuration file. It is a convenient tool for orchestrating and managing multi-container applications.

### To install Docker Compose on Windows
you can download the Docker Compose installer from the [official Docker website](https://docs.docker.com/compose/install/).

### To install Docker Compose on macOS
you can install Docker Compose using Homebrew, a popular package manager for macOS. Execute the following command in the terminal:

        brew install docker-compose

### To install Docker Compose on a Linux operating system, you can execute the following commands:
    $ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

    $ sudo chmod +x /usr/local/bin/docker-compose

### Note:

In the example, Docker Compose version (1.29.2) is mentioned, you can replace it with the latest available version from the [official Docker Compose repository](https://github.com/docker/compose/releases) on GitHub.