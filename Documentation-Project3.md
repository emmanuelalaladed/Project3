# Project 3
## Step 1: Backend Configuration
   1. Update and Upgrade Ubuntu with commands

   - *sudo apt update*
   - *sudo apt upgrade*

   2. Get the location of Node.js in Ubuntu repositories and install Node.js
    - *curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - *
    
    - *sudo apt-get install -y nodejs*

   3. The Node.js installation command install both Node.js and NPM. To verify the instalation of both Node.js and NPM use the follwoing command
    - *node -v*
    - *npm -v*
    ![Node.js and NPM version](./images/Node-and-npm-version.PNG)

### Application Code Setup
    
1. Creatye new Directory for the To-Do project

      - *mkdir Todo*
![New Todo Directoruy](./images/New-Todo-Directory.PNG)

2. Make new changes inside the current Todo Directory and initialize the project to create the new project.jason file.

 - *cd Todo*
 - *npm.init*
 
 ![Initialization-of-Project](./images/npm-init.PNG)

 3. Confirm the newly created project.json file

  ![Newly-reated-project.json-file](./images/projectfile.PNG)


### Install Expressjs

1. use the command to install Expressjs

- *npm install express*
2.  Create a file called "index.js", then use *ls* to confirm the installation.

 - *touch index.js*

![List-of-files/folder](./images/list.PNG)

3. Install dotenv using the command

- *npm install dotenv*

![Dotenv](./images/dotenv.PNG)

4. Open the index.js file and place the code as shown below

    ![index-code](./images/index-code.PNG)

5. Verify that the server is working using the command

- *node index.js*

![Server-testing](./images/test%20the%20server.PNG)

6. Verify the new Website
 - curl -s http://169.254.169.254/latest/meta-data/public-ipv4
 ![Getting-the-Public-IP-address](./images/Checking%20the%20public%20address.PNG)
 

 - http://54.221.127:5000
  ![Express-website](./images/website.PNG)

  ### Model

1. Installing the Mongodb database for the app
- *npm install mongoose* 
- create a new directory  "model"inside parent directory "Todo"
    - *mkdir model*
- inside the new directory "model" create a new file called "todo.js"
  ![Create_todo_file](./images/mkdir.PNG)

- Edit "todo.js" file as shown below

  ![Todo.js_file](./images/mkdir.PNG)


2. Open the "api.js file inside the "route" directory and input the provided script.

    ![api_js](./images/api_js.PNG)


### Mongodb Database

1. create and new database called Monggodb
- ![mongoddb](./images/mondodb.PNG)

2. Create the database
![Mongodb](./images/mongodb2.PNG)

3. Create a new file inside "Todo" directory and add new script 
  ![env](./images/env.PNG)







