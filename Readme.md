### Unboxing Docker Desktop

Time to Complete: 15-30 minutes

### How to Use This Hands-On Lab
1. You have installed the latest version of Docker Desktop.
2. You have installed a Git client.
3. You have an IDE or a text editor to edit files. Docker recommends using Visual Studio Code.
4. Clone the getting-started-app repository using the following command:
```sh
$ git clone https://github.com/artofthepossible/whale-of-a-time
```

Here's a guided tour of Docker Desktop based on the provided knowledge sources:</br>

Docker Desktop is an all-in-one application for Mac, Linux, or Windows that allows you to build, share, and run containerized applications and microservices. </br>
It provides a user-friendly graphical interface for managing containers, applications, and images directly from your machine.</br>

**New Docker Commands**
You can interact with docker desktop via the cli with these new commands

```sh
$ docker desktop start
✓ Starting Docker Desktop

$ docker desktop stop
✓ Stopping Docker Desktop

$ docker desktop restart
✓ Starting Docker Desktop

$ docker desktop status
✓ Check status

```
When you open Docker Desktop, you'll see the Docker Desktop Dashboard, which offers several key views:</br>

**Containers view**
```sh
This provides a runtime view of all your containers and applications.
You can interact with containers, manage their lifecycle, and perform common actions.
```
![Containers View](./images/containers-view.png)

When a user selects an individula container in Docker Desktop, they can access detailed information like logs, low level details via inspect, you can exec into the container via docker debug, browse the file system and review stats.

**Logs**: View and search through the container's logs, copy log entries, and clear the log terminal.

**Inspect: Access** low-level details about the container, such as the local path, image version, SHA-256, and port mappings.

**Bind mounts**: Explore and manage bind mounts associated with the container.

**Exec**: Use the integrated terminal to run commands within the container, which is useful for debugging or understanding the container's current state.

**Files**: Browse the container's filesystem, edit files, drag and drop files between the host and container, and download files to the host.

**Stats**: Monitor the container's resource usage, including CPU, memory, network, and disk space over time.

**Docker Debug**
You can enable Docker Debug to execute commands, run the container.
![Docker Debug View](./images/dockerdebug-view.png)

```sh
For our sample application with a flask frontend and mongo backend defined as servicees in the compose.yaml file, we can, we can view configurations via the 
```
**compose file viewer**
![Compose Viewer](./images/composeviewer.png)

**Images view**: 
```sh
Here you can see a list of your Docker images, run images as containers, pull the latest versions from Docker Hub, and inspect images.
It also shows image vulnerabilities and clean-up options.
```
![Images Viewer](./images/images-view.png)

**Volumes view**: 
```sh
This displays a list of volumes and allows you to create, delete, and see which ones are being used.
```
![Volume Viewer](./images/volume-view.png)

**Builds view**: 
```sh
You can inspect your build history and manage builders here.
```

The Dashboard also provides access to:</br>

**Settings menu** 
```sh
For configuring Docker Desktop
```
![Settings](./images/settings.png)

**Troubleshoot menu**
```sh
For debugging and performing restart operations
```
![Troubleshoot](./images/troubleshoot.png)

**Pro Tips Commands**
```sh
$ docker desktop start
✓ Starting Docker Desktop

$ docker desktop stop
✓ Stopping Docker Desktop

$ docker desktop restart
✓ Starting Docker Desktop

$ docker desktop status
✓ Check status

```

**Notifications center** 
```sh
For updates and other information
```
![Notifications Center ](./images/notifications-center.png)

**Learning center** 
```sh
Quick in-app walkthroughs and resources
```
![Learning Center ](./images/learning-center.png)

**Quick Search**
```sh
A key feature of Docker Desktop that is located in the Dashboard header.
This allows you to search for containers, images, extensions, volumes, and even Docker documentation.
```
![Quick Search ](./images/quick-search.png)

**Extensions**
```sh
Docker Extensions are a feature in Docker Desktop, to connect the common tasks and workflows that a developer work on
They extend the functionality of your common developer tools and help your developers to glean better insights, integration and automation when building containers
```
![Extensions ](./images/extensions.png)




### Resources
[Docker Init](https://docs.docker.com/reference/cli/docker/init/)
[Containers View](https://docs.docker.com/desktop/use-desktop/container/)
[Images](https://docs.docker.com/desktop/use-desktop/images/)
[Volumes](https://docs.docker.com/desktop/use-desktop/volumes/)
[Builds](https://docs.docker.com/desktop/use-desktop/builds/)
