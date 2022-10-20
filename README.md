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

# Run OCI Image
docker compose up -d

# (Optional) Recreate Run OCI Image
docker compose up --build --force-recreate -d
```
## Access Sonarqube
Wait 1-2 minutes, until Sonarqube ready to use!
<your_ip>:9000 

![Alt text](sonar.jpg?raw=true "Sonarqube Up & Running")
![Alt text](login-sonar.jpg?raw=true "Sonarqube Login")
![Alt text](plugin.jpg?raw=true "Sonarqube Plugin Installed")

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

## Ref
https://github.com/mc1arke/sonarqube-community-branch-plugin