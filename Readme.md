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

For our sample application with a flask frontend and mongo backend defined as servicees in the compose.yaml file, we can, we can view configurations via the **compose file viewer**
[composeviewer.png]


**Images view**: 
```sh
Here you can see a list of your Docker images, run images as containers, pull the latest versions from Docker Hub, and inspect images.
It also shows image vulnerabilities and clean-up options.
```
**Volumes view**: 
```sh
This displays a list of volumes and allows you to create, delete, and see which ones are being used.
```

**Builds view**: 
```sh
You can inspect your build history and manage builders here.
```

The Dashboard also provides access to:</br>

**Settings menu** 
```sh
For configuring Docker Desktop
```

**Troubleshoot menu**
```sh
For debugging and performing restart operations
```

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

**Learning center** 
```sh
Quick in-app walkthroughs and resources
```

**Quick Search**
```sh
A key feature of Docker Desktop that is located in the Dashboard header.
This allows you to search for containers, images, extensions, volumes, and even Docker documentation.
```



### Resources
[Docker Init](https://docs.docker.com/reference/cli/docker/init/)
[Containers View](https://docs.docker.com/desktop/use-desktop/container/)
[Images](https://docs.docker.com/desktop/use-desktop/images/)
[Volumes](https://docs.docker.com/desktop/use-desktop/volumes/)
[Builds](https://docs.docker.com/desktop/use-desktop/builds/)
