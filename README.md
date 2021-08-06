# Redmine GTT Deployment Files

**WAR File** containing Redmine-GTT and a **PostgreSQL dumpfile** containg a Sample Redmine Configuration for fast deployment to Tomcat.

## Prequisites

1. Working Tomcat Application Server
2. Working PostgreSQL Database with PostGIS

## Installation

* clone this repository
* create a `redmine` PostgreSQL database 

```shell
createdb redmine
```

* import the sample Redmine database

```shell
pg_restore -d redmine redmine.dmp
```

* copy the redmine.war into <Tomcat Dir>/webapps directory. Tomcat will automatically deploy this file. 

* wait for a minute or so in order for Tomcat to deploy completely. The Redmine application can be accessed afterwards using this url: 
  
```
http://localhost:8080/redmine
```
  
* pre-configured login users are: 
  
  
```
  username: admin password: georepublic
  username: user  password: georepublic
```
  

