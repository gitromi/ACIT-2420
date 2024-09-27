Creating a Remote Server on DigitalOcean with Arch Linux

1. Generate an SSH Key

What are SSH keys?
SSH Keys are a secure authentication method for accessing remote systems. They consist of a public key store on the server, and a private key kept on your local machine. This eliminates the need for a password, providing a more secure way of logging in.

Steps to Generate SSH keys
    1. Open your terminal and run the following command
    ssh-keygen -t rsa -b 4096
    2. When prompted, press enter to save they key in your default location.

2. Add your SSH Key to DigitalOcean
When you add your SSH key   