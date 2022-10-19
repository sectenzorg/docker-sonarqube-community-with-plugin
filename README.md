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
docker build -f release.Dockerfile . --build-arg SONARQUBE_VERSION=9.6.1-community --build-arg PLUGIN_VERSION=1.12.0 --tag 
sonarqube-with-community-branch-plugin:9.6.1-community

docker compose up -d
```

![Alt text](sonar.jpg?raw=true "Sonarqube")

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)