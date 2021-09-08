**MEAN STACK DEPLOYMENT TO UBUNTU IN AWS**

Task
In this project we are going to implement a simple Book Register web form using MEAN stack.

**Step 1: Install NodeJs**

Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine. 
Node.js is used here to set up the Express routes and AngularJS controllers.

**Update ubuntu**

sudo apt update
![image](https://user-images.githubusercontent.com/67065306/132577155-616a1b02-4f4f-42d5-9a81-172dae65aee3.png)

**Upgrade ubuntu**

sudo apt upgrade
![image](https://user-images.githubusercontent.com/67065306/132577651-5fe08dfc-fbc1-49bb-8aea-308088f31857.png)


**Install NodeJS**

sudo apt install -y nodejs
![image](https://user-images.githubusercontent.com/67065306/132579868-5fc55672-9664-461e-854f-77dd42b4108c.png)

**Step 2: Install MongoDB**

MongoDB stores data in flexible, JSON-like documents. Fields in a database can vary from document to document and data structure can be changed over time. 
For our example application, we are adding book records to MongoDB that contain book name, isbn number, author, and number of pages.

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6
![image](https://user-images.githubusercontent.com/67065306/132580644-0ebf902d-df30-44b0-9f84-3f55e5afb9b6.png)

echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list

![image](https://user-images.githubusercontent.com/67065306/132581174-71ea7036-82d1-41b8-a475-6434e5dac1b3.png)

**Install MongoDB**

sudo apt install -y mongodb
![image](https://user-images.githubusercontent.com/67065306/132581358-c0665e6e-da22-4004-94e6-9126fd25e9dd.png)

**Start The server**

sudo service mongodb start

Verify that the service is up and running

sudo systemctl status mongodb
![image](https://user-images.githubusercontent.com/67065306/132581920-b3154c83-6946-45b2-a278-bec30a670d7c.png)

**Install** [npm](https://www.npmjs.com) – **Node package manager.**

sudo apt install -y npm

![image](https://user-images.githubusercontent.com/67065306/132582469-8fb05839-8463-466d-9853-4f671eab2ed6.png)

**Install ‘body-parser package**

We need ‘body-parser’ package to help us process JSON files passed in requests to the server.

sudo npm install body-parser

![image](https://user-images.githubusercontent.com/67065306/132582945-57a2f360-1fa9-48ec-90e9-fe1f920731c2.png)

**Create a folder named ‘Books’**

mkdir Books && cd Books

In the Books directory, Initialize npm project

npm init

![image](https://user-images.githubusercontent.com/67065306/132584000-f7525b86-78bc-40a2-82b3-63a1aaf4110a.png)

Add a file to it named server.js

vi server.js 

![image](https://user-images.githubusercontent.com/67065306/132584381-e2353281-b263-4a1a-953e-b9425c09b104.png)

**INSTALL EXPRESS AND SET UP ROUTES TO THE SERVER**

**Step 3: Install Express and set up routes to the server**
Express is a minimal and flexible Node.js web application framework that provides features for web and mobile applications. 
We will use Express in to pass book information to and from our MongoDB database.
We also will use Mongoose package which provides a straight-forward, schema-based solution to model our application data. 
We will use Mongoose to establish a schema for the database to store data of our book register.

sudo npm install express mongoose

![image](https://user-images.githubusercontent.com/67065306/132584904-bd275855-f90a-4ea8-afe8-9f481414b9ac.png)

In ‘Books’ folder, create a folder named apps

mkdir apps && cd apps
Create a file named routes.js

vi routes.js
Copy and paste the code below into routes.js


In the ‘apps’ folder, create a folder named models

mkdir models && cd models

Create a file named book.js

vi book.js
Copy and paste the code below into ‘book.js’

![image](https://user-images.githubusercontent.com/67065306/132585801-3e5c0ca1-68bc-4cbe-a272-b1617f884e92.png)


**Step 4 – Access the routes with AngularJS**
AngularJS provides a web framework for creating dynamic views in our web applications. 
In this task, we use AngularJS to connect our web page with Express and perform actions on our book register.

Change the directory back to ‘Books’

Create a folder named public

mkdir public && cd public

Add a file named script.js

vi script.js

Copy and paste the Code below (controller configuration defined) into the script.js file.

![image](https://user-images.githubusercontent.com/67065306/132586534-a1f7b3f0-31a7-497c-b50d-f5bddea194ce.png)


In public folder, create a file named index.html;

vi index.html
Cpoy and paste the code below into index.html file.

![image](https://user-images.githubusercontent.com/67065306/132586847-ab6fcb28-f01b-427d-9ab3-8633e01b80bd.png)

Will change the directory back up to Books

cd ..

We will start the server by running this command:

node server.js

![image](https://user-images.githubusercontent.com/67065306/132590655-7b377cd8-f0b3-45a2-8980-b4d3635983c6.png)

