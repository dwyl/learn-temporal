# Hello World _Tutorial_

This is the default project that is scaffolded out when you run 
`npx @temporalio/create@latest ./tutorial`.

<!--
https://docs.temporal.io/docs/typescript/hello-world
walks through the code in this sample.
-->


### Prerequisites

To run this example, you will need:

+ [x] Docker: https://docs.docker.com/get-docker 
  Learn: https://github.com/dwyl/learn-docker
+ [x] Node.js: https://nodejs.org/en
+ [x] Internet connection to download the dependencies
+ [x] 10 minutes of time.



### Run the Complete Example

Before you begin the tutorial,
try to run the _finished_ project.

1. Clone the project:

```sh
git clone https://github.com/dwyl/learn-temporal.git
```

Once you've cloned the project,
enter the `learn-temporal` directory.

```sh
cd learn-tutorial
```

2. Prepare to Run the Project 

Open a **_second_ terminal window**
so you can run the Temporal Server
(Docker containers).

In your **_current_ terminal window**, 
change working directory 
into the `tutorial` directory:

```sh
cd tutorial
```

In the second terminal window,
change into the `docker-compose` window:

```sh
cd docker-compose
```


3. Install the Node.js Dependencies

> **Note**: Don't run this command using your mobile bandwidth 
(unless you have an unlimited plan) 
as it will download [**`500 MB`+**](https://github.com/dwyl/learn-temporal/issues/1#issuecomment-1066741638) of data.

In the `tutorial` directory
(where the `package.json` file is),
install the Node.js dependencies by running: 
`npm install` 

You should see something similar to:

```
added 361 packages from 271 contributors and audited 361 packages in 9.762s
```

4. Install & Initialize the Docker Containers

Run the Temporal Server locally,
by issuing the following command 
from within the `docker-compose` directory
(_second terminal window_):

```sh
docker-compose up
```

Once Docker has successfully downloaded 
all its dependencies and started the containers,
you should see something similar to the following:

```
Creating temporal-elasticsearch ... done
Creating temporal-postgresql    ... done
Creating temporal               ... done
Creating temporal-web           ... done
Creating temporal-admin-tools   ... done
```

And in the Docker Desktop App you will see:

![docker-temporal-5-containers](https://user-images.githubusercontent.com/194400/157717991-1acf3bf2-db3a-4167-bce1-4bd080aa32ae.png)



> See the quick install guide:
https://docs.temporal.io/docs/server/quick-install


Once the Docker network is running, 
Open the following url in your web browser:
http://localhost:8088/

You should see an interface similar to the following:

![image](https://user-images.githubusercontent.com/194400/157565096-3449ec47-e201-4a51-8520-33ec3643ce4f.png)



<!--
If you don't already have a `docker-compose` directory 
in the root of your project,
clone it from:

```sh
git clone https://github.com/temporalio/docker-compose.git
```

Once you have a `docker-compose` directory, 
open a second terminal window/tab 
and run the following:
-->

<br />

5. Run the Worker

In the _first_ terminal window,
execute the command:

`npm run start.watch` to start the Worker.

You should see output similar to:

```sh
> temporal-hello-world@0.1.0 start.watch /learn-temporal/tutorial
> nodemon src/worker.ts

[nodemon] 2.0.15
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): src/**/*
[nodemon] watching extensions: ts
[nodemon] starting `ts-node src/worker.ts`
Found prebuilt bridge module {
  binary: '/learn-temporal/tutorial/node_modules/@temporalio/core-bridge/releases/x86_64-apple-darwin/index.node'
}
[INFO] [temporal_sdk_core] Registering worker task_queue="hello-world"
[INFO] assets by path learn-temporal/tutorial/lib/*.map 585 bytes
[INFO]   asset learn-temporal/tutorial/lib/workflows.d.ts.map 192 bytes [compared for emit]
[INFO]   asset learn-temporal/tutorial/lib/activities.d.ts.map 181 bytes [compared for emit]
[INFO]   asset learn-temporal/tutorial/lib/client.d.ts.map 106 bytes [compared for emit]
[INFO]   asset learn-temporal/tutorial/lib/worker.d.ts.map 106 bytes [compared for emit]
[INFO] assets by path learn-temporal/tutorial/lib/*.ts 347 bytes
[INFO]   asset learn-temporal/tutorial/lib/workflows.d.ts 151 bytes [compared for emit]
[INFO]   asset learn-temporal/tutorial/lib/activities.d.ts 102 bytes [compared for emit]
[INFO]   asset learn-temporal/tutorial/lib/client.d.ts 47 bytes [compared for emit]
[INFO]   asset learn-temporal/tutorial/lib/worker.d.ts 47 bytes [compared for emit]
[INFO] asset main.js 491 KiB [emitted] (name: main)
[INFO] runtime modules 670 bytes 3 modules
[INFO] modules by path ./node_modules/@temporalio/ 129 KiB
[INFO]   modules by path ./node_modules/@temporalio/common/lib/ 53.2 KiB
[INFO]     modules by path ./node_modules/@temporalio/common/lib/*.js 44.7 KiB 14 modules
[INFO]     modules by path ./node_modules/@temporalio/common/lib/converter/*.js 8.52 KiB 3 modules
[INFO]   modules by path ./node_modules/@temporalio/workflow/lib/*.js 75.9 KiB
[INFO]     ./node_modules/@temporalio/workflow/lib/worker-interface.js 9.64 KiB [built] [code generated]
[INFO]     ./node_modules/@temporalio/workflow/lib/internals.js 18.4 KiB [built] [code generated]
[INFO]     ./node_modules/@temporalio/workflow/lib/alea.js 2.9 KiB [built] [code generated]
[INFO]     + 7 modules
[INFO] ../../../../../src/main.js 413 bytes [built] [code generated]
[INFO] ./src/workflows.ts 386 bytes [built] [code generated]
[INFO] ./node_modules/long/src/long.js 39.2 KiB [built] [code generated]
[INFO] ./node_modules/ms/index.js 2.95 KiB [built] [code generated]
[INFO] webpack 5.70.0 compiled successfully in 2573 ms
[INFO] Workflow bundle created { size: '0.48MB' }
[INFO] Worker state changed { state: 'RUNNING' }
```


6. Run the Workflow

In _third_ terminal window, 
execute the following command
to run the Workflow:

```sh
npm run workflow
```

The client should log the Workflow ID that is started, 
and you should see it reflected in Temporal Web UI.

Optionally, you can also uncomment the `await handle.result()`, 
rerun, and see the client script return:

```bash
Hello, Temporal!
```




![image](https://user-images.githubusercontent.com/194400/157565604-c06efc45-c0a8-440c-864d-8b36ade7a956.png)


<br /> <br />

## Tidy Up Time

### Done with Docker?

If you need to remove the Temporal docker containers
(e.g: because they are taking up a lot of space on your SSD)
run the following command:

```
docker container prune
```