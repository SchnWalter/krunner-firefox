Experimental 😄

### Required Dependencies

Debian/Ubuntu  
`sudo apt install cmake extra-cmake-modules build-essential libkf5runner-dev libkf5textwidgets-dev qtdeclarative5-dev gettext`

openSUSE  
`sudo zypper install cmake extra-cmake-modules libQt5Widgets5 libQt5Core5 libqt5-qtlocation-devel ki18n-devel ktextwidgets-devel kservice-devel krunner-devel gettext-tools`  

Fedora  
`sudo dnf install cmake extra-cmake-modules kf5-ki18n-devel kf5-kservice-devel kf5-krunner-devel kf5-ktextwidgets-devel gettext`  

### Build instructions

```
cp /usr/share/applications/firefox.desktop ~/.local/share/applications/firefox.desktop
git clone https://github.com/alex1701c/FirefoxProfileRunner
cd FirefoxProfileRunner
mkdir build
cd build
cmake -DQT_PLUGIN_INSTALL_DIR=`kf5-config --qt-plugins` ..
make
sudo make install
```


Restart krunner to load the runner (in a terminal type: kquitapp5 krunner;kstart5 krunner )

After this you should see your runner in the system settings:

systemsettings5 (Head to "Search")

You can also launch KRunner via Alt-F2 and you will find your runner.
