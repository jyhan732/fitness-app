# fitness-app

* npm run seed
* npm start

* git init
* git add .
* git commit -m "..."
* git branch -m master main
* git remote add origin git@github.com:jyhan732/fitness-app.git

# Create Github Repo

* Create a new repo "fitness-app" for the project

# GIT

* git pull
* git pull origin main --allow-unrelated-histories
* git push -u origin main

# Check GitHub Repo

* Refresh GitHub repo page to see the changes

# Modify server.js 

1. Remove the lines of code that requires the 'morgan' module and its setup:

    ```js
    const logger = require("morgan");
    app.use(logger("dev"));
    ```

2. Add or replace with the following lines:

    ```js
    const PORT = process.env.PORT || 3000;
    
    mongoose.connect(
    process.env.MONGODB_URI || 'mongodb://localhost/workout',
    {
        useNewUrlParser: true,
        useUnifiedTopology: true,
        useCreateIndex: true,
        useFindAndModify: false
    }
    );
    ```

# GIT

* git add .
* git commit -m "..."
* git push

# Heroku set up

1. Create New App
2. In the "Settings" tab, configure an env variable MONGODB_URI with its value copied from the MongoDB Atlas "Connect" tab
3. In the "Deploy" tab, choose and specify the GitHub repo for integration and deployment
4. Click on the "Deploy" button to deploy the app to heroku
5. Click on "View" to run the app
