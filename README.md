# todolist_app
<br>
Guidelines to run web app locally
<br>
- For this app to work, you need to configure the following environment variables in your .env file in the root directory.<br>
MONGODB_USERNAME=<value> 
<br>
MONGODB_PASSWORD=<value>
<br><br>
- Use these commands to run the application

```bash
# to install dependencies 
npm install

# to run the server
nodemon app.js

```

- Open `http://localhost:4000` with your browser to see the application.

<br>
<h2>Firebase hosting</h2><br>
1. Install Firebase CLI <br>

```bash
npm install -g firebase-tools
```
<br>
2. Login to Firebase <br>

```bash

firebase login
```
<br>
3. Navigate to your frontend project directory: <br>

```bash
cd your-frontend-project

firebase init hosting

firebase serve

firebase deploy

```
<br>
<h2>EC2 Hosting</h2><br>
1. Launch an EC2 Instance <br>
Log in to the AWS Management Console.
Navigate to EC2 and click Launch Instance.
Configure the instance:
<br>
-Choose an Ubuntu Server or any preferred OS AMI.<br>
-Select an instance type (e.g., t2.micro for free tier).
Configure security groups to allow:
<br>
-Port 22 (SSH) for access.<br>
-Port 80 (HTTP) for web traffic.<br>
Additional ports (e.g., 3000 for Node.js, 5000 for Flask) as needed.
Launch the instance and download the key pair file (.pem).
<br><br>
2. Connect to the Instance via SSH <br>
Open Windows Terminal or PowerShell. 
Navigate to the folder with your .pem file.<br>
Run the SSH command:<br>

```bash

ssh -i "your-key-file.pem" ubuntu@<Public-IP-of-EC2>

```
<br>
3. Set Up the Server Environment <br>
Update and install required packages: <br>

```bash

ssh -i "your-key-file.pem" ubuntu@<Public-IP-of-EC2>

```
<br>
4. Deploy the Backend Application <br>
Copy your backend files to the EC2 instance using SCP or Git:<br>
To upload files: <br>

```bash

scp -i "your-key-file.pem" -r /path/to/backend ubuntu@<Public-IP-of-EC2>:/home/ubuntu/

```
<br>
Navigate to the backend directory and install dependencies:<br>

```bash

npm install

```
<br>
Start the application: <br>

```bash

node app.js

```
