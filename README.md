# Step to deploy a MERN (MongoDB, Express.js, React.js, Node.js) Application to Heroku

## Repository Structure Setup

```
your-app
│   README.md   
│   index.js   
│   package-lock.json   
│   package.json   
│   node_modules   
│   .gitignore   
│
└───app - Node.js Application repository
|      │
|      └───controller
|      │
|      └───middleware
|      │
|      └───model
│
└───client - Should contain your whole React.js App
│
└───config - Database and other configuration files
│
└───tests - Optional repository for writing test cases
```

## Contents of .gitignore (In the root repository)

Copy the following content into the .gitignore file in the root directory. If you cannot find one, create a new .gitignore file in the root directory and then copy.

```
# Logs
logs
*.log
npm-debug.log*

# Runtime data
pids
*.pid
*.seed

# Directory for instrumented libs generated by jscoverage/JSCover
lib-cov

# Coverage directory used by tools like istanbul
coverage

# Grunt intermediate storage (http://gruntjs.com/creating-plugins#storing-task-files)
.grunt

# node-waf configuration
.lock-wscript

# Compiled binary addons (http://nodejs.org/api/addons.html)
build/Release

# Dependency directory
# https://docs.npmjs.com/misc/faq#should-i-check-my-node-modules-folder-into-git
node_modules

```

## Removing .git from React App (client) repository

1. Navigate to ```client``` repository by running the command ```cd client```
2. Run the command ```sudo rm -rf .git``` (Notice the dot before git as it is important)
3. Run the command ```ls -a``` and make sure that the ```.git``` repository (hidden) is deleted inside the ```/client``` repository
4. Navigate back to the root repository

## Heroku Setup

1. First create a Heroku Account
2. Read Heroku's documentation thoroughly. Check it out [here](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up)
3. Setup Heroku CLI as instructed in the above link
