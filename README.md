## Laravel Configurations Steps to Delpoy app on Heroku platform  
### Steps for configure Laravel project after matching the app from the github repository
- add Procfile file
  - add in procfile file this line  
    ` web: vendor/bin/heroku-php-apache2 public/ `
- get logged-in
- add the configuration as pair with the app name in the Heroku by **--app app_name** command.
- or can edit the configuration from the dashboard in the heroku "on the Browser".
```
heroku login
heroku config:add --app app_name  APP_NAME="Mobidal Formations"
```
- add an add-on for postgreSQL from browser
  - go to resources and find postgres Add-ons field 
- run this command for get the configuration of the postgres DB
```
heroku pg:credentials:url --app app_name
```
- modify the config with the new configurations 

```
heroku config:add --app app_name  DB_CONNECTION=pgsql
heroku config:add --app app_name  DB_HOST=host
heroku config:add --app app_name  DB_PORT=port
heroku config:add --app app_name  DB_DATABASE=dbname
heroku config:add --app app_name  DB_USERNAME=user
heroku config:add --app app_name  DB_PASSWORD=password
```
- run commands from the CLI using bash or  direct commands 

```
heroku run bash --app app_name
```
OR Run direct the command like this:
```
heroku run php artisan migrate
```
### Changing the Application

- Now the APP is runnig Live in the Herroku Platform, you can change the app from the github and rematching the repository again
- or you can change in the app from the bash by
```
heroku run bash --app app_name
``` 



