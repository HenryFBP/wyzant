# Running

## Database setup

### DIY

Install and set up MySQL Server 8.

DIY MySQL setup is at your own peril. I won't detail how to do this.

Take note of the configuration under `./src/main/resources/hibernate.cfg.xml`

The password is `potato123` and the username is `root`, and the host is `jdbc:mysql://127.0.0.1:3306/`.

### Using docker-compose

Install [docker-compose](https://docs.docker.com/compose/install/).

`cd docker-database`

`sudo docker-compose up -d`

This brings up a database on `127.0.0.1:3306`.

#### Deleting docker database

`cd docker-database`

`sudo docker-compose stop; sudo docker-compose rm -f`

## Inserting test users and pets

Run `mvn install; mvn exec:java -Dexec.mainClass="com.example.main.TestUserInserter"`
at this project's root directory.

## Retrieving some users and pets

Run `mvn install; mvn exec:java -Dexec.mainClass="com.example.main.TestUserRetriever"`
at this project's root directory.
