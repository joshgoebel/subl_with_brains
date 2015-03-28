# subl (with brains)

## Summary

subl_with_brains is a modified subl executable that attemps to load projects instead of folders when you ask subl to open a folder.  

### Example:

Lets say you have the project folder `/secret/source/skynet`:

    # you run
    $ subl /secret/source/skynet
    
    # what really happens
    $ subl --project /secret/source/skynet.sublime-project

What actually happens is `skynet` is searched for `skynet.sublime-project` and if that file exists then it is opened as a project.  If a project file can't be found then the original `subl` is called as usual.  

Any arguments you pass should be passed thru to the real `subl` just any single directory argument will be remapped to `--project`.  `subl_with_brains` is just acting as a wrapper around the real executable.

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


## I have my project files all store in a single directory somwhere

It'd be easy enough to handle that edge case (I was just solving my own problem here), please submit a pull request.


## I'm on Windows, how do I use this?

**I don't know.**  Right now it surely won't work because the hard-coded path is a Mac path.  Pull requests to update this section are welcome if you're a Windows guy.  


## Contributions

Contributions are welcome, just submit a pull request on GitHub.

