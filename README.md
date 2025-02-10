![image](https://github.com/user-attachments/assets/cc27e70e-2426-4069-8358-ad855ee3094e)
Task: We have a MySQL relational database with a schema (country-city, language-by-country). 
And there is a frequent request from the city, which comes with a delay. 
We came up with a solution - to transfer all data that is frequently requested to Redis (in memory storage of key-value type).
And we don't need all the data, but a specific set of fields. The project will be in the format of a tutorial. That is, here we will raise the problem and immediately solve it.

So, let's start with what software we will need:

IDEA Ultimate (who has run out of keys - write to the group curator in Slack)
Workbench (or any other client for MySQL)
Docker
redis-insight is optional.

Our action plan:

Configure docker. There are specifics for each OS, so we advise you to search the Internet for an answer to a question like "how to install docker on windows"). Check that everything works.
Run the MySQL server as a docker container.
Expand the dump.
Create a project in IDEA, add maven dependencies.
Make a domain layer.
Write a method for obtaining all data from MySQL.
Write a data transformation method (in Redis we will write only those data that are frequently requested).
Run the Redis server as a docker container.
Write data to Redis.
Optional: install redis-insight, look at the data stored in Redis.
Write a method for getting data from Redis.
Write a method for obtaining data from MySQL.
Compare the speed of getting the same data from MySQL and Redis.
