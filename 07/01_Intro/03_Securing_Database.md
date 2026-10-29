### Secure with simple authentication
For a demonstration see https://youtu.be/1saxBK0ibIg?t=288

#### Steps

1. In Datagrip: Add admin-user i.e. in database mflix
```
use mflix
db.createUser(
   {
     user: "mflixAdmin1",
     pwd: "Hello1234",  // Or  passwordPrompt()
     roles: [ "readWrite", "dbAdmin" ]
   }
)
```
2. On the console: Enable authentication in the configuration.
For Window:
```
nano '/c/Program Files/MongoDB/Server/7.0/bin/mongod.cfg'
# add
security:
    authorization: enabled
```
... and start mongodb with the change. For Windows either
with WINDOWS+R and services.msc or with sc-Command
```
sc query MongoDB
sc stop MongoDB
sc start MongoDB
```

3. Connect without credentials -> mflix database should not be visible
4. Connect with credentials -> mflix database should be visible
5. Make a test query on the mflix database

Source:
* https://stackoverflow.com/questions/56110254/how-to-run-mongodb-as-a-service-with-authentication-on-a-windows-machine
* https://www.mongodb.com/docs/manual/reference/built-in-roles/#std-label-built-in-roles