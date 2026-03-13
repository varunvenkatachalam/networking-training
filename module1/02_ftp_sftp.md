# Hosting FTP and SFTP Server and Performing PUT and GET Operations

# FTP (File Transfer Protocol)

FTP is a standard network protocol used for transferring files between a client and a server over a network.

However, FTP is not secure because it transfers data in plain text.

# Installing FTP Server

To host an FTP server in Linux, we can use the **vsftpd** package.

Install the FTP server:

sudo apt update
sudo apt install vsftpd

Start the FTP service:

sudo systemctl start vsftpd

Enable it to start automatically during system boot:

sudo systemctl enable vsftpd

Check if the service is running:

sudo systemctl status vsftpd

# Connecting to FTP Server

To connect to the FTP server from a client system:

ftp <server_ip>

Example:

ftp 192.168.1.10

After connecting, the FTP server will ask for a username and password.

# PUT Operation (Upload File)

The PUT command is used to upload a file from the client machine to the FTP server.

Example:

put sample.txt

This command transfers the file **sample.txt** from the client system to the FTP server.

# GET Operation (Download File)

The GET command is used to download a file from the FTP server to the client machine.

Example:

get sample.txt

This command downloads the file **sample.txt** from the server to the client system.

# SFTP (Secure File Transfer Protocol)

SFTP is a secure version of FTP that works over the **SSH protocol**.  
Unlike FTP, it encrypts data during transfer.

# Connecting to SFTP Server

Since SFTP uses SSH, the SSH server must be running on the system.

To connect to the SFTP server:

sftp username@server_ip

Example:

sftp varun@192.168.1.10

After authentication, the user will enter the SFTP interactive shell.

# Upload File Using SFTP

To upload a file:

put sample.txt

This uploads the file to the remote system.

# Download File Using SFTP

To download a file:

get sample.txt

This downloads the file from the server to the local machine
