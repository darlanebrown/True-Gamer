# MERN Prototyping Starter

This is an example start project for [Kickstart Coding](http://kickstartcoding.com/)

**DO NOT** use this project in production. It exposes an API to MongoDB
without any sort of security. The only purpose of the API is to allow rapid
front-end prototyping.

## Usage


### Set-up

1. Get the code. You can either download this repo as a tar.gz or zip file,
then extract, or do a git pull and copy over the files into your project.

2. Set-up your MongoDB database. Either set-up an mLab database for testing
purposes with your team (easiest), or install and configure a local DB.

3. Create a ".env.local" file, that contains your credentials. This file WILL
NOT go into your git repo (because it is in .gitignore). It should be in the
following format:

```bash
export MONGODB_URI='mongodb://USERNAME:PASSWORD@something.com:1234/DB_NAME'
```

Where USERNAME and PASSWORD is replaced with an actual username and password on
the MongoDB. In the case of mLab, you will have to create a username and
password as a separate step.

4. NPM install backend:

```bash
npm install
```

5. NPM install frontend:

```bash
cd client
npm install
```


### Running

For local development, use the included "run.sh" Bash script:

```bash
bash run.sh
```

Look inside the script. Can you understand what it is doing?  It's main goal is
just to save you the steps of opening up two terminal windows or tabs. You can,
however, still do that method, it's up to you.


### Heroku

If you want to use your mLabs database on Heroku, you will need 

    heroku config:set MONGODB_URI='mongodb://someUser:...'


To ensure Heroku has the right configuration values set (which should occur
after you have done `heroku create` to make a new Heroku app, and added an
mLabs add-on to allow MonogoDB on Heroku), do a command like the following:

```bash
heroku config
```

You should see `MONGODB_URI` specified, something like:
    MONGODB_URI  mongodb://someUser:somePassword@something.com:1234/someDatabaseName 

Launching to Heroku is like any other app:

```bash
git push heroku master
```



