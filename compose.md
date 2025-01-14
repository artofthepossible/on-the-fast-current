### Unboxing Docker Compose
It consists of a Python web API backend to generate avatars and a Javascript SPA (single page app) frontend. If you are not a Python or Javascript guru, don't panic!


Time to Complete: 5-10 minutes

Usage
To get started, clone the [avatars](https://github.com/dockersamples/avatars
cd avatars) repository locally:

```sh
$ git clone https://github.com/artofthepossible/avatars
cd /Users/epabishai/apps/artofthepossible/customers/pnc/avatars
docker compose up -d

Initiate the Watch
docker compose watch

Make Code Changes
Update the web index.html code with the following: 
<h1>docker compose watch</h1>
```

Compose launches the services and attaches in file watch mode.
As the developer makes changes to the applciation, the image is rebuilding and the changes are synched for a faster feedback loop to the developer
