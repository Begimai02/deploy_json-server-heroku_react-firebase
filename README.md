### fake_server_heroku_bg

## How to deploy your fake json-server on heroku?

### First part, prerequisite

1. Write on your terminal ```npm init -y```
2. Than install json server ```npm i json-server```
3. Create ```.gitignore``` file, and add one line in that file ```/node_modules```
4. Create ```server.js``` file to set up server (Add some boilerplate code in ```server.js```. It is always would be like this)
5. Create ```db.json``` file, and include your own data from ```db.json``` in react app.
6. Push everything into github new repo.

### Second part, heroku
1. Create heroku account,
2. Install heroku-cli. Examples here https://devcenter.heroku.com/articles/heroku-cli
And check ```heroku --version``` is it installed.
3. Next --> ```heroku login```. It will open a tab in the browser. Confirm login.
4. ```heroku create ...``` in place of dots write the name of the project.
(Name must start with a letter, end with a letter or digit and can only contain lowercase letters, digits, and dashes.)
5. Push your app to Heroku ``` git push heroku master ```
6. Open your created app ```heroku open```

### Creating a Pipeline
A pipeline is simply a connection between your GitHub repo and your Heroku Project.
So, Whenever you update your db.json for example and push your changes to a specific branch Heroku will be listening to this branch and build your app with the updated database.


