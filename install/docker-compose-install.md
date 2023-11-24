# Requires Docker Compose on Linux

# 1. Download the installer
```
wget -O jfrog-compose-installer.tar.gz "https://releases.jfrog.io/artifactory/jfrog-prox/org/artifactory/pro/docker/jfrog-platform-trial-prox/7.71.5/jfrog-platform-trial-prox-7.71.5-compose.tar.gz"
```

# 2. Extract it
```
tar -xvzf jfrog-compose-installer.tar.gz
```

# 3. CD into directory
```
cd jfrog-platform-trial-pro*
```

# 4. Run the config script
```
sudo ./config.sh
```

# 5. Start RabbitMQ
```
sudo docker-compose -p trial-pro-rabbitmq -f docker-compose-rabbitmq.yaml up -d
```

# 6. Start JFrog Artifactory and Xray
```
sudo docker-compose -p trial-pro up -d
```