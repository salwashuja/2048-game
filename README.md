**# 2048-game**

This repository contains a Dockerized implementation of the classic 2048 game. The game is deployed using AWS Elastic Beanstalk, leveraging Docker for containerization. The project aims to demonstrate a complete workflow from development to deployment in the cloud.

![image](https://github.com/salwashuja/2048-game/assets/172596215/65705ca8-7112-42da-84e5-b3fd062c3a18)

**# Features**

- Classic 2048 game mechanics
- Responsive design
- Dockerized application for a consistent environment across different platforms
- Deployment on AWS Elastic Beanstalk for scalability and ease of management

**# Technologies Used**

- HTML
- CSS
- JavaScript
- Docker
- AWS Elastic Beanstalk

**# Project Overview**
This Dockerfile automates the setup of an Nginx web server to host the 2048 game. By following the steps to build and run the Docker container, you can quickly deploy the game and make it accessible via a web browser. This project demonstrates the use of Docker to containerize a simple web application, providing a portable and reproducible environment.

![image](https://github.com/salwashuja/2048-game/assets/172596215/dd0da4c5-ef21-41ad-bf00-d51073ddeb4a)

**Build the Docker Image:**
Build the Docker image using the provided Dockerfile.

_docker build -t 2048-game ._

![image](https://github.com/salwashuja/2048-game/assets/172596215/3a2a81ef-a1cb-4cdb-a549-38914d9037a6)


**Run the Docker Container:**

Run the container and map port 80 of the container to port 80 of your host machine.

_docker run -d -p 80:80 <image_id>_

![image](https://github.com/salwashuja/2048-game/assets/172596215/d442d6c9-3104-420e-89f6-9b096e46da8a)

**Access the Game:**
Open a web browser and navigate to http://localhost:80 to access and play the 2048 game.

**Deploying the Dockerized 2048 game to AWS Elastic Beanstalk**

Let's go through the steps for deploying your Dockerized 2048 game to AWS Elastic Beanstalk using the AWS Management Console.

**Steps:**

**1. Create an Elastic Beanstalk Application**

Log in to the AWS Management Console and navigate to the Elastic Beanstalk service.
Click on "Create a new environment".
Select "Web server environment" and click "Select"

![image](https://github.com/salwashuja/2048-game/assets/172596215/947483a0-af28-476c-8aa7-ebf601e4a7b7)

**2. Configure Your Environment**

**Application Information:**

Application Name: Enter a name for your application, e.g., 2048-game.
Environment Name: Enter a name for your environment, e.g., 2048-game-env.

![image](https://github.com/salwashuja/2048-game/assets/172596215/9fc3c69a-e24e-476c-828a-3a19dd90792a)


**Platform:**

For Platform, select "Docker".
For Platform Branch, select the appropriate Docker version.

![image](https://github.com/salwashuja/2048-game/assets/172596215/64f26d9b-c8ce-4deb-8721-18d1e713d412)


**Application Code:**

Choose "Upload your code".
Click "Choose File" and upload the Dockerfile file you created earlier

![image](https://github.com/salwashuja/2048-game/assets/172596215/41aca166-20e5-4d31-b251-e5654e9bb3f2)

**3. Environment Settings**

**Environment Type:** Choose "Load balanced" or "Single instance" based on your requirement.
**Instance Type:** Choose an instance type. The default t2.micro is usually sufficient for a simple application.

![image](https://github.com/salwashuja/2048-game/assets/172596215/a9e98704-9aec-4f7e-a031-eaaebee7e0c9)


**Create Environment**   

Click "Create environment".
Elastic Beanstalk will start provisioning resources and deploying your Docker container. This process might take a few minutes.

**4. Access Your Application**

Once the environment creation is complete, you will be provided with a URL to access your application. Click on the URL to open your 2048 game in the web browser.

![image](https://github.com/salwashuja/2048-game/assets/172596215/64d9d78b-28d1-449c-ad9e-f533245c1bed)








