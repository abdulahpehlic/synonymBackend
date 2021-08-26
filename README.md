# Synonym Application

This app is used to retrieve and create synonyms for a word.  

The app has been tested by SonarQube, and all the issues are reviewed/fixed.  
All the controller endpoints, as well as service methods with custom logic, have unit tests.  

The app is deployed to Heroku, and linked to this GitHub repository. Whenever a new commit is pushed, the Heroku app will be rebuilt with the latest commits. 
The following link leads to the Heroku app: https://stormy-tor-83845.herokuapp.com/ 

You can test the app using endpoints provided at the end of this file, or use the Angular frontend app deployed at Heroku:  
http://reinvent-synonym.herokuapp.com/ 

To run the app follow the steps below:

##### 1. Make sure nothing is running on port 8080  
##### 2. Install Lombok for your IDE:  

-Download the open source Lombok.jar here: https://projectlombok.org/downloads/lombok.jar  

-Run the jar and specify the directory where your IDE is installed  

-Here's a guide to installing Lombok for various IDE's: https://projectlombok.org/setup/overview  

Introducing Lombok to a project may seem like a hassle but it comes with several advantages, such as code simplicity.  


##### 3. Run the app with your IDE
##### 4. Endpoints
_______________________________________________________
Endpoints description:
###### -Retrieving synonyms by wordString(path variable) -> returns a list of synonyms:
`Method type: GET`

`Path: api/words/{wordString}`  

###### -Check for existings synonyms with the same description:
`Method type: GET`

`Path: api/words/check/{description}`

###### -Add synonyms (stores new synonyms into the database):
`Method type: POST`

`Path: api/words/add`

`RequestBody: You must provide syonyms list as a JSON object in the following form:`

```
[
    {
        "word": "cell",
        "description" : "smallest living organism"
    },
    {
        "word": "germ",
        "description" : "smallest living organism"
    }
]
```
_______________________________________________________
