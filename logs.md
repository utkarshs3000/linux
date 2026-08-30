## [ RHEL Lab ]

// SSH and Authentication Logs

 &emsp;What I practiced:  
 &emsp;Checking SSH login activity and authentication logs in RHEL.

 &emsp;Why I practiced it:  
 &emsp;A security analyst needs to review successful and failed login attempts.

 &emsp;Commands used:        
 >sudo journalctl -u sshd --since "15 minutes ago"  
 >sudo ls -l /var/log/secure  
 >sudo tail -n 30 /var/log/secure

 &emsp;Result:  
 &emsp;I found successful SSH logins, failed password attempts and authentication failures in the logs.

 &emsp;What the result means:  
 &emsp;I can use system logs to check who tried to log in and whether the attempt succeeded or failed.

 &emsp;Why this matters for a SOC analyst:  
 &emsp;These logs can help detect suspicious logins, repeated password failures and unauthorized access attempts.

<img width="1920" height="1080" alt="Screenshot 2026-08-30 164939" src="https://github.com/user-attachments/assets/4f1a42fa-5267-4c4d-ae4d-38c41b2ac641" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 164530" src="https://github.com/user-attachments/assets/1b0532ee-0233-493c-890d-077b62626761" />
