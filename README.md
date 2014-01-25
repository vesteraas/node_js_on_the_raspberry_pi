# Installing Node.js on your Raspberry Pi #
Using a web browser, find a pre-built version of Node.js at `http://nodejs.org/dist/`.  A valid distribution should end with **linux-arm-pi.tar.gz**.

Example:

`http://nodejs.org/dist/v0.10.9/node-v0.10.9-linux-arm-pi.tar.gz`

Log in to your Raspberry Pi:
	
	ssh pi@<RASPBERRY-PI-ADDRESS>

Download the Node.js distribution:

	wget http://nodejs.org/dist/v0.10.9/node-v0.10.9-linux-arm-pi.tar.gz
 
Expand the archive:

	tar xvfz node-v0.10.9-linux-arm-pi.tar.gz
	
Move the archive contents to the /opt directory:

	sudo mv node-v0.10.9-linux-arm-pi /opt
	
Create a symlink:

	sudo ln -s /opt/node-v0.10.9-linux-arm-pi /opt/node
	
Create symlinks for the node binaries and library:

	sudo ln -s /opt/node/bin/node /usr/bin/node
	sudo ln -s /opt/node/bin/npm /usr/bin/npm
	sudo ln -s /opt/node/lib/node /usr/lib/node
	
If you can't find such a file, create it.

Re-login to your Raspberry Pi, and test that everything works by typing:

    node --version
    
Switching between versions
--------------------------
Switching between different versions of Node.js is easy.  Just follow the instructions above, and update the symlink **/opt/node** accordingly:

	sudo rm /opt/node
	sudo ln -s /opt/node_vX.YY.Z-linux-arm-pi /opt/node

Donate
------
Did you find this little guide useful?  Consider donating a few satoshis to:

### 1GqWwzqwWAaQLobKutBK7e3dYLbxA8S6Hc ###
