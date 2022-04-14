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
<img width="800" alt="Снимок экрана 2022-04-14 в 19 27 13" src="https://user-images.githubusercontent.com/76545834/163400675-ab0b29c7-ebae-40a5-b74c-26a18b5c521d.png">

2. Connect with github
<img width="800" alt="Снимок экрана 2022-04-14 в 19 30 06" src="https://user-images.githubusercontent.com/76545834/163401182-a03eb0e2-4f4b-4a9d-90fe-d8dc34161d3b.png">

3. Configure auto-deploy and choose the branch of the Pipeline
<img width="800" alt="Снимок экрана 2022-04-14 в 19 28 01" src="https://user-images.githubusercontent.com/76545834/163400830-923ee684-4c82-469b-bcbe-84b2a0e28ea7.png">


Now whenever you push the changes to the selected branch, the database will be updated and can be accessed via the same base API.


---


## How to deploy your front on firebase?
1. Install firebase tools ```npm install -g firebase-tools```
2. Create build folder for deploying ```npm run build```
3. Enter into your firebase account```firebase login```
4. Setup a firebase context for the current application ```firebase init```
5. Press space to select the features, than enter to confirm your choice.
 
  Select first ```Hoisting```

<img width="889" alt="Снимок экрана 2021-11-30 в 16 08 27" src="https://user-images.githubusercontent.com/76545834/163412479-901f51e6-b77a-4337-a2b7-dc180dc14cd1.png">
 
6. Go to the firebase console. And create new project or use an existing project (where you made an auth)
<img width="889" alt="Снимок экрана 2021-11-30 в 16 08 27" src="https://user-images.githubusercontent.com/76545834/163412905-094d4797-5786-4970-b754-5e798c3bd70a.png">

7. Select your project and press enter key.
8. Type `build` folder. Build is a compiled version of a program.

9. Configure as a single app --> `yes`.

10. Set up automatic builds and deploys with GitHub --> `no`.

11. File build/index.html already exists. Overwrite? --> `no`.

12. The last part `firebase deploy`.

<img width="671" alt="Снимок экрана 2022-04-14 в 21 07 16" src="https://user-images.githubusercontent.com/76545834/163419338-a268b0ba-1f45-4b54-a657-189e36d89397.png">



