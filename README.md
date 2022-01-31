# Sets up linux machine with common tools

```bash
git clone https://github.com/fstaffa/machine-setup.git

sudo apt update &&
  sudo apt -y install python3-pip pipx python3-venv &&
  pipx install ansible --include-deps

sudo `which ansible-playbook` -i "localhost," -c local wsl-ubuntu.yml


# fish setup
curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher

chezmoi apply


# AWS install
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip && sudo ./aws/install
```

Running the changes in fish

```fish
sudo (which ansible-playbook) -i "localhost," -c local wsl-ubuntu.yml
```

# Manjaro

## Guix

``` fish
cd /tmp
wget https://git.savannah.gnu.org/cgit/guix.git/plain/etc/guix-install.sh
chmod +x guix-install.sh
./guix-install.sh
```

# Mac OS

```
brew tap homebrew/cask-fonts
brew install font-caskaydia-cove-nerd-font


```

# guix

``` fish
sudo apt-get install nscd
sudo apt-get install deamonize
sudo /etc/init.d/guix-daemon start
```

# syncthing

``` fish
systemctl --user start syncthing.service 
```
