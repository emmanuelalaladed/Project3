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

![Database](./images/DB.PNG)

3. Create a new Network access to allow all network.
    ![network-Access](./images/Netaccess.PNG)

4. Create a new hidden file called "env" inside  "Todo" directory and add a collection string to access the database created. The Database access is place inside the hidden file ".env" to make it secured.

  ![env](./images/env.PNG)

  - The collection string can be retrieved from the cloud Mongodb as shown below

    ![Step1](./images/collection1.PNG)

    ![Step2](./images/collection2.PNG)

5. Edit the initial created "index.js" file as replaced with the new script as shown below
   ![New_index_file](./images/index-js.PNG)

6. Launch the server using 
    
    *node index.js*

    ![Server-Launch](./images/ServerAccess.PNG)





### Testing Backend Code without Frontend using RESTful API

Install Postman to test the backend created even when the fronend is not available. Then perform the following
1.  Create a POST request to the *API* using the link *http://*ec2-44-202-166-238.compute-1.amazonaws.com:5000/api/todos*
  ![POST access](./images/post%20access.PNG)

- Set the Header and the body has shown below, then click *send*
  
![Header](./images/Post-header.PNG)
![Body](./images/Post-body.PNG)

- Click *Send* to test the backend created

 ![Post](./images/Post.PNG)

2. Create a GET request from the API from the same link *http://*ec2-44-202-166-238.compute-1.amazonaws.com:5000/api/todos* t retreive the records from the To-do application from the backend.

 - Set the Header as shown below and click *send*

   ![Get-Header](./images/Post.PNG)
- Click *Send* to acccess the backend application To-do.
   ![Get](./images/GET.PNG)




## STEP 2: FRONTEND CREATION
 We will create the Web client to connect witht the backend application via API.

 1. In the Todo directory run the command below, to create a new directory called **client * in *Todo* directory.
    
      *npx create-react-app client*
2. Running a React App

   - First install *concurrently* to run multiple commands at the same time on the same terminal
    *npm install concurrently --save-dev*

    - Then install *nodemon* for server running and monitoring.
     *npm install nodemon --save-dev*
    
    - Edit the *package.json* 
    ![Nodemon](./images/nodemon%20script.PNG)

3. Configuration of Proxy in package.json
 - Navigate to *client*  using *cd client*
 - Open the *package.json* file using *vi package.json* 
 - Add the key value pair inside the *package.json* using

 *"proxy": //localhost:5000*
   ![Client key value](./images/client%20file.PNG)

4. Run *npm run dev* inside the Todo directory.The result is below

   ![run-server](./images/runserver.PNG)

5. Add port 3000 to the allowed port number
   ![port3000](./images/port%203000.PNG)

6. Launch the app using the public address with port 3000
   ![Lauchapp](./images/app-opening.PNG)

 ### Creating your React Components
 1. Navigate into *client* directory, then into *src* directory. Inside the *src* directory create directory *components*
    ![Create](./images/client%20create.PNG)
  
2. Navigate in the newly created directory and create  three files Input.js, ListTodo.js and Todo.js
 ![Create-files](./images/inside%20folder.PNG)

3. Open the file *Input.js* and paste the provided script.
   ![imput](./images/Input.PNG)

4. Install Axios insode the client directory using
   *npm install axios*


5. Navigate into *components* directory and paste the provided script into the *ListTodo.js* file.
   ![ListTodo](./images/ListTodo.PNG)

6. Inside *Todo.js* file paste the script provided
   ![Todo](./images/Todofile.PNG)

7. Inside the *src* directory replace the content in *App.js* with the provided script.

  ![App](./images/App.js)
  
8. Replace the script inside *App.css* file in *src* directory with the provided script.

   ![Appcss](./images/Appcss.PNG)


9. Inside the *src* directory replace the script inside the *index.css with the provided script.

   ![indexcss](./images/indexcss.PNG)


10. Back to the *Todo* directory and run *npm run dev*

    ![startserver](./images/startnpm.PNG)

11. Access the To-Do app vis the *localhost:3000*

    ![TodoApp](./images/Todoapp.PNG)