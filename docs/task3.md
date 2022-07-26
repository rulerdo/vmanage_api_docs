# Create Script File

Now it is time to create the script file, here we will execute all the class methods and support functions created on the previous tasks

## Open vManage API file

Browse repository and open the vmanage api file

    .
    ├─ vmanage_api.py

## Import the modules and functions

Import all functions from the support manager file

Import the sdwan manager class

## Load parameters from YAML

Use the load_yaml function to get the variables from config file

Extract all the parameters to indivudial variables to facilate usage

* vmanage
* port
* user
* pwd

This variables will be used later on the code

## Load arguments from Terminal

Use the get_arguments function to get the paramaters from the terminal

Extract all the arguments to individual variables to facilate usage

* action
* resource
* table

This arguments will be used later on the code

## Load request body from JSON

Use the load_payload function to get the data from json file and save it in a body variable

* body

## Create a new SDWAN manager class instance

Use the variables with the connection parameters to instantiate a new sdwan_manager object from the class

##  Send an API request

Use the arguments and the send_request method from the class to send an API call

Save the response into a variable called data

## Print API call response on terminal

Use the table argument to determine the format and print the data variable on the terminal with one of the print support functions

## Logout

Use the logout method to close the session from vmanage

## Test the vmanage_api script file

Execute the script with the following paramaters

    python vmanage_api.py -r "/device/monitor"

If any issues compare your code to the one on the following links

<a href="https://wwwin-github.cisco.com/rgomezbe/vmanage_api/blob/master/vmanage_api.py" target="_blank">vmanage_api.py</a>