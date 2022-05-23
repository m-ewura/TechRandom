### Best Practices For Securing Container Images

> Containers allow for pkging and shipping apps in a std way. They make it easy to scale up/ tear down envs with variable workloads.

_What actions can one take to remediate vulnerabilities discovered in a container image ?_ <br>
   * _Prerequisites_:
     * _linux_
     * _docker_
     * _trivy_

#### 1. Scan Container Images

* Install Trivy
>If using Ubuntu, can follow these steps to install trivy: <br>
> `$ sudo apt-get install wget apt-transport-https gnupg lsb-release` <br>
> `$ wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | >sudo apt-key add -` <br>
> `$ echo deb https://aquasecurity.github.io/trivy-repo/deb $(lsb_release >-sc) main | sudo tee -a /etc/apt/sources.list.d/trivy.list` <br>
> `$ sudo apt-get update` <br>
> `$ sudo apt-get install trivy`

* Create/Make a dir either in the root dir and change to it.
    In the new dir, create a dockerfile following these steps:
    > `$ cat << 'EOF' > Dockerfile` <br>
    > `$ FROM debian:10.0` <br>
    > `$ RUN apt-get -y install bash` <br>
    > `$ ADD ./myfile.tar /tmp` <br>
    > `$ EXPOSE 22` <br>
    > `$ EOF`

* Make another dir archive with a text file
> `$ mkdir archive`<br>
> `$ echo this is some text > ./archive/file.txt` <br>
> `$ tar cvf myfile.tar archive`

* Build the dockerfile
> `$ docker build -t mytestimage:0.1 ./ -f Dockerfile`

* Start Docker
> `$ sudo service docker start`

* Scan with trivy
    Check to find images:
    > `$ docker images`

    Scan:
    > `$ trivy image mytestimage:0.1` where `mytestimage` is the repository and `0.1`  is the tag.

    Can also scan and create an output file:
    > `$ trivy i -f json -o mytestimage:0.1.json mytestimage:0.1`

