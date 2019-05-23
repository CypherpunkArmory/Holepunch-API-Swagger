# ![Holepunch](dist/holepunch_logo.svg)


This repository contains the code to run a [Swagger Editor](https://github.com/swagger-api/swagger-editor) with locally that contains ready-to-use examples to interact with the [Holepunch API](https://github.com/CypherpunkArmory/holepunch/).

The API follows the specifications defined by [OpenAPI 3.0](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md).



## Running locally

##### Prerequisites
- Node 6.x
- NPM 3.x

If you have Node.js and npm installed, you can run `npm start` to spin up a static server.

Otherwise, you can open `index.html` directly from your filesystem in your browser.

If you'd like to make code changes to Swagger Editor, you can start up a Webpack hot-reloading dev server via `npm run dev`. 

##### Browser support

Swagger Editor works in the latest versions of Chrome, Safari, Firefox, Edge and IE11.


## Docker

### Running the image from DockerHub
There is a docker image published in [DockerHub](https://hub.docker.com/r/lithogen/holepunch-api-swagger).

To use this, run the following:

```
docker pull lithogen/holepunch-api-swagger
docker run -d -p 6000:8080 lithogen/holepunch-api-swagger
```

This will run Swagger Editor (in detached mode) on port 80 on your machine, so you can open it by navigating to `http://localhost` in your browser.

### Building and running an image locally

To build and run a docker image with the code checked out on your machine, run the following from the root directory of the project:

```
# Install npm packages (if needed)
npm install

# Build the app
npm run build

# Build an image
docker build -t swagger-editor .

# Run the container
docker run -d -p 5050:8080 swagger-editor

```

You can then view the app by navigating to `http://localhost:5050` in your browser.


## Setting up the Holepunch API Locally

Refer to the official [Holepunch repository](https://github.com/CypherpunkArmory/holepunch/) to set the server up locally.  

This will allow the examples in the Swagger Editor to work. 


## License

Copyright 2018 SmartBear Software

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at [apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
