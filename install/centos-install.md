# 1. Download the installer
```
wget -O jfrog-rpm-installer.tar.gz "https://releases.jfrog.io/artifactory/jfrog-prox/org/artifactory/pro/rpm/jfrog-platform-trial-prox/[RELEASE]/jfrog-platform-trial-prox-[RELEASE]-rpm.tar.gz"
```

# 2. Extract it
```
tar -xvzf jfrog-rpm-installer.tar.gz
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