# Catalog Project - Udacity Full Stack  

## About This Application

* The application can be accessed via a web browser at this url/address `http://localhost:5000`, once the server is running (steps provided below).  
* The user must have a Google account in order to do anything other than view categories and items.  
* The application will provide the user with a login page using their Google account information.  
* The application will not allow a user the Edit or Delete catagories created by another user.
* The application will not allow a user to Add, Edit or Delete items in a category created by another user.  
* JSON endpoint are provided as described in the JSON Endpoints section of this document.  

## Environment

The following were used for the development and testing of this project:  
* sqlite
* Python 2.7
* Eclipse Version: 2018-12 (4.10.0)
* FireFox Quantum 64.0
* Google Chrome Version 73.0.3683.86 (Official Build) (64-bit)
* VirtualBox Version 5.2.22 r126460 (Qt5.6.2)
* Vagrant Version 2.2.2
* Postman [Get Postman](https://www.getpostman.com/downloads/)
* Files required to operate the server and application are located in the catalog.zip file.
If you are familiar with vagrant environments and have one established with the suggested software from the this section,  
then load the contents of the supplied catalog file into a new directory under vagrant. Else follow the directions below.  

To establish the environment used by the author do the following:  

1. Downlod the Udacity Full Stack Wed Developer virtual machine setup from Github  [https://github.com/udacity/fullstack-nanodegree-vm](https://github.com/udacity/fullstack-nanodegree-vm)  
 and follow the directions on how to perform the installation.  
1. Load the files and directories supplied in the catalog.zip file into `/FSND-Virtual-Machine/vagrant/catalog` using windows explorer.
note that the root of the directory path will depend on where you installed the package.  
1. It is not necessary to run the database in the instructions as one has been provided in the catalog file.  
1. From wherever you installed the vm package use a command line tool such as Git Bash  
for the following commands.  
1. `cd /FSND-Virtual-Machine/vagrant/ `  
1. `vagrant up`  
1. `vagrant ssh`  
1. `cd /vagrant` 
1. `cd catalog`  
 
The Database Setup and Running the Server sections will be performed inside the catalog directory.

## Database Setup

* A sample database is supplied with sample data and is named itemcatalog.db  
* Optionally a new blank database can be created by running `python database_setup.py`  
* Optionally the new blank database can be loaded with data by running `python loaddatabasecontent.py`

## Running the Server

1. Use python to run the server application from the catalog directory: `python application.py`  
1. Once the server is up the catalog application can be accessed via a web browser at this url/address `http://localhost:5000`  

## JSON Endpoints

The follwing JSON endpoints are available.<br/>
The examples are intended to work with the author supplied populated database.  
1. Return all the items in a category: `http:localhost:5000/category/<int:category_id>/item/JSON`  
     -example: `http://localhost:5000/category/1/item/JSON`  
1. Return a particular item in a category: `http://localhost:5000/category/<int:category_id>/item/<int:item_id>/JSON`  
     -example: `http://localhost:5000/category/1/item/1/JSON`  
1. Return all the categories: `http://localhost:5000/category/JSON`  
     -example:  `http://localhost:5000/category/JSON`  
1. Return all the users: `http://localhost:5000/users/JSON`  
     -example:  `http://localhost:5000/users/JSON`  
1. Return all the categories owned by a particular user: `http://localhost:5000/user/<int:user_id>/categories/JSON`  
     -example:  `http://localhost:5000/user/1/categories/JSON`  


## Acknowledgements

- Udacity Full Stack Web Development - Catalog Project.
- Stack Overflow for help by reading previously answered questions about flash, flask, Google OAuth2.
- python validation - [PEP8 online tool](http://pep8online.com/)
- Google OAuth2 documentation