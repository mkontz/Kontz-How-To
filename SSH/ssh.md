# Setting Up SSH

[SSH directions](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) on github

## Linux Setup

### Generate key

* `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
	* enter a file name or press enter to accept default
	* enter passphrase (twice)
### Set permissions
This applies to new or existing private and public keys in .ssh folder

 * Home directory: `cd ~`
	* `sudo chmod 700 .ssh`
* .ssh directory: `cd .ssh/`
	* `sudo chmod 644 id_rsa.pub`
	* `sudo chmod 600 id_rsa`
	
### Add key to ssh-agent

	* `eval "$(ssh-agent -s)"`
	* `ssh-add ~/.ssh/id_rsa`
 
### Github
* login into github
* go to setting -> SSH and GPG keys
* Select New SSH key
* Follow direction to upload new or existing public key

### Test
 * Set remote to point to ssh github repo path (as opposed to https)
 * fetch and push repo to verify proper setup
 	* Enter passphrase first time for ssh agent

## Windows
### Install PuTTYgen
[www.puttygen.com/](https://www.puttygen.com/)

* Install PuTTYgen (if not already installed)
	* Reboot Windows
* Open PuTTYgen
	* load id_rsa generated from Ubuntu
	* Enter Passphrase
	* Save as .ppk file
* open repo in Git Extension
* go to Repository -> Remote repositories
	* Replace https URL with SSH URL
	* browse to .ppk file
	* Load SSH key
* open a terminal and try to push and fetch, it should prompt for passphrase
* Push from Git Extensions