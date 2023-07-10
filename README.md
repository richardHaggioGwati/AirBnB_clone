# The AirBnB Clone Project

![AirBnB Logo](https://assets.entrepreneur.com/content/3x2/2000/1405612741-airbnb-why-new-logo.jpg)

## Project Description
This is the first part of the AirBnB clone project where we worked on the backend of the project whiles interfacing it with a console application with the help of the cmd module in python.

Data (python objects) generated are stored in a json file and can be accessed with the help of the json module in python

## Description of the command interpreter:
The interface of the application is just like the Bash shell except that this has a limited number of accepted commands that were solely defined for the purposes of the usage of the AirBnB website.

This command line interpreter  serves as the frontend of the web app where users can interact with the backend which was developed with python OOP programming.

Some of the commands available are:
- show
- create
- update
- destroy
- count

And as part of the implementation of the command line interpreter coupled with the backend and file storage system, the folowing actions can be performed:
-   Creating new objects (ex: a new User or a new Place)
-   Retrieving an object from a file, a database etc…
-   Doing operations on objects (count, compute stats, etc…)
-   Updating attributes of an object
-   Destroying an object

## How to start it
These instructions will get you a copy of the project up and running on your local machine (Linux distro) for development and testing purposes.

## Installing

You will need to clone the repository of the project from Github. This will contain the simple shell program and all of its dependencies.

```
https://github.com/richardHaggioGwati/AirBnB_clone.git
```

## How to use it
It can work in two different modes:


**Interactive** and **Non-interactive**.

In **Interactive mode**, the console will display a prompt (hbnb) indicating that the user can write and execute a command. After the command is run, the prompt will appear again a wait for a new command. This can go indefinitely as long as the user does not exit the program.

```
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$
```

If the shell is launched in **Non-Interactive** mode with a command input piped into its execution so that the command is executed as soon as the Shell launches. No prompt will show up in this mode, and the user won't be required to provide any more input.


```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
```

## Format of Command Input

In the case of **Non-interactive mode**, orders must be piped through an echo in order to be sent to the console.

When the prompt appears in **Interactive mode**, the commands must be typed using a keyboard; they are then acknowledged when the enter key is depressed (new line). When this occurs, the console will make many attempts to run the command or, if none of them were successful, it will display an error message. In this mode, the **CTRL + D**, **CTRL + C**, **quit**, or **EOF** commands can be used to close the console.

## Arguments

Arguments should be seperated by a space for the code to run efficiently.

Example:

```

user@ubuntu:~/AirBnB$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
user@ubuntu:~/AirBnB$ ./console.py

```

## Available commands and what they do

This will be the recognizable commands by the interpreter are the following:

| Command                         | Description                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **quit or EOF**                 | Exits the program                                                                                                                                                                                                          |
| **-----**                       | **-----**                                                                                                                                                                                                                  |
| **help** or **help <command\>** | Provides a text describing how to use a command.                                                                                                                                                                           |
| **-----**                       | **-----**                                                                                                                                                                                                                  |
| **create <class name\>**        | Creates a new instance of a valid `Class`, saves it (to the JSON file) and prints the `id`.  Valid classes are: BaseModel, User, State, City, Amenity, Place, Review.                                                      |
| **-----**                       | **-----**                                                                                                                                                                                                                  |
| **show**                        | Prints the string representation of an instance based on the class name and `id`                                                                                                                                           |
| **Usage**                       | **show <class name\> <id\>** --or-- **<class name\>.show(<id\>)**                                                                                                                                                          |
| **-----**                       | **-----**                                                                                                                                                                                                                  |
| **destroy**                     | Deletes an instance based on the class name and `id` (saves the change into a JSON file).                                                                                                                                  |
| **Usage**                       | **destroy <class name\> <id\>** --or-- **<class name>.destroy(<id>)**                                                                                                                                                      |
| **-----**                       | **-----**                                                                                                                                                                                                                  |
| **all**                         | Prints all string representation of all instances based or not on the class name.                                                                                                                                          |
| **Usage**                       | By itself or **all <class name\>** --or-- **<class name\>.all()**                                                                                                                                                          |
| **-----**                       | **-----**                                                                                                                                                                                                                  |
| **update**                      | Updates an instance based on the class name and `id` by adding or updating attribute (saves the changes into a JSON file).                                                                                                 |
| **Usage**                       | **update <class name\> <id\> <attribute name\> "<attribute value\>"** ---or--- **<class name\>.update(<id\>, <attribute name\>, <attribute value\>)** --or-- **<class name\>.update(<id\>, <dictionary representation\>)** |
| **-----**                       | **-----**                                                                                                                                                                                                                  |
| **count**                       | Retrieve the number of instances of a class.                                                                                                                                                                               |
| **Usage**                       | **<class name\>.count()**                                                                                                                                                                                                  |
