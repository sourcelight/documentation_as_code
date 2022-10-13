# DEPLOY JAVA REACT/ANGULAR ON DIGITAL OCEAN

## Overview

Both applications run each on differents droplets on DO as services, they are managed by the NGINX HTTP server that acts as Reverse Proxy.

The 2 active droplets on Digital Ocean(DO)are:

* **ubuntu-java-angular-cirro** where is running the Java-Angular application

* **ubuntu-java-react-cirro** where is running the Java-React application


## Running/stopping/configuring applications

 First update the jar file named **example-cirro-service-0.0.1-SNAPSHOT.jar** containing the whole deployable project inside the home directory **riccardo**
and then digit from the same path the following commands:

* to start the application: <pre> systemctl start springboot</pre>
* to stop the application: <pre> systemctl start springboot</pre>
* to check the application: <pre> systemctl status springboot</pre>

Each time you modify application's configuration it's necesary to stop and start the application.<br>You can find all **configuration's files** under the folder:
<pre>/opt/cirro/config/applications/cirro-java/</pre>

The specific path configuration is itself configurable modifying the pom.xml of "**example-cirro-service**" project for different deploy environments, below is reported a snippet:<br>

```
<properties>
<CIRRO_JAVA_CONFIGURATION>/opt/cirro/config/applications/cirro-java</CIRRO_JAVA_CONFIGURATION>
</properties>
```

The **files logs** generated are under the folder:
<pre>/opt/logs/</pre>
and are themself configurable through the file:
**logback-xxx.xml**


## DataBase

Both applications connect to the same database instance called "**db-java-cirro**"
Respectively on 2 different schemas:
* **db_angular** for the Java-Angular application
* **db_react** for the Java-React application

User Admin: xxxxxx

Pwd Admin : yyyyyy


## External Access
To access the database instance and the console from a local machine you need to 
* use a VPN as WireGuard  
* modify the firewall rules on the DO droplets. At the moment the access is designed in ssh with the private key on the local machine.

