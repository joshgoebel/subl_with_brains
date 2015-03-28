# subl (with brains)

subl_with_brains is a wrapper for the subl command line tool that attempts to load projects (rather than folders) whenever it can.

## Example:

Lets say you have the project folder `/secret/source/skynet`:

    # you run
    $ subl /secret/source/skynet
    
    # this is what happens
    $ subl --project /secret/source/skynet/skynet.sublime-project

Behind the scenes `/secret/source/skynet` is searched for `skynet.sublime-project`.  If that file exists then it is opened as a project.  If it can't be found then the real `subl` is called as usual and will behave as it regularly would.

Any other arguments you pass in will simply be passed to the real `subl`.

## Why

I'm too spoiled by TextMate where this behavior is the default.


## Installation

    # ~/bin should be in your PATH
    mkdir ~/bin
    https://raw.githubusercontent.com/yyyc514/subl_with_brains/master/subl > \
    ~/bin/subl
    chmod +x ~/bin/subl
    subl -v
    # subl (with brains) 0.1
    # Sublime Text Build 3083

After installation you may need to tweak the SUBL variable to point to your installation of  Sublime Text if it's not at the default /Applications/ location.

## Contributions

Contributions are welcome, just submit a pull request on GitHub.


## FAQ

###  I have my project files all stored in a single directory...

It'd be easy enough to handle that edge case (I was just solving my own problem here), please submit a pull request.


### I'm on Windows, how do I use this?

**I don't know.**  Right now it surely won't work because the hard-coded path is a Mac path.  Pull requests to update this section are welcome if you're a Windows guy (or gal).  
