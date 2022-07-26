# Create support manager module

The support manager module includes a set of functions that will assist us executing our calls, this functions are not API related

There is a function to load a yaml file, another to load a json file, one to get arguments from the terminal and finally two functions to do some pretty printing

## Open Support Manager file

Browse repository and open the file to work on the support functions

    .
    ├─ modules/
       └─ support_manager.py

## Create an argument parser

The API methods need some parameters to be provided by the user, 

Use the argparse module to obtain the following arguments from the terminal

* action
* resource
* payload (to be loaded from a json file)

## Create the config YAML file

We will use a YAML config file to provide our script with the required parameters to connect to vmanage

Open the config file

    .
    ├─ config/
       └─ config.yaml

Create the following key/value pairs

* VMANAGE: 10.89.1.134
* PORT: 443
* USERNAME: apilover
* PASSWORD: Cisco12345!

## Load YAML file

We will now use the yaml module to load the config file and load the values into our code

Create the function to acomplish this, since these values are mandatory, please also consider to use inputs and ask the user for the values not present on the file

## Create a JSON file with a new user

Go back to the vmanage API documentation and retrieve a sample call with the users defined at the moment

Open the payload file

    .
    ├─ config/
       └─ payload.json

Copy the output from vmanage and modify the text to create a new test user

* group : netadmin
* description : Python Test User
* username : test_YOURCEC
* password : cisco12345
* locale : en_US
* resGroupName : global

## Load JSON file

We will now use the json module to load the payload file and load the values into our code

Create the function to acomplish this

## Create a print dictionary function

Create a function to print all keys and values of a dictionary side by side

## Create a print table function

Use tabulate module and create a function to print the data from our GET requests

It should use the keys of the json data to create a "first row" with the headers of the table

## Add last argument to our parse function

Now that we have two print options we can use another argument to decide to do a simple format print or a table print

Include this argument to the parser

## Test the support functions

Open the test support file on the root of the repository

    .
    ├─ test_support.py

Use the provided sample-data for your testing

* Import the support module
* Use the help to display the argument options
* Use terminal to provide different arguments and print them
* Load and print the values from a YAML file
* Load and print the values from a JSON file
* Use print_formatted function to print a dictionary
* Use print_tabulate function to print a table from a dictionary

If any issues compare your code to the one on the following links

<a href="https://wwwin-github.cisco.com/rgomezbe/vmanage_api/blob/master/modules/support_manager.py" target="_blank">support_manager.py</a>

<a href="https://wwwin-github.cisco.com/rgomezbe/vmanage_api/blob/master/test_support.py" target="_blank">test_support.py</a>
