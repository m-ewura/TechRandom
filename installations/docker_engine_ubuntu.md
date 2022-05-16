#### Install Docker on Ubuntu Server

If you have any of these ubuntu versions, you can proceed:
* Ubuntu Jammy 22.04
* Ubuntu Impish 21.10
* Ubuntu Focal 20.04
* Ubuntu Bionic 18.04

First check for old docker versions and uninstall by running in cli
<br> `$ sudo apt-get remove docker docker-engine docker.io containerd runc`

* Install using repository for ease of installation and upgrade tasks.
> * Set up repository <br> run `$ sudo apt update` <br> `$ sudo apt-get install \ ca-certificates \ curl \ gnupg \ lsb-release`
> * Add Docker’s official GPG key: <br> `$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`
> * Set up stable repository with: <br> `echo \"deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
> * Install Docker Engine: <br> `$ sudo apt-get update` <br> `$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin`
> <br> The above code auto installs the latest version but to install a specific version, list the versions available by running:<br> `$ apt-cache madison docker-ce` <br> After, run this `sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io docker-compose-plugin` , where VERSION_STRING is what comes after `docker-ce |` and before `| https...` in the list of versions available.
> * To verify `Docker Engine` is installed: <br> run `$ sudo docker run hello-world`
> <br> If you get an error: <br> _Cannot connect to the Docker daemon at unix:/var/run/docker.sock. Is the docker daemon running?_
> <br> __Check status by running:__ <br> `sudo systemctl status docker`
> <br> If you get an error: <br> _System has not been booted with systemd as init system (PID 1). Can't operate.
>Failed to connect to bus: Host is down_
> <br> __Run this cmd if using Ubuntu 20.4 & Docker 20.10.11:__ <br> `$ sudo service docker start` to start Docker <br> run `sudo docker run hello-world` again and response should contain <br> `... Hello from Docker! This message shows that your installation appears to be working correctly ...`

* To uninstall Docker,
> * Uninstall the Docker Engine, CLI, Containerd, and Docker Compose packages:
><br> `$ sudo apt-get purge docker-ce docker-ce-cli containerd.io docker-compose-plugin`
> * To delete images, containers, volumes, or customized configuration files on your host that are not automatically deleted after running that, run <br>
> `$ sudo rm -rf /var/lib/docker`
> <br> `$ sudo rm -rf /var/lib/containerd`

* To run Docker without root privileges,
> run `$ sudo groupadd docker`
> <br> run `$ sudo usermod-aG docker $USER` where $USER is your ubuntu username.
