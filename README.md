## Swagger API Generation 

** In order to keep up to date, run swagger-codegen against latest Asterisk ** 

You can run the latest Asterisk version via Docker Compose using the provided docker-compose.yml file and the configs located under the asterisk folder. These configs set the default username and password to asterisk:asterisk for testing and updating specs for new versions.



```
bin/update-swagger
``` 
will generate a new API into `./SwaggerClient-php`. You will have to move this into the project root dir by hand and keep the existing composer.json file.

I renamed some APIs to enhance readability, this is not scripted you would have to do this by hand after update.


