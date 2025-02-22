# microservices-docker-project

Prerequisites:
Docker and Docker Compose installed on your system.

Change to the directory where the ```docker-compose.yml``` file is located. This directory should also contain the ```spring-boot-app``` and ```node-app-docker``` folders.

Run the following command to build and deploy the containers in detached mode:
```docker-compose up -d --build```

Verify Running Containers:
```docker ps```

After the containers are running, perform a health check by executing:

```curl -s https://raw.githubusercontent.com/kkenan/basic-microservices/master/health_check.sh | bash```

The output should match the sample provided in the attached image, confirming that the services are operating correctly.

![image](https://github.com/user-attachments/assets/ea419e70-8655-41e9-921c-456914790533)

For cleaning containers and images, run the command:
```docker-compose down --rmi all```
