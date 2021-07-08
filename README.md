# Cutefish DE Ubuntu

How to install Cutefish Desktop in Ubuntu? 

The goal is to create a better experience Linux desktop OS.

## Dependencies

```sh
sudo apt install -y git devscripts build-essential cmake ninja-build
```

```sh
sudo apt install -y qtbase5-dev qtquickcontrols2-5-dev libkf5networkmanagerqt-dev modemmanager-qt-dev debhelper extra-cmake-modules libkf5kio-dev libkf5screen-dev libqt5sensors5-dev qtdeclarative5-dev qttools5-dev qttools5-dev-tools libxcb-icccm4-dev qtbase5-private-dev kwin-dev libkdecorations2-dev libqt5xdg-dev libdbusmenu-qt5-dev libxcb-ewmh-dev libicu-dev libxcb-randr0-dev libsm-dev libxcb-xfixes0-dev libxcb-damage0-dev libxcb-composite0-dev libxcb-shm0-dev libxcb-util-dev libxcb-image0-dev libxtst-dev libpulse-dev libpolkit-qt5-1-dev libpolkit-agent-1-dev libqt5x11extras5-dev
```

## Build and install
```sh
mkdir -p ~/Downloads/cutefish
cd ~/Downloads/cutefish

git clone https://github.com/cutefishos/libcutefish.git
cd libcutefish
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/fishui
cd fishui
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/kwin-plugins
cd kwin-plugins
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/launcher
cd launcher
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/qt-plugins
cd qt-plugins
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/wallpapers
cd wallpapers
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
sudo apt-get install ./*.deb -y

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/dock
cd dock
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/filemanager
cd filemanager
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/terminal.git
cd terminal
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/settings
cd settings
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/statusbar
cd statusbar
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
git clone https://github.com/cutefishos/core
cd core
dpkg-buildpackage -uc -us -b

cd ~/Downloads/cutefish
sudo apt-get install ./*.deb -y

## no debian directory
# cd ~/Downloads/cutefish
# git clone https://github.com/cutefishos/calculator
# cd calculator

## no debian directory
# cd ~/Downloads/cutefish
# git clone https://github.com/cutefishos/icons
# cd icons
```

## License

This project has been licensed by GPLv3.
