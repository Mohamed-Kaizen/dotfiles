# Zorin

??? note
    This is my personal preferences.

## Utils

```bash
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev curl software-properties-common cmake libgl1-mesa-dev libsdl2-dev libvulkan-dev apt-transport-https ca-certificates gnupg lsb-release gcc make tree git wget unzip
```

```bash
sudo ufw enable
```

### Installing Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```


## Development

### Docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker 
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

#### Images

```bash
docker pull getmeili/meilisearch
docker pull postgres:13-alpine
docker pull traefik
docker pull dgraph/dgraph:latest
docker pull dgraph/standalone
docker pull redis
docker pull plausible/analytics
docker pull minio/minio
docker pull yandex/clickhouse-server:21.6
docker pull python:3.9-slim-buster
docker pull python:3.8-slim-buster
docker pull node:14
docker pull node:16
```


### python

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.8
sudo apt install python3.9
brew install pipx
pipx completions
pipx install poetry
pipx install cookiecutter
poetry config virtualenvs.in-project true
poetry completions fish > ~/.config/fish/completions/poetry.fish
poetry completions bash > /etc/bash_completion.d/poetry.bash-completion
```

### nodejs

```bash
curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt install -y nodejs
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update && sudo apt install yarn
sudo yarn global add pnpm
sudo yarn global add @antfu/ni
sudo yarn global add vercel
```


## Applications

### software center

- vscode
- pycharm
- vlc
- brave
- keeweb
- telegram
- citra
- balenaetcher
- steam
- lutris
- stacer
- Kooha
- Blanket


### from sources

#### XDM

```bash
wget https://github.com/subhra74/xdm/releases/download/7.2.11/xdm-setup-7.2.11.tar.xz
tar -xvf xdm-setup-7.2.11.tar.xz
sudo ./install.sh
rm install.sh readme.txt xdm-setup-7.2.11.tar.xz
```


#### Ulauncher

```bash
wget https://github.com/Ulauncher/Ulauncher/releases/download/5.12.1/ulauncher_5.12.1_all.deb
```


#### TimeShift

```bash
sudo add-apt-repository -y ppa:teejee2008/timeshift
sudo apt-get update
sudo apt-get install timeshift
```

#### NeoFetch

```bash
sudo apt install neofetch
```

#### Fish and starship

```bash
sudo apt install fish
chsh -s /usr/bin/fish
mkdir -p ~/.config/fish
mkdir -p ~/.config/fish/completions
sh -c "$(curl -fsSL https://starship.rs/install.sh)"
echo 'eval "$(starship init bash)"' >> ~/.bashrc
echo "starship init fish | source" >> ~/.config/fish/config.fish
poetry completions fish > ~/.config/fish/completions/poetry.fish
```

