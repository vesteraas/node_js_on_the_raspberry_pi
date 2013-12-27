# Installing Node.js on your Raspberry Pi #

Using a web browser, find a pre-built version of Node.js at `http://nodejs.org/dist/`.  A valid distribution should end with **linux-arm-pi.tar.gz**.

Example:

`http://nodejs.org/dist/v0.10.9/node-v0.10.9-linux-arm-pi.tar.gz`

On your Raspberry Pi, open a terminal window (Or connect to it via SSH)

Download the Node.js distribution:

    wget http://nodejs.org/dist/v0.10.9/node-v0.10.9-linux-arm-pi.tar.gz
 
Expand the archive:

	tar xvfz node-v0.10.9-linux-arm-pi.tar.gz
	
Move the archive contents to the /opt directory:

	sudo mv node-v0.10.9-linux-arm-pi /opt
	
Create a symlink:

	sudo ln -s /opt/node-v0.10.9-linux-arm-pi /opt/node
	
Append the following lines to the file .bash_profile in your home directory:

    #!/bin/bash
    NODE_HOME=/opt/node
    PATH=$PATH:$NODE_HOME/bin
    
Re-login to your Raspberry Pi, and test that everything works by typing:

    node --version
    
