# StoraTAG
# Team Members
Nandini, Jayant, Aryan, Maiv, Ereena

# About the Project
The project helps reduce wastage of food and increase the mobility and management over food. It is basically for supervision of food in granaries or cold storage to prevent damage and have easy access over food information(details like harvest day, possible expiration, cost price, possible selling price). For small grainery owners it can save a lot of money as sometimes product brought for more is sold for cheaper due to mismanagement. A remote website with all the information of stock can help in seamless trade and save resources.

The goal of the project was to create a mass food storage system that could be used to remotely monitor and manage food granaries or cold storage. StoraTAG is an RFID-enabled mass storage system that helps reduce food waste and improve food mobility and management by allowing us to trace the lifecycle of a sack from the time it enters the storage unit until it exits. It also uses a UID system (Unique Identification System) to distinguish sacks from one another and stores their related data in a database, making it simple for the user to track the status of the sacks from our StoraTAG website.

## Advantages

- Assists in real-time monitoring of product availability.
- Helps in tracking the exact location of food products.
- Includes minimizing food waste and improving food mobility and management.
- Helps in inefficient cost and fuel consumption management. It can save a lot of money for small granary owners because goods brought in at a higher price are sometimes sold for a lower price owing to poor management.
- A remote website with all stock information can aid in seamless commerce and resource conservation.

## Physical Schematic


The physical system reflects the many objects and relationships that those objects will have, as depicted in the diagram above. The given system can be scaled up or down depending on the needs (as the number of sacks increases, so does the number of tags).

## Software Goals

- Allows the user to check the status of various sacks using their UID on our StoraTAG website.
- Allows the user to review food information (details like harvest day, possible expiration, cost price, possible selling price, etc.) for each and every sack in the cold storage.
- Allows the user to maximize earnings while also displaying the expiration date of our sacks on the website, reducing spoilage and wastage.

## High-level Architecture

### System Architecture/Component Diagram



A run-through depiction of major system components that come together to make StoraTAG work is shown above.

### Software Architecture



The user can use the front-end client to access the system by going to the web server (server.js). The system's landing page is a login page, from which the user can either enter a valid username and password or establish an account that will require a password to verify.

## Functions

### Login Function

The login page is designed to authenticate users' login information, such as username, email, password, and password confirmation.



### Insertion Function

Insertion page is designed to add or remove sacks containing food information.



## System Components

### Data Flow



### Website Design



### Data Storage



### Device and Data Communication


## Setup Guide

### Step 1: Cloning Repository

Generate a clone GitHub repository containing all the frontend and backend files.



### Step 2: Starting Login Page

Changing directory to registration and login page (based on MEAN stack) folder and then starting the Node.js server by using command - node server.js.



### Step 3: Starting the web server and API

Changing directory to Updated front end + mqtt 2 folder and then starting the web and API server individually from their directories, by running the command npm start.



### Step 4: Initializing RFID Reader

Setup RFID scanner with ESP32 as shown in the given pictures as each color is dedicated to a different pin.



### Step 5: Setting up RFID server

Open rfid_ver1 folder, then at line number 12, col 28 paste the serial-port name with which we are communicating to RFID scanner.

At last, open the terminal change directory to rfid_ver1 folder, then run the server with npm start.



## User Guide

When a user visits the StoraTAG website, they will first encounter a login screen. In order to access the homepage, they must provide their login credentials. If the user forgets the password, they can click on forgot password or for registration they can click on register here and they will get redirected to the registration page.


As it can be seen from the above image, we have registered user as aryan and those credentials are also shown in our MongoDB database as users.


As the user fills the correct credentials, they would be directed to the homepage of StoreTAG.

This is our StoraTAG homepage, where we can see profile data at the top with parameters such as name and email ID, as well as a Logout button in the upper right corner that will take us back to the Login page.

In our Home page, we have a navbar with additional features such as a web page for entry of new sack data, and in addition, we can see stock in our navbar with which we can examine our inserted data.

We can see the UID for our sacks on the insert sack web page because when we scan our RFID tags to the scanner, they only need to be touched with it. A UID is a unique ID assigned to each tag, as seen in the diagram below. We must submit after entering each detail, and all data will be stored on the sack data web page via our own build api.

We can see this data at both backend and sack data web page.

The Error 404 page was built so that if the server or URL is incorrect, this page would appear, informing the user that something is wrong.

The feedback mechanism implemented to our navbar, as illustrated in the above image, is designed to allow users to provide us with valuable feedback. The image below displays the several parameters that the user will fill out (Name, email) as well as some remarks about our management system. The input might be negative or good depending on the user experience, which will allow us to adapt our system based on the feedback we receive.

When the user submits his/her response on our web app, we will get that response on our database. Ultimately a message will show up on our website after the submission of a response which will indicate that we have received the user’s response.
