# SSHLogin

## Steps

Use pwn module to interact with SSH servers. Paramiko used for error handling.

Opening passwords file -> iterating over each password, cleaing the password, uses the pwn module to make a SSH connection using that password, checking if the response is valid. If the response is correct we stop checking passwords.

<img width="1008" height="644" alt="image" src="https://github.com/user-attachments/assets/880b36df-ff48-4915-810f-f97f22a15e1d" />
