# Assignment - Full-Stack (TypeScript/Python)

The subject of this assignment is a small web application that acts as an interactive explorer for the characters from the movie franchise Star Wars.  If you are not familiar with Star Wars, don't worry, prior knowledge of the movies is not required to complete the assignment. The assignment has two parts, one is concerned with developing a thin back-end layer, while the other is concerned with creating a front-end for the back-end layer.

## Application Overview

The main purpose of the application should be to display the list of characters from the Star Wars universe. Clicking on one of the characters from the list should open a detail view of the corresponding character. The data for the application should be queried from an open API called [SWAPI (Star Wars API)](https://swapi.dev/) that should give access to all data that is needed to fullfill the requirements. However, access to the application should be granted to authenticated users only.

### Login
The login screen should be shown to unauthenticaed users and prompt the user for their credentials. Signing up for new accounts or resetting the account password is not required for this assignment.

### Character List
The character list should be a simple list that displays the name of the character. Each list entry should be clickable and open the detail view for the selected character when the user clicks the list entry.

### Filter
The filter should allow the user to filter the list of characters by the movie the character appeared in (i.e. show only characters that appeared in Episode IV: A New Hope). When the user changes the filter settings in the filter section, the list of characters should instantly adapt to only show characters that match the chosen filter settings. 

### Character Details
The character details that are shown when the user selects a character from the character list should show a brief summary of the character, including the name of the character, the movie the character appeared in, the species of the character (if available), and the spaceships associated with the character. For the character "Han Solo", for instance, the detail view should display the following information:

> **Name:** Han Solo  
> **Species:** Human  
> **Movies:** Episode IV, Episode V, Episode VI, Episode VII  
> **Spaceships:** Millenium Falcon, Imperial shuttle  


## Back-End Task (2-3h)

The back-end part of the assignment is concerned with creating a thin back-end API layer that acts as an API proxy for SWAPI with added features.

SWAPI is a public API and as such does not require any authentication to query the data. However, we do want to restrict access to our application to registered users only. Thus, it will be necessary to add authentication endpoints to our API layer. Additionally, SWAPI does not support server-side filtering of the provided data. Thus, it will be necessary to add server-side filtering to our API layer. As a minimum requirement, we want to be able to filter the characters by the movie they appear in. Preferably, we should come up with a generic solution that allows us to filter the characters by any attribute.

### Authentication

Authentication to our API layer should be implemented using token based authentication. JWT should be used as the access token format. An access token should be able to be acquired through a dedicated token endpoint that takes user credentials and returns a corresponding access token. All other API routes should be secured and only return data when authenticating with a valid access token. Access tokens should be short-lived and expire after 10 minutes. Refreshing access tokens is not required for this assignment. Valid user credentials CAN be hard coded for this assignment.

### Technical Details

The API layer should be implemented in Python and use a modern, ASGI compliant web framework, such as Sanic or FastAPI.

## Front-End Task (2-3h)

For the front-end part of the assignment, you will need to create a front-end application that satisfies the requirements stated in the Application Overview section.

### Project Setup
We should be able to start the application using the `npm start` command. The app should use the latest major version of your front-end framework of choice.

### External Libraries
You are allowed to use any external library to complete this task. You are also allowed to use UI libraries. Please make sure that the application looks appealing, consistent, and has a good user experience.

## How to Work on This Assignment
* Clone this repository
* Create periodic commits with meaningful commit messages
* If you don't want to create a public repository for this assignment, please invite us to your private repository
* Make sure to include a brief description on how to run your solution
* If you have any questions, feel free to contact us at jobs@rocketloop.de

Please note that we will not be able to accept solutions without periodic commits or if we are unable to run your solution.
