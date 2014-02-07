# OSX

## Install

### XCode - mac App Store
- open xcode agree to terms of service

### command line tools
- mavericks: xcode-select —install.
- > mavericks (10.9) open Xcode menu bar > preferences > Downloads > install command line tools

### heroku client 
- https://toolbelt.heroku.com/

### postgres.app 
- http://postgresapp.com/

- add postgres.app to the path for compiling pg extensions (pyscopg adapter later)

open ~/.bashrc or ~/.zshrc and add the following 

````bash
# For Postgres.app

export PATH="/Applications/Postgres.app/Contents/MacOS/bin:$PATH"
````

### homebrew -http://brew.sh/

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
