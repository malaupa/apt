# Test Repo for testing [malaupa/composite-apt-repo-action](https://github.com/malaupa/composite-apt-repo-action)
To use repo in your environment use following commands to setup source list with related key:
```
wget -O- https://malaupa.github.io/repo-test/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/repo-test.gpg > /dev/null
echo 'deb [arch=amd64 signed-by=/usr/share/keyrings/repo-test.gpg] https://malaupa.github.io/repo-test/repo jammy main' | sudo tee /etc/apt/sources.list.d/repo-test.list
sudo apt update
sudo apt install corp-net-indicator
```