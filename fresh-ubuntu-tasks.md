
## Basic Stuff
<!-- Update repositories and upgrade old stuff -->
sudo apt update && upgrade
<!-- Install Google Chrome -->
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - 
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt update
sudo apt install google-chrome-stable
<!-- Install git if not installed -->
sudo apt install git
<!-- Generate SSH Key & Add key to ssh agent -->
ssh-keygen -t rsa -b 4096 -C "andre@stratioautomotive.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
<!-- Install Spotify -->
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886
echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt update
sudo apt install spotify-client
<!-- Install Slack https://slack.com/downloads/linux -->
<!-- Install Vim -->
sudo apt install vim
<!-- Install ULauncher http://ulauncher.io/ -->
<!-- Install ZSH -->
sudo apt install zsh
<!-- Make ZSH default shell -->
chsh -s /bin/zsh
<!-- ZSH Configuration Framework -->
git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"
<!-- RUN Config -->
setopt EXTENDED_GLOB
for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done


## Python Stuff
<!-- Install PyCharm on /opt/pycharm https://www.jetbrains.com/pycharm/download/download-thanks.html?platform=linux&code=PCC -->
<!-- Install development tools/libs -->
sudo apt install build-essential libssl-dev libffi-dev python-dev
<!-- Install Pip -->
sudo apt install python3-pip


## NodeJS Stuff

