# Github SSH Setup Script

## This script helps you set up a new SSH key for your Github account, allowing you to use the git command line interface to push and pull repositories from your account.

### Prerequisites
* A Unix-based system with bash installed

* A Github account

* The `ssh-keygen` command installed on your system

### Running the script
* Make the script executable with `chmod +x github-ssh-setup.sh`

* Run the script with `./github-ssh-setup.sh`
* Follow the prompts in the terminal to complete the setup
### What the script does
1. Prompts you for the email you use for your Github account
2. Generates a new RSA key pair and saves it to `~/.ssh/id_rsa`
3. Adds the key to the SSH agent `with ssh-add`
4. Prompts you for a name for the key
5. Checks if the Github CLI (`gh`) is installed. If not, it prompts you to install it with `brew`.
6. Adds the public key to your Github account with the `gh ssh-key add` command.
### Tips
* If you already have an SSH key set up for your Github account and you want to use a new one, make sure to remove the old key from your account before running this script.

* If you don't want to install the Github CLI, you can manually add the public key to your account by going to your Github settings, selecting "SSH and GPG keys", and clicking "New SSH key".
