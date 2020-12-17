# Execute job on remote machine using SSH
install jenkins using docker and execute build process on remote machine

1) Create  a centos machine Machine using bridge adaptor
2) Install the centos minimal version latest image
3)Install ssh server on the new VM machine
4) Install docker
5) Install docker compose
6) CMD "sudo chmod +x /usr/local/bin/docker-compose"
7) install Jenkins image in docker
8) create jenkins_home folder "mkdir jenkins_home"
9) create the "centos7" folder and add the docker file from the centos7 library in this repository
10) create SSH keys in the centos 7 folder using "ssh-keygen -f remote-key"
11) run the docker-compose file using "dockercompose up -d"
