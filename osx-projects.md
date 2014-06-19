## OSX Project Time Setup


Howdy! Congrats on making it to projects! There are a couple more things that are worth setting up depending on what your project is.

So far this guide is focused on web apps and will help you install / get started on the following:

- postgres
- heroku 


###postgres.app 
PostgreSQL is a Database Server.  Using PostgreSQL is not required during the Hackbright Curriculum, however many student projects that use a database will take advantage of it (especially if you deploy on heroku).

- http://postgresapp.com/

- add postgres.app to the `$PATH` variable for compiling pg extensions (pyscopg adapter later) by adding the following to the bottom of `~/.profile` (or ~/.zshrc if you've installed it.)

````bash
# For Postgres.app

export PATH="/Applications/Postgres.app/Contents/Versions/9.3/bin:$PATH"
````


###Heroku Client 
If you don't already have an account go to http://heroku.com and sign up for one.

Once you have an account, download:
- https://toolbelt.heroku.com/

After installing, make sure to follow the heroku getting started step to login and create an ssh key.  

