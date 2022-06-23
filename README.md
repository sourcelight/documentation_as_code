# example-cirro-java-app

The application itself is designed to support https, despite of this it is configurable and you can change in the configuration files the port number and the protocol communication.


### Requirements
- Java 11
- Spring Boot
- Apache Maven 3.8.4
- Mysql 8.0.27
- Node 18.1.0
- React 17
- Angular 13

### Setup

```bash
git clone https://github.com/test-IO/example-cirro-java-react-app.git
```

The whole project contains 3 applications inside opportunity integrated each other:
- One kind of Connector (Spring Boot)

and 2 FE SPA applications

- React 
- Angular 

To create the relatives jars, simply run the following files for each case, they'll compile automatically the whole executable project respectively for React or Angular.
Note that all the following commands have to be run from root folder of the project

```bash
deploy_angular_prod.bat  # In case of Angular for prod Environment
deploy_angular_dev.bat  #  In case of Angular for dev Environment

deploy_react_prod.bat  #  In case of React for prod Environment
deploy_react_dev.bat  #  In case of React for dev Environment
```

To run a single jar:

```bash
java -jar  -Dprofile=dev  example-cirro-service-0.0.1-SNAPSHOT.jar

java -jar  -Dprofile=prod  example-cirro-service-0.0.1-SNAPSHOT.jar
```
Below is provided an utility to get the TOKEN to access manually the Cirro Platform with some client :

```bash
print_token_cirro.bat
```



