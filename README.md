# LAB 1

# Difference Between CMD and ENTRYPOINT

CMD is used to provide a default command for the container.  
This command can be overridden when running the container.

ENTRYPOINT is used to define the main executable of the container.  
It always runs when the container starts and is not easily overridden.

Example:

```dockerfile
CMD ["python", "app.py"]
```

If the container is started with another command, the CMD instruction will be replaced.

---

# Difference Between COPY and ADD

COPY is used to copy files and directories from the host machine into the Docker image.

ADD can do the same thing as COPY, but it also supports extracting compressed files automatically and downloading files from URLs.

For regular file copying, COPY is the recommended instruction because it is simpler and more predictable.

---

# Problem 1

- Run the container hello-world
- Check the container status
- Start the stopped container
- Remove the container
- Remove the image

## Run the container hello-world

![alt text](images/image.png)

## Check the container status

![alt text](images/image-12.png)

## Start the stopped container

![alt text](images/image-13.png)

## Remove the container

![alt text](images/image-14.png)

## Remove the image

![alt text](images/image-15.png)

---

# Problem 2

- Run container centos or ubuntu in an interactive mode
- Run the following command in the container “echo docker ”
- Open a bash shell in the container and touch a file named hello-docker
- Stop the container and remove it. Write your comment about the file hello-docker
- Remove all stopped containers

## Run container centos or ubuntu in an interactive mode

![alt text](images/image-6.png)

## Run the following command in the container “echo docker ”

![alt text](images/image-7.png)

## Open a bash shell in the container and touch a file named hello-docker

![alt text](images/image-8.png)

## Stop the container and remove it. Write your comment about the file hello-docker

![alt text](images/image-16.png)
`The file hello-docker was created inside the container filesystem. After removing the container, the file was deleted because it was stored in the container writable layer and not in a Docker volume.`

## Remove all stopped containers

![alt text](images/image-17.png)

---

# Problem 3

- Deploy a MySQL database called app-database. Use the mysql latest image, and use the
  -e flag to set MYSQL_ROOT_PASSWORD to P4sSw0rd0!. The container should run in the
  background.

![alt text](images/image-18.png)

---

# Problem 4

- Run the image Nginx
- Add html static files to the container and make sure they are accessible
- Commit the container with image name IMAGE_NAME

## Run the image Nginx

![alt text](images/image-19.png)

![alt text](images/image-20.png)

## Add html static files to the container and make sure they are accessible

![alt text](images/image-21.png)

![alt text](images/image-22.png)

![alt text](images/image-23.png)

![alt text](images/image-24.png)

## Commit the container with image name IMAGE_NAME

![alt text](images/image-25.png)

---

# Problem 5

- Create a python simple app
- Create a dockerfile to containerize the python app
- Build the image and test it
- (Bonus)create a dockerfile for the same app in smaller size using multi staging
- Push the created image into your docker hub repo

## Create a python simple app

![alt text](images/image-27.png)
![alt text](images/image-26.png)
![alt text](images/image-28.png)

## Create a dockerfile to containerize the python app

![alt text](images/image-30.png)
![alt text](images/image-29.png)

## Build the image and test it

![alt text](images/image-32.png)

---

## (Bonus)create a dockerfile for the same app in smaller size using multi staging

![alt text](images/image-34.png)
![alt text](images/image-33.png)
![alt text](images/image-35.png)

---

## Push the created image into your docker hub repo

![alt text](images/image-36.png)
![alt text](images/image-37.png)
