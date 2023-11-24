# 1. Download the installer
```
wget -O jfrog-deb-installer.tar.gz "https://releases.jfrog.io/artifactory/jfrog-prox/org/artifactory/pro/deb/jfrog-platform-trial-prox/7.71.5/jfrog-platform-trial-prox-7.71.5-deb.tar.gz"
```

# 2. Extract it
```
tar -xvzf jfrog-deb-installer.tar.gz
```

# 3. CD into directory
```
cd jfrog-platform-trial-pro*
```

# 4. Run the installer
```
sudo ./install.sh
```

# 5. Start Artifactory
```
sudo systemctl start artifactory.service
```

# 6. Start Xray
```
sudo systemctl start xray.service
```

# Access the JFrog Platform
```
http://<hostname>:8082

For Example: http://localhost:8082 or http://192.168.86.243:8082
```