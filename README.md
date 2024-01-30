# Travel-Memory-Application-Deployment

The TravelMemory application has been developed using the MERN stack. The application consists of frontend & backend which are developed using JavaScript programming language.

## Objectives :
-	Set up the backend running on Node.js.
-	Configure the front end designed with React.
-	Ensure efficient communication between the front end and back end.
-	Deploy the full application on an EC2 instance.
-	Facilitate load balancing by creating multiple instances of the application.
-	Connect a custom domain through Cloudflare.

## Backend Configuration
-	Access the complete codebase of TravelMemory Application from the GitHub link.
   https://github.com/UnpredictablePrashant/TravelMemory
-	Clone the complete repository and navigate to the backend directory of the TravelMemory application.
-	Make the necessary changes into the codebase as mentioned in the README.md file in the repository.

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/ee0f29c3-584b-4d3f-bd63-3f707c6d7c7e)

-	Update the .env file in the backend directory of the application to incorporate with the database connection details and port information.
-	To connect the backend with the database utilize Mongo DB compass and enter the Mongo DB URL and the port number in the .env file.
-	Configure the backend to run on PORT=3000 and set up the reverse proxy by installing Nginx and run it on PORT=80.
-	To set up the reverse proxy make the necessary changes in the /etc/nginx/sites-available/default file with the details of the subdomain and the proxy_pass = http://webserver.
  
![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/5c50203d-ff64-45b4-82a3-da7367f7c4cc)

-	If the reverse proxy setup is done successfully, this is how the backend application with the subdomain looks like.

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/2d5276ff-81ad-49c2-98c8-e1763c69776f)

## Frontend And Backend Connection
-	Navigate to the frontend directory of the application and in the url.js file update it with the subdomain of the backend application.
-	Also make the necessary changes in the package.json file, so that the frontend application runs on the preferred port number when the servers are up.
-	Follow the same steps for the reverse proxy setup as done in the backend application.

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/d878594d-a13d-4e4d-bf2d-c0a7afe20551)

-	If the reverse proxy setup for the frontend is done successfully, this is how the frontend application with the subdomain looks.

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/7cfb662a-69fc-40b5-a1f0-d01f4222b83d)

## Scaling the Application
-	To scale the application, we need to create multiple instances with the same configurations by creating the snapshots of the frontend and backend application.
-	We need to create the AMI and launch new instances using the AMI.

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/0864396d-0ae3-4384-80a9-4630d5191dc1)

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/60732a16-119c-439b-ab4c-5c9879390bfa)

-	We need to create a load balancer to ensure the efficiency of incoming traffic.
-	Create the application load balancers by specifying the instances into their respective target groups.

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/c0ca51ff-41fd-4314-a4fd-5bfee7ce3679)

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/104fdbe9-c56e-4fa9-8282-cc6151193c51)

## Domain Setup with CloudFlare
-	Connect your custom domain to the application using Cloudflare.
-	Create a CNAME record pointing to the load balancer endpoint of the backend.
-	Create an A record with the IP address of the EC2 instance hosting the frontend.

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/7e47b17e-8b9e-4a4f-a30b-c8a9f34530d3)

## Successful Deployment

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/b212d59b-d0b5-4ce1-808e-c20b66fe4073)

![image](https://github.com/TeamKanyarasi/Travel-Memory-Application-Deployment/assets/139607786/c20e9441-9717-4466-a975-4c10bd3aa86b)

