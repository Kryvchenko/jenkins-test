# API testing with Postman and continuous integration with Jenkins

## Tools

- Postman 
- Jenkins

## Setup

- clone this repository
- install all dependencies for this project with `npm install` 

## Jenkins Setup for local run

- launch your Jenkins server
- navigate to Manage Jenkins > Manage Plugins 
- install `NodeJS Plugin`
- make sure that you have Pipeline and Pipeline: GitHub Groovy Libraries plugins installed 
- navigate to Manage Jenkins > Global Toll Configurations > NodeJS installations > Add Node JS
- choose version `NodeJs 18.10.0`
- to the name field add `18.10.0`

![alt text](./assets/node-setup.png)

## Running job in Jenkins localy

- create a new pipeline
- pipeline script from SCM
- SCM (Git)
- use the current repo URL(https://github.com/Kryvchenko/jenkins-test)
- build now

### Additionally, you can find `config.xml` and `logs` file in builds folder

## Running test locally

- navigate to the project directory 
- open terminal
- to run the test: `npm run test`
- to generate a report: `npm run report` 
- to open the report navigate to the Newman folder and open the HTML file in your browser

## Run collection in Postman

- click the button bellow 
- fork the collection
- choose the environment:`Updates env`
- run the tests

[![Run in Postman](https://run.pstmn.io/button.svg)](https://god.gw.postman.com/run-collection/23524391-ee4c4d5a-68bb-4f15-b9e2-12da0894434d?action=collection%2Ffork&collection-url=entityId%3D23524391-ee4c4d5a-68bb-4f15-b9e2-12da0894434d%26entityType%3Dcollection%26workspaceId%3Dbfaf19bf-cb6b-4016-93b7-65e73bb056db#?env%5BUpdates%20env%5D=W3sia2V5IjoidXJsIiwidmFsdWUiOiJodHRwczovL2FwaS5kcm9wYm94YXBpLmNvbS8yLyIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0In0seyJrZXkiOiJ1cGxvYWRVcmwiLCJ2YWx1ZSI6Imh0dHBzOi8vY29udGVudC5kcm9wYm94YXBpLmNvbS8yL2ZpbGVzL3VwbG9hZCIsImVuYWJsZWQiOnRydWUsInR5cGUiOiJkZWZhdWx0In0seyJrZXkiOiJmaWxlSWQiLCJ2YWx1ZSI6ImlkOmlTQmVrZHdrV3hvQUFBQUFBQUFCVmciLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiYW55In0seyJrZXkiOiJmaWxlTmFtZSIsInZhbHVlIjoiSW50cm8udHh0IiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImFueSJ9LHsia2V5IjoiZmlsZVBhdGgiLCJ2YWx1ZSI6Ii9Ib21ld29yay9JbnRyby50eHQiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiYW55In0seyJrZXkiOiJ0b2tlblVybCIsInZhbHVlIjoiaHR0cHM6Ly9hcGkuZHJvcGJveGFwaS5jb20vb2F1dGgyL3Rva2VuIiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImRlZmF1bHQifSx7ImtleSI6ImNsaWVudElkIiwidmFsdWUiOiJxd24ydHp6Z3J1aDFhbXQiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiZGVmYXVsdCJ9LHsia2V5IjoiY2xpZW50U2VjcmV0IiwidmFsdWUiOiJhZ2hlYTJlOGlyNmR0cHQiLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiZGVmYXVsdCJ9LHsia2V5IjoicmVmcmVzaFRva2VuIiwidmFsdWUiOiJlTHRzVWFZOFJQSUFBQUFBQUFBQUFhREJOY0diSU91WFlLR1A5SGhuNkhFN0dDRVNlOVNLRldzOE5JX1RvQ3VtIiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImRlZmF1bHQifSx7ImtleSI6ImFkZFVwbG9hZEJvZHkiLCJ2YWx1ZSI6IntcInBhdGhcIjpcIi9Ib21ld29yay9JbnRyby50eHRcIixcIm1vZGVcIjpcImFkZFwiLFwiYXV0b3JlbmFtZVwiOnRydWUsXCJtdXRlXCI6ZmFsc2UsXCJzdHJpY3RfY29uZmxpY3RcIjpmYWxzZX0iLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiYW55In0seyJrZXkiOiJhZGRNZXRhQm9keVRleHQiLCJ2YWx1ZSI6IntcImZpbGVcIjpcInt7ZmlsZUlkfX1cIixcImFjdGlvbnNcIjpbXX0iLCJlbmFibGVkIjp0cnVlLCJ0eXBlIjoiYW55In0seyJrZXkiOiJhZGREZWxldGVCb2R5VGV4dCIsInZhbHVlIjoie1wicGF0aFwiOlwie3tmaWxlUGF0aH19XCJ9IiwiZW5hYmxlZCI6dHJ1ZSwidHlwZSI6ImFueSJ9XQ==)