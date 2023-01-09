## DESCRIPTION OF THE PROJECT

The **AirBnB** clone project's goal is to deploy on your server a simple copy the *AirBnB website*.
After a 4 month period, you will have a complete web application composed of:
1. A command inteerpreter to manipulate data without a visual interface
2. A website that shows the final product to all: static and dynamic
3. A database or files that store data
4. An API that provides a communication interface between the front-end and your data

**But first...**
**The console**
- create your data model
- manage object via a console/command interpreter
- store and persist objects to a JSON file
The first piece is to manipulate a powerful storage system. This storage engine will give us an abstraction between "My object" and "How they are stored and persisted".
This means: from your console code and from the front-end and RestAPI you will build later, you won't have to pay attention of how your objects are stored
This abstraction will also allow you to change the type of storage easily without updating all of your codebase
The console will be a tool to validate this storage engine

![server_side_architecture](Images/server_side_architecture.png)

## DESCRIPTION OF THE COMMAND INTERPRETER

The command intepreter in this case is limited to a specific use case, since we want to be able to manage the objects of our project
- Create a new object
- Retrieve an object from a file, a databse etc...
- Do operations on objects
- Update attributes of an object
- Destroy an object

**How to start & use it**
The command line interpreter can be started by executng the command `./console.py`. The **console** can, *create*, *destory*, and *update* objects
Type `help` within the console to get a list of command options and its function

**Example in interactive mode:**
```bash
$ ./console.py
( hbnb ) help

Documented commands (type help <topic>):
========================================
EOF   help   quit

( hbnb )
( hbnb )
( hbnb ) quit
$
```
**Example in non-interactive mode:**
```bash
$ echo "help" | ./console.py
( hbnb )

Documented commands ( type help <topic>):
=========================================
EOF  help  quit
( hbnb )
$
$ cat test_help
help
$
$ cat test_help | ./console.py
( hbnb )

Documented commands ( type help <topic>):
=========================================
EOF  help  quit
( hbnb )
$
```

All tests should also pass in non-interactive mode: `$ echo "python3 -m unittest discover tests" | bash`
