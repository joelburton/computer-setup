# OSX

The Mac is clearly the best plaform for developers.  It's based on Unix (BSD) (the version the Mac uses is called "Darwin").  If you get a job writing python code, there's a high likelyhood that your code (when release) will need to run on a unix server.  So why not run unix on your development environment?  With the Mac, you've got all the power of Unix under the hood, but you've got a user interface that's actually -- usable! (Unlike those Linux weenies).

## What Version are you on?
You can figure out what version of OSX you're on if you click on the apple icon in the top left corner and go to about this mac.


Supported versions
- 10.9: Mavericks
- 10.8: Mountain Lion
- 10.7: Lion 


## Install

### XCode
Xcode is the set of developer tools, provided by Apple, for the Mac.  We're not going to be developing in Xcode, but we do need to use some of the components that Xcode provides.  They're not installed by default.  If you're on a recent Mac, run the "App Store" app and you can install Xcode from there.

Whatever version of OSX you're on, after you install you'll need to launch XCode at least once to agree to the Terms of Service.


####Mavericks, Mountain Lion

- Download and install through the mac App Store
- open xcode agree to terms of service

If you're on mavericks, open the `terminal` and run `xcode-select —install`

For Mountain Lion, Open Xcode, open Xcode menu bar(top left) > Preferences > Downloads Tab > click install for command line tools.

XCode 5.1 broke some things that are particularly annoying. Add the following lines to your .bash_profile:

````bash
export CFLAGS=-Qunused-arguments
export CPPFLAGS=-Qunused-arguments
````

#### Lion

Update OSX to at least 10.7.4

Download an Xcode Version 4.6.3 from Apple's developer web site.  You'll need a Apple Developer Account to log in, but it's free:

https://developer.apple.com/downloads/index.action

- Download and install through the link above
- open xcode agree to terms of service
- Open Xcode, open Xcode menu bar(top left) > Preferences > Downloads Tab > click install for command line tools.



## Setup Python

OSX comes with Python (cool, huh?)  But there's a couple of things missing that will make our lives easier.

Run the following commands in your terminal window:

````bash
sudo easy_install pip
sudo pip install virtualenv python-twitter
````


###Sublime Text 2
Sublime Text is a very popular editor for developers and what we us on our pair programming workstations.  Download a copy from http://www.sublimetext.com/ and install it into Applications.

Sublime is very cusomizable (which is probably one of the reasons it is so popular).  Every developer is different, so customize to your own style, but here are some recommendataions:

####Format for Python
Press Command-, (comma) to open the Preferences.sublime-settings file.  Add the following lines:

````json
{
  "translate_tabs_to_spaces": false,
  "tab_size": 4,
  "rulers": [80]
}
````

`translate_tabs_to_spaces` will automatically convert tab characters to spaces.
`tab_size` will tell sublime that every tab should equal 4 spaces
`rulers` takes a list of integers at which to draw lines in sublime. This is helpful for conforming to pep8


####subl on the Command Line
To be able to type "subl" on the command line like we do on the pair programming workstations, create the following symbloic link from the Terminal:

````bash
sudo ln -s /Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl /usr/local/bin
````

####Package Control
Sublime has its own package manager that makes it easy to install additioanl sublime plugins.  Follow the instructions at the link below to install it (make sure you select Sublime 2):

https://sublime.wbond.net/installation#st2

#####SublimeLinter
The pair programming workstations at Hackbright have SublimeLinter already installed. That's what generates those little red and yellow icons showing you where potential syntax errors in your code may be before you run it.  Use the Package Manager you installed above to install the SublimeLinter plugin. 

####More
This is a good place to start if you'd like to customize Sublime further:

http://dbader.org/blog/setting-up-sublime-text-for-python-development


### homebrew 
- http://brew.sh/
- scroll to the bottom and find the ruby -e command. Run that to get

Once brew is installed, you can test it by installing spark
` brew install spark `


## Configuring SSH
### ssh-keygen

````bash
# Don't worry if you already have a ~/.ssh dir
mkdir ~/.ssh && cd ~/.ssh
````

Now let's generate a public / private key pair.  Run `ssh-keygen`. This will ask you several questions. I would recommend leaving the name of the file as id_rsa & setting a good passphrase.

Do the following once you've generated a key. 

` Login to github ` > ` Go to Settings (top right hand side)` > `Go to SSH keys`


From here you can create a new github key. Click `add key` and paste the line of text from `.ssh/id_rsa.pub` (unless you named it something else).

test it by running  `ssh git@github.com` (hit yes to confirm RSA sig)

you should see something like
````

Hi GITHUB NAME! You've successfully authenticated, but GitHub does not provide shell access.

Connection to github.com closed.
````


### Next Steps

You're good to go for everything you'll need during the fellowship. Once projects start, be sure to checkout osx-projects for additional help.
