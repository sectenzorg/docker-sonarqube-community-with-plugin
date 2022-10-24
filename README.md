# Docker Sonarqube Community with Plugin

## Installation

Install Docker 
```bash
git clone https://github.com/sectenzorg/docker-portainer
sudo apt install make git
sudo make install-docker
```
## Install Docker Compose
https://docs.docker.com/compose/install/

## Usage

```bash
git clone https://github.com/sectenzorg/docker-sonarqube-community-with-plugin

# Build OCI Image
docker build -f release.Dockerfile . --build-arg SONARQUBE_VERSION=9.6.1-community --build-arg PLUGIN_VERSION=1.12.0 --tag sonarqube-with-community-branch-plugin:9.6.1-community

# Before run installation
You can set them dynamically for the current session by running the following commands as root:

sysctl -w vm.max_map_count=524288
sysctl -w fs.file-max=131072
ulimit -n 131072
ulimit -u 8192

# Run OCI Image
docker compose up -d

# (Optional) Recreate Run OCI Image
docker compose up --build --force-recreate -d
```
## Access Sonarqube
```bash
Wait 1-2 minutes, until Sonarqube ready to use!

<your_ip>:9000
```
## Ref
https://github.com/mc1arke/sonarqube-community-branch-plugin