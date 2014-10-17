#Windows

Windows is clearly the best platform for developers.  Ok, we just said that to make you feel better.  Prepare for some mocking from your Mac & Linux counterparts, but while they're spending hours typing obscure commands in their terminal you can gloat at how you can run programs that actually make life easier.  That being said, a lot of developers do use Windows as their development environment.  There's a reason Windows is installed on more computers than anything else.

If you want the full "command line" experiance, you can always install Ubuntu on a Virtual Machine.

https://www.virtualbox.org/

## Setup Git Bash

Go to [Git Bash](http://git-scm.com/download/win) and follow the setup instructions there. This will add additions to your command prompt in Windows.

## Setup Python

Get the 32bit installer here: https://www.python.org/ftp/python/2.7.6/python-2.7.6.msi

Even if you are running 64bit Windwows, install the 32bit version of Python.

Install Python to it's default location. (C:\Python27)

### Add the Python 2.7 Directory to your System Path Environment Variable

In order to make it so you can access Python via any command line prompt (and not just the Python-specific one), you’ll need to add the newly-installed Python 2.7 directory to your “Path” system environment variable. This makes it easier to access Python and run scripts in whatever shell you’re using to using (Command Prompt, PowerShell, and my personal favorite: Git Bash.)

So, go to Control Panel –> System Properties –> Environment Variables and select the PATH variable from the list below:

![](https://raw.githubusercontent.com/hackbrightacademy/computer-setup/master/images/image44.png)

Click Edit

![](https://raw.githubusercontent.com/hackbrightacademy/computer-setup/master/images/image45.png)

And append the Python path to the end of the string – the default path will be something like C:\Python27.
Also make sure you include the C:\Python27\Scripts in the Path too even if it doesn’t exist yet – this is where your package management tools, unit testing tools, and other command line-accessible Python programs will live.
With that in place, you can now start the Python interpreter on any command prompt by invoking the python command. Let’s get our package manager set up for Python.

### Install pip to Manage Your Python Packages
There’s a couple of different options for package management in Python – pip is the one that doesn’t suck.

Pip makes it trivial for us to install Python packages, like Requests. And we’re going to have to install packages pretty often if we’re working with third party tools and libraries, so this is a must-have.

[Pip has a detailed set of instructions on how to install it from source](https://pip.pypa.io/en/latest/installing.html) – if you don’t have the curl command on your system, just use your Git or even your web browser to download the source file mentioned in their instructions.

### Sublime Text 2
Sublime Text is a very popular editor for developers and what we us on our pair programming workstations.  Download a copy from:

http://www.sublimetext.com/

Sublime is very cusomizable (which is probably one of the reasons it is so popular).  Every developer is different, so customize to your own style, but here are some recommendataions:

####Format for Python
Press Command-, (comma) to open the Preferences.sublime-settings file.  Add the following lines:

````
{
  "tab_size": 4,
  "translate_tabs_to_spaces": false
}
````

####Package Control
Sublime has its own package manager that makes it easy to install additioanl sublime plugins.  Follow the instructions at the link below to install it:

https://sublime.wbond.net/installation

####pylint
The pair programming workstations at Hackbright have the pylint plugin installed.  That's what generates those little red and yellow icons showing you where potential syntax errors in your code may be before you run it.  Use the Package Manager you installed above to install the pyline plugin.

####SublimeLinter
There is a more general linter that handles more than Python called SublimeLinter. The link to install it for Sublime Text 2 is https://sublime.wbond.net/installation#st2
