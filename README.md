# simple-site
This project is a demonstration of an Express application that publishes static web pages.

The web pages are stored in the directory `/public` of the project root.

## Installation of dependencies

`npm install`

## Running application on `localhost` using the default port

`npm start`

You'll output similar to the following:

```
2022-10-04T18:33:36.002Z  info: Node server is running on port 8080 at Tue Oct 04 2022 11:33:36 GMT-0700 (Pacific Daylight Time)
```

## Calling the default page

In a web browser enter the following URL:

`http://localhost:8080`


![localhost](https://user-images.githubusercontent.com/1110569/193900809-922f3c56-a6b6-4de3-bfac-310e70f98f94.png)

# Deploying and running the project as a Linux container buildah and Podman

Navigate to the source code directory in a terminal window.

Then run the following command to create the container image.

`buildah bud -t simplesite -f Containerfile  .`

Follow up with the command to run the container in the background against that image.

`podman run -d -p 8080:8080 simplesite`

Test that the container is operating properly

# Deploying and running the project as a Linux container using Docker

Navigate to the source code directory in a terminal window.

Then run the following command to create the container image.

`docker build -t simplesite -f Containerfile .`

Follow up with the command to run the container in the background against that image.

`docker container run -d -p 8080:8080 simplesite`

Test that the container is operating properly

`curl localhost:8080`

You will get a response similar to the following:


