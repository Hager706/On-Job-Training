# Documentation: Dockerized Node.js App

## Overview
This project is a simple Node.js application that uses Express to serve a "Hello, Dockerized Node.js App!" message. The app is containerized using Docker for easy deployment and scalability.

## Prerequisites
Before getting started, ensure you have the following installed on your system:

- 🟢 **Node.js** 
- 📦 **npm** 
- 🐳 **Docker** 

## Project Structure
```
my-node-app/
├── app.js               # Main application file
├── Dockerfile           # Docker configuration file
├── .dockerignore        # Files to ignore in Docker build
├── package.json         # Node.js dependencies and scripts
└── README.md            # Project documentation (this file)
```

## Setup Instructions


### 1. 📦 Install Dependencies
Install the required Node.js dependencies:

```bash
npm install
```
![Alt text](pic1.png)

### 3. 🚀 Run the App Locally
To run the app without Docker:

```bash
node app.js
```
Visit **http://localhost:3000** 

![Alt text](pic2.png)

## Docker Setup

### 1. 🏗️ Build the Docker Image
Build the Docker image for the Node.js app:

```bash
 docker build -t lab1-docker .
 ```

### 2. ▶️ Run the Docker Container
Run the container and map port 9000 on my host to port 3000 in the container:

```bash
docker run -p 9000:3000 my-node-app
```
Visit **http://localhost:9000** to access the app.

![Alt text](pic2.png)

### 3. ⏹️ Stop the Container
To stop the running container, find the container ID using:

```bash
docker ps
```
Then stop the container:

```bash
docker stop <container-id>
```


