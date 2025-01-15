Windows Version: [[How to setup Robotpy and Driver Station on Windows (Not complete)]]
## You should only need to follow this guide if you have already tried the robotpy-installer repository in the github

Here is the link to the github: (https://github.com/AltaHighRobotics/RobotpyInstallers)
Since you are on a linux machine, you will run the linux-robotpy-installer.sh
## If those installers did not work, this guide should help you

### Install Robotpy

Make sure your python is Python3.12, you can check by running:
```bash
python3 -V
```
You should see `Python3.12
If you do NOT HAVE PYTHON 3.12 you need to fix that, to install it, run:
```bash
sudo apt install python3.12
```
Go to your terminal and enter:
````bash
pip config set global.break-system-packages true
# Making sure it is the right version
python3 -m pip install robotpy==2024.3.2.2
# Will download the normal dependacies that you will need
python3 -m pip install robotpy['commands2', 'phoneix5']
pip config set global.break-system-packages false
````

This will prevent your system from flagging robotpy as a global enviornment package so that you can properly install it, you may also need to set break-system-packages for syncing your robotpy packages (we'll include it dw bbg <3 :3)

### There we go!
You now have robotpy and its dependacies installed, if your project requires extra dependancies, you can install them with:

python3 -m pip install robotpy[<PACKAGE_NAME>]`


### Install Driver Station (annoying)
If you would like to install a working linux version of FRC driver station as well (which should already be in the windows machines), you may be out of luck unless you are on arch linux apparently (I have ubuntu, my friend has arch but only his worked)
#### This is a rust version of driver station so it will install rust for you

To install, go to [this link](https://github.com/Redrield/Conductor) and follow it's instructions, unless if you just wanna run this code:

# Installs nodejs and libraries needed for Conductor DS`
````bash
sudo apt-get install -y nodejs libudev-dev libx11-dev libxi-dev libpango1.0-dev libatk1.0-dev libsoup2.4-dev libgtk-3-dev libwebkit2gtk-4.0-dev

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
export NVM_DIR="$HOME/.nvm"
# This loads nvm
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
# This loads nvm bash_completion
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
nvm install 14
nvm use 14

# Install Rust`
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"
cargo install cargo-bundle

# Downloads Conductor driver station`
git clone https://github.com/Redrield/Conductor
make setup && make release
````

#type/Robotics