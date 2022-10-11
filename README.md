# API testing with Postman and continuous integration with Jenkins

## Tools

- Postman 
- Jenkins

## Setup

- clone this repository
- install all dependencies for this project with `npm install` 

## Jenkins Setup

- launch your Jenkins server
- navigate to Manage Jenkins > Manage Plugins 
- install `NodeJS Plugin`
- make sure that you have Pipeline and Pipeline: GitHub Groovy Libraries plugins installed 
- navigate to Manage Jenkins > Global Toll Configurations > NodeJS installations > Add Node JS
- choose version `NodeJs 18.10.0`
- to the name field add `18.10.0`

![alt text](./assets/node-setup.png)

## Running job in Jenkins

- create a new pipeline
- pipeline script from SCM
- SCM (Git)
- use the current repo URL(https://github.com/Kryvchenko/jenkins-test)
- build now

## Running test locally

- navigate to the project directory 
- open terminal
- to run the test: `npm run test`
- to generate a report: `npm run report` 
- to open the report navigate to the Newman folder and open the HTML file in your browser

## Run collection in Postman

- click the button bellow 
- fork the collection
- choose the environment:`QA dropbox env`
- run the tests

[![Run in Postman](https://run.pstmn.io/button.svg)](https://god.gw.postman.com/run-collection/23524391-c3a9ca84-b5cc-48c6-82aa-73e2c093ed3a?action=collection%2Ffork&collection-url=entityId%3D23524391-c3a9ca84-b5cc-48c6-82aa-73e2c093ed3a%26entityType%3Dcollection%26workspaceId%3Dbfaf19bf-cb6b-4016-93b7-65e73bb056db#?env%5BQA%20dropbox%20env%5D=W3sia2V5IjoidXJsIiwidmFsdWUiOiJodHRwczovL2FwaS5kcm9wYm94YXBpLmNvbS8yLyIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoiaHR0cHM6Ly9hcGkuZHJvcGJveGFwaS5jb20vMi8iLCJzZXNzaW9uSW5kZXgiOjB9LHsia2V5IjoiZmlsZUlkIiwidmFsdWUiOiJpZDppU0Jla2R3a1d4b0FBQUFBQUFBQU5RIiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImFueSIsInNlc3Npb25WYWx1ZSI6ImlkOmlTQmVrZHdrV3hvQUFBQUFBQUFBNEEiLCJzZXNzaW9uSW5kZXgiOjF9LHsia2V5IjoiZmlsZVBhdGgiLCJ2YWx1ZSI6Ii9Ib21ld29yay9JbnRyby50eHQiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiYW55Iiwic2Vzc2lvblZhbHVlIjoiL0hvbWV3b3JrL0ludHJvLnR4dCIsInNlc3Npb25JbmRleCI6Mn0seyJrZXkiOiJmaWxlTmFtZSIsInZhbHVlIjoiSW50cm8udHh0IiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImFueSIsInNlc3Npb25WYWx1ZSI6IkludHJvLnR4dCIsInNlc3Npb25JbmRleCI6M30seyJrZXkiOiJ1cGxvYWRVcmwiLCJ2YWx1ZSI6Imh0dHBzOi8vY29udGVudC5kcm9wYm94YXBpLmNvbS8yL2ZpbGVzL3VwbG9hZCIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0Iiwic2Vzc2lvblZhbHVlIjoiaHR0cHM6Ly9jb250ZW50LmRyb3Bib3hhcGkuY29tLzIvZmlsZXMvdXBsb2FkIiwic2Vzc2lvbkluZGV4Ijo0fV0=)