# Create sdwan manager class

This module is a class to handle the authentication process and perform our app API calls

This class will be instantiated on a script file that we will use to execute all our functions

## Open SDWAN Manager file

Browse repository and open the file to work on the sdwan manager class

    .
    ├─ modules/
       └─ sdwan_manager.py

## Create the init method

Define the static parameters needed to connect to vManage

* server
* port
* username
* password
* host (Build it by concatenating server + ":" + port)

## Create the class methods

Lets steal the code we need from postman

* Open our postman test collection and go to the "authentication" request'
* Click on the code button on the left
* Choose the python option from the menu and copy the code 
* Paste code under the get_auth_cookie method of the class and modify as needed
* Do the same for the get_auth_token, send_request and logout methods* 

## Enhance send_request method

Our main method is not complete yet, we will need to do additional changes to enable the ability to perform the 4 basic CRUD actions

Add the following arguments to the method

* action
* resource
* body 

Add some exception handling and some friendly printing options to display a readable message in casy of any errors

## Final changes on init method

Since we want authentication to happen natively we are going to add a couple of things to our init method

* Create a cookie attribbute and assign it the value returned from the cookie method
* Do the same thing for the token

## Test the class

Open the test sdwan class file on the root of the repository

    .
    ├─ test_sdwan_class.py

* Import the class module
* Provide the basic connection attributes statically
* Start a session to vmanage (new class instance)
* Test printing the cookie and token
* Define an action, resource ('/device/monitor') and an empty body
* Send an api request
* Print the response 

If any issues compare your code to the one on the following links

<a href="https://wwwin-github.cisco.com/rgomezbe/vmanage_api/blob/master/modules/sdwan_manager.py" target="_blank">sdwan_manager.py</a>

<a href="https://wwwin-github.cisco.com/rgomezbe/vmanage_api/blob/master/test_sdwan_class.py" target="_blank">test_sdwan_class.py</a>