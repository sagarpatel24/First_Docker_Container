# First_Docker_Container
Sample Application Running on Docker container


In this small project I am going to show you how to set up container and run the container.

Step 1: Unzip the folder called app.zip in to your terminal
Step 2 Now we will build the docker file called dockefile and then use that file to build the container Image.

Dockerfiel Content:

FROM node:10-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "/app/src/index.js"]


Now run the following commands in your terminal

docker build -t docker-101 .

then 


docker run -dp 3000:3000 docker-101

if you visit the port 3000 then you winn see the application running on the browser.
