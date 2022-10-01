# Docker-install-on-ubuntu
How To Install dpkg on Ubuntu 20.04
#Uninstall old versions
sudo apt-get remove docker docker-engine docker.io containerd runc
#Installation methods
#Set up the repository
 sudo apt-get update
 sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
    Add Docker’s official GPG key:

$ sudo mkdir -p /etc/apt/keyrings
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
Use the following command to set up the repository:

$ echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb
  #Install Docker Engine
   $sudo apt-get update
 $sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
 #a. List the versions available in your repo:
$ apt-cache madison docker-ce
# b. Install a specific version using the version string from the second column, for example, 5:20.10.16~3-0~ubuntu-jammy.

 sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io docker-compose-plugin
Verify that Docker Engine is installed correctly by running the hello-world image.

 sudo service docker start
 sudo docker run hello-world
