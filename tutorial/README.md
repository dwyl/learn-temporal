# Hello World _Tutorial_

This is the default project that is scaffolded out when you run 
`npx @temporalio/create@latest ./tutorial`.

https://docs.temporal.io/docs/typescript/hello-world
walks through the code in this sample.

### Prerequisites

To run this example, you will need:

+ [x] Docker: https://docs.docker.com/get-docker 
  Learn: https://github.com/dwyl/learn-docker
+ [x] Node.js: https://nodejs.org/en
+ [x] Internet connection to download the dependencies
+ [x] 10 minutes of time.

### Running this sample



1. Make sure Temporal Server is running locally 
(see the [quick install guide](https://docs.temporal.io/docs/server/quick-install/)).

If you don't already have a `docker-compose` directory 
in the root of your project,
clone it from:

```sh
git clone https://github.com/temporalio/docker-compose.git
```

Once you have a `docker-compose` directory, 
open a second termnial window/tab 
and run the following:

```sh
cd  docker-compose
docker-compose up
```

Once Docker has successfully downloaded all its dependencies and booted the containers,
you should see something similar to the following in the Docker Desktop App:

![docker-temporal-5-containers](https://user-images.githubusercontent.com/194400/157717991-1acf3bf2-db3a-4167-bce1-4bd080aa32ae.png)


2. Install the node.js dependencies by running: `npm install` 
(in the root directory of the project, where the `package.json` file is)

Once 

3. `npm run start.watch` to start the Worker.

4. In another shell, `npm run workflow` to run the Workflow Client.

The client should log the Workflow ID that is started, and you should see it reflected in Temporal Web UI.

Optionally, you can also uncomment the `await handle.result()`, rerun, and see the client script return:

```bash
Hello, Temporal!
```


