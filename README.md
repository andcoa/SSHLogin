# SSH Login Brute Force

## Objective  
Simulate a brute-force attack using a custom Python script to enumerate SSH credentials. Use the pwn module to interact with SSH servers and Paramiko for error handling. Open the passwords file and iterate over each password, clean the password, use the pwn module to make a SSH connection using that password and check if the response is valid. If the response is correct, the script stops checking passwords.

## Skills Learned  
- **Python Scripting**: Developed a custom brute-force script using `pwntools` and `paramiko` libraries to automate SSH login attempts.  
- **Password List Enumeration**: Leveraged a wordlist to simulate common password guessing tactics.  
- **Error Handling & Connection Logic**: Handled authentication exceptions gracefully while managing network session logic.  
- **Red Team Tactics Awareness**: Gained hands-on experience with offensive techniques used by threat actors.  
- **Detection Engineering Insight**: Used the script to generate authentic brute-force telemetry for SIEM testing and alert tuning.

## Tools Used  
- **Python**  
- **pwntools**  
- **paramiko**  
- **Kali Linux / Ubuntu (Attacker Host)**  
- **OpenSSH Server (Target)**  
- **Custom Password List**

## Steps

1. **Set Up SSH Environment**  
   - Configured a Linux VM with OpenSSH enabled to act as the target server.  
   - Created a non-root user (`notroot`) with a known weak password for simulation.

2. **Create a Common Password Wordlist**  
   - Used `rockyou.txt` as the base and extracted the top common passwords into `ssh-common-passwords.txt`.

3. **Built the Brute-Force Script**  
   - Wrote a Python script using `pwntools` and `paramiko` to automate SSH login attempts.  
   - Implemented logic to iterate through each password, attempt authentication, and detect success or failure.

<img width="1005" height="651" alt="image" src="https://github.com/user-attachments/assets/b6a2189d-33b9-4100-8517-0c14bb65c63a" />

Result:

<img width="632" height="728" alt="image" src="https://github.com/user-attachments/assets/74a1017f-a42f-4c86-9bb0-38350ff4c1dc" />

