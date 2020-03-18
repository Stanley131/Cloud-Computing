### Prep to Install (Ubuntu)
1. Update a aptitude 

	``sudo apt-get update -y``

2. Install the additional packages 

	`` sudo apt-get install -y linux-image-generic-lts-trusty linux-headers-generic-lts-trusty``

3. Reboot system. 

	``sudo reboot``

4. Purge older version. 
	
	``sudo apt-get purge -y lxc-docker* && sudo apt-get -y purge docker.io*``

5. Update your packages. 

	``sudo apt-get update -y && sudo apt-get install -y apt-transport-https ca-certificates``

6. Get the new GPG key. 

	``sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D``

7. Add an entry for your OS:
	( A boot entry is a set of options that define a load
	 configuration for an operating system or bootable 
	 program.) 

	``deb https://apt.dockerproject.org/repo ubuntu-precise main``

	[Version](https://runnable.com/docker/install-docker-on-linux)

8. update again: ``sudo apt-get update -y``


9. Verify Aptitude pulls from the right repository. 

	``sudo apt-cache policy docker-engine``

### Install Docker 
1. Install linux package:

``update -y && sudo apt-get install -y linux-image-extra-$(uname -r)``

2. Install Docker:

	``sudo apt-get install docker-engine -y``

3. Start Docker: 

	``sudo service docker start``

4. Verify Docker: 

	``sudo docker run hello-world``

5. Docker group (optional): 
	- Run the following command to create a Docker group on Ubuntu:
		``sudo groupadd docker && sudo usermod -aG docker ubuntu``
	- log out and back in 
	- docker run hello-world