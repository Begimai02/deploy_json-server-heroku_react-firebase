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

1. Navigate to Deploy tap and create a pipeline, Connect your GitHub with the fake-server repo.
<img width="1440" alt="Снимок экрана 2022-04-14 в 19 27 13" src="https://user-images.githubusercontent.com/76545834/163400675-ab0b29c7-ebae-40a5-b74c-26a18b5c521d.png">

2. Connect with github
<img width="1440" alt="Снимок экрана 2022-04-14 в 19 30 06" src="https://user-images.githubusercontent.com/76545834/163401182-a03eb0e2-4f4b-4a9d-90fe-d8dc34161d3b.png">

3. Configure auto-deploy and choose the branch of the Pipeline
<img width="1440" alt="Снимок экрана 2022-04-14 в 19 28 01" src="https://user-images.githubusercontent.com/76545834/163400830-923ee684-4c82-469b-bcbe-84b2a0e28ea7.png">


Now whenever you push the changes to the selected branch, the database will be updated and can be accessed via the same base API.

