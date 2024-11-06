# docker-swarm-replicas
# what is replicas
In docker replicas are used to create multiple instance of a service in docker swarm environment.
This is especially useful for load balancing it allow you to distribute workload across  multiple containers
# Steps to create replicas
1)To generate the token the commands
docker swarm init
![Screenshot 2024-11-06 194507](https://github.com/user-attachments/assets/acbbe1b6-d33e-44cf-83c8-4ab80b2441ee)
2) copy the token in the above image
3) To create the worker node copy the token and then paste the token insecond server and third server 
![Screenshot 2024-11-06 195108](https://github.com/user-attachments/assets/62ba0269-7968-41a2-84a6-6c91d1df7285)
To list the node commands is
docker node ls
4)To create the service in manager node with replicas by the command is 
docker service create --name gpay --replicas 3 --publish 80:80 httpd
![Screenshot 2024-11-06 200046](https://github.com/user-attachments/assets/2027bff9-b193-4f8f-98ca-29a727d5edce)
5) By using Dockerfile we can create the image as shown in below image
![Screenshot 2024-11-06 202149](https://github.com/user-attachments/assets/6cbd91d0-9a93-42b2-81b0-f2abed39e6f1)
6)To get html page for login type html page for login in w3 school copy the code
Create index.html file in manager node with vi index.html and paste the copied html code in editor and save it
 7)Build the image by using command is
 docker build -t image .
 8) by using public ip and port number which we gave we can see as below
 ![Screenshot 2024-11-06 202254](https://github.com/user-attachments/assets/6631dc40-bf64-4ec2-9c9d-940ec10059d6)
 9)To create the service with created image by the command is
Docker service create –name paytm –replicas 3 –publish 81:80 image
10) Go to docker hub and create the repository in docker hub
    then give command docker login the provided username and password
11) Type docker push prashanth957/docker it will push to docker hub
Now create the service by command
docker service create --name phonepe --replicas 10 --publish 83:80 image 
Check the images by using command docker images and copy the recently created image 
![Screenshot 2024-11-06 205623](https://github.com/user-attachments/assets/e3a65a75-9f52-4a7d-b0f6-a5939347bba3
If u stop the container wontedly then that container will start immediately in the server 


