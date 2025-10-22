To install Trivy on Ubuntu, you can follow these steps to add the official Aqua Security repository and install via apt: Install necessary dependencies.

``` 
sudo apt-get install wget apt-transport-https gnupg lsb-release
```

# Add the Trivy GPG key.
```
    wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null
```
# Add the Trivy repository to your sources list:
```
    echo "deb [signed-by=/usr/share/keyrings/trivy.gpg] https://aquasecurity.github.io/trivy-repo/deb generic main" | sudo tee -a /etc/apt/sources.list.d/trivy.list
```
# Update your package lists.
```
    sudo apt-get update
```
# install trivy.
```
    sudo apt-get install trivy
```
After completing these steps, Trivy will be installed on your Ubuntu system. You can verify the installation by running trivy --version to check the installed version.
