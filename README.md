# First_Docker_Container
Sample Application Running on Docker container

NOTE: Check corrosponding images in the repo in case if you want to.

In this small project I am going to show you how to set up container and run the container.

Step 1: Unzip the folder called app.zip in to your terminal

Step 2 Now we will build the docker file called dockefile and then use that file to build the container Image.

Dockerfile Content:

FROM node:10-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "/app/src/index.js"]

check docker.png for more info...

Now run the following commands in your terminal

docker build -t docker-101 .

then 

docker run -dp 3000:3000 docker-101

if you visit the port 3000 then you winn see the application running on the browser.


you can use following commands to stop remove and restart the container in case if you want to make some changes in to source code.

you need to run the following command in order to get hte conatiner id first.

try this: container ps

Stop the container:  container stop <container-id>
  
Start the container: docker run -dp port:port docker-image

remove the container: container rm <container-id>

Check how to get container ip in docker_id.png....

Great! you just finished setting up and running the container.

Now, we can share this container Image with our community so other people can use it.


To push an image, we first need to create a repo on Docker Hub.

    Go to Docker Hub and log in if you need to.

    Click the Create Repository button.

    For the repo name, use 101-todo-app. Make sure the Visibility is Public.

    Click the Create button!

If you look on the right-side of the page, you'll see a section named Docker commands. This gives an example command that you will need to run to push to this repo.

In your newly created instance if you run the following command then you can see the app running on your browser

docker run -dp 3000:3000 sagar240894/101-todo-app


For more info. go to Docker website and try play with docker. You will see the steps above to fulfill your requirements.

Hope this helps.
