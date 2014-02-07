# OSX

## Install

### XCode 
- Download and install through the mac App Store
- open xcode agree to terms of service

### command line tools
If you're on mavericks, open the `terminal` and run `xcode-select —install`


- > mavericks (10.9) open Xcode menu bar > preferences > Downloads > install command line tools
You can figure out what version of OSX you're on if you click on the apple icon in the top left corner and go to about this mac.
### heroku client 
- https://toolbelt.heroku.com/

### postgres.app 
- http://postgresapp.com/

- add postgres.app to the `$PATH` variable for compiling pg extensions (pyscopg adapter later)

Add the following to the bottom of `~/.bashrc` (or ~/.zshrc if you've installed it.)

````bash
# For Postgres.app

export PATH="/Applications/Postgres.app/Contents/MacOS/bin:$PATH"
````

### homebrew 
- http://brew.sh/
- scroll to the bottom and find the ruby -e command. Run that to get

## Configuring SSH
### ssh-keygen
` mkdir ~/.ssh && cd ~/.ssh`

`ssh-keygen`
This will ask you several questions. I would recommend leaving the name of the file as id_rsa & setting a password.


test it using 
ssh git@github.com (hit yes to confirm RSA sig)

you should see something like
````
PTY allocation request failed on channel 0

Hi GITHUB NAME! You've successfully authenticated, but GitHub does not provide shell access.

Connection to github.com closed.
````
