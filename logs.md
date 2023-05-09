### Saturday, May 6 (3 hrs)
* Reattempted ns-3.33 build on MacServer 
    * Missing boost library fialed build
    * Insufficient permissions to install with brew
    * Support pending
* Worked with first.cc on Linux server
    * Played around with various parameters observed changes in output
* Video for congestion control in TCP using ns3

### Monday, May 9 (2 hrs)
* Tried to run ns-allinone-3.33
    * Error: Missing boost library 
    * Tried to install with brew 
* Updating Home Brew
    * Neeed to update brew before installing new libraries
    * old OS was is no longer supported which made this more difficult 
```bash
    git -C /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core fetch --unshallow
    * /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

    sudo chown -R $(whoami) /usr/local/var/homebrew

    sudo chown -R $(whoami) /usr/local/lib/python3.7/site-packages /usr/local/share/zsh /usr/local/share/zsh/site-functions
    chmod u+w /usr/local/lib/python3.7/site-packages /usr/local/share/zsh /usr/local/share/zsh/site-functions

    sudo chown -R $(whoami) /usr/local/Cellar

    brew upgrade
```

*  Install boost library 
```bash
    brew install boost
```
### Monday, May 9 (1 hr)
* Unable to run ns3 with an old version of python (previously 2.7)
    * https://www.python.org/downloads/
* Created github reposiroty to log progress




