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






