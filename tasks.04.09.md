# Docker
​
1. What is containerization, and how does it differ from virtualization?

Conatainerization is the process of creating a separate package that contains everything necessary to run. It's much lighter than a virtual machine, but has the necessary components to be an "all-in-one" solution: code, runtime environment, system tools, libraries and settings. 
​
2. Why is containerization important in modern software development and deployment?

It takes up much less power than a virtual machine would, and is totally isolated from it's host, so that any errors are also isolated and have no affect between host and container. 
​
3. What is the difference between an image and a container in Docker?

A Docker image is a static element that reflects everything that the container should have. It is like an overview. A container is an executed image, an instance of this image. One image can be a template to produce many containers, and container is where the work is done.  
​
4. Can you give an example of a situation where you might choose to use Docker containers in a software development project?

Containers are a good way to make applications "travel" inside the production, and they can be used to pass the application along to another team. 
​
5.If you were tasked with explaining Docker to someone who has never heard of it before, how would you describe it in a few sentences?

Docker is like a box of your favourite chocolates. Imagine you like different chocolates by different producers, and some might even not be available in the UK, so you might have to go abroad to get them. Usually it would take you a lot of time and effort to find the specific chocolates one by one, bring them together and have sitting in a pretty box together. If it's a Docker box, it already has all of them picked out, delivered, set neatly side-ba-side and waiting for you to enjoy of offer your friends. 

​
## Extension
​
Fill in this cheat sheet throughout the day to help and remind you understand how to use Docker commands
​
| Command | Description |
| :-----: | ----------- |
|   ps    |list running containers, -a flag to list the terminated ones 
| images  |top level images with attributes
|  pull   |pull images from repo
|  build  |create an image from Dockerfile
|   run   |create and run container from image
|  stop   |stop running the container, but gracefully :D 
​
| Flag | Description  
|:------:|---------------------------------------------------
| -a | list all, including stopped ones
| -d | run in the background
| -t | name tag
| -p | map port on host machine to port in container 
​
Below is an example of a how you might format a docker command. (In documentation having something wrapped in square brackets [] denotes that it is optional to provide this in the command)
​
```bash
docker run [OPTIONS] <IMAGE[:TAG|@DIGEST]> [COMMAND] [ARG...]