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

```bash
npm install -g firebase-tools

firebase login

cd your-frontend-project

firebase init hosting

firebase serve

firebase deploy

```

