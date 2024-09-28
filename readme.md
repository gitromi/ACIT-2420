Creating a Remote Server on DigitalOcean with Arch Linux

Table of contents
1. Generate SSH keys
2. Add SSH Key to DigitalOcean
3. Add a Custom Arch Linux Image
4. Create a Droplet Running Arch Linux
5. Using cloud-init for Automation
6. Connect to Your Droplet Using SSH

1. Generate an SSH Key

What are SSH keys?
SSH Keys are a secure authentication method for accessing remote systems. They consist of a public key store on the server, and a private key kept on your local machine. This eliminates the need for a password, providing a more secure way of logging in.

Steps to create an SSH key pair
On windows, you may have to create a .ssh directory in your home directory first.

~ = your home directory.


    1. Open your terminal and run the following commmand: 
    ssh-keygen -t ed25519 -f ~/.ssh/do-key -C "your email address"

In powershell, Tilde does not always work. You may have to enter the full path. Replace "your-user-name" with your Windows user name, and "youremail@email.com" with your email account.

```ssh-keygen -t ed25519 -f C:\Users\your-user-name\.ssh\do-key -C "youremail@email.com"```


    2. After running that command, you will recieve a prompt to enter a passphrase. You can leave this blank. If you do decide to create a passphrase, make sure to remember it/have it written down somewhere safe.

    3. You will recieve the key fingerprint. Select and copy your key fingerprint.

2. Add your SSH Key to DigitalOcean
    Why add SSH keys to DigitalOcean?
    Adding your SSH key to DigitalOcean will allow you to securely access any droplet you create, without the need to enter a password.

    1. Log in to digital ocean
    2. Navigate to Settings on the side bar
    3. Click Settings>Security>Add SSH Key
    4. Paste the previously copied randomart image into the SSH Key content
    5. Create a name for your SSH Key, click "Add SSH Key"
