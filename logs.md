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
### Monday, May 9 (1.5 hr)
* Unable to run ns3 with an old version of python (previously 2.7)
    * https://www.python.org/downloads/
* Created github reposiroty to log progress

### Wednesday, May 11 (2 hrs)
* installing sumo dependencies 
```
brew update
brew install gcc
brew install cmake
```

### Saturday, May 13 (3.5 hrs) 
* installing sumo dependencies 
```
brew install --cask xquartz
brew install xerces-c fox proj gdal gl2ps
brew install python swig eigen pygobject3 gtk+3 adwaita-icon-theme
python3 -m pip install texttest
pip3 install --upgrade pip

```
* installing sumo 
```
git clone --recursive https://github.com/eclipse/sumo
brew install xerces-c
export SUMO_HOME="$PWD/sumo"
cd $SUMO_HOME
mkdir build/cmake-build
cd build/cmake-build
cmake ../..
cmake --build . --parallel $(sysctl -n hw.ncpu)
```
* install swig
    * the cmake --build command encountered an error due to missing java.swig libraries
```
brew install swig
brew install eigen
brew install proj

cd /Users/cailab/Desktop/s_zarei/sumo
cmake -H. -Bbuild
cmake --build build --verbose
cd build
make

```
* VANET Simulation using ns3 and SUMO video
    * open browser osmWizard to generate map
```
cd sumo/tools
python3 osmWizard.py
```
    * Error with SSL certificate, try 'pip install -U certifi'

### Sunday, May 14 (1.5 hrs)
* James came to help with the installation of sumo
* brew install sumo was also unsuccessfull
* decided to proceed without sumo for now

### Friday, May 19 (1.5 hrs)
* understanding third.cc

### Thursday, May 25 (1.5 hrs)
* continuing with third.cc