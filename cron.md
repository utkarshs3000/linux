## [ RHEL Lab ]

// Cron Jobs and Scheduled Tasks

 &emsp;What I practiced:  
 &emsp;Checking the cron service and creating a scheduled task in RHEL.

 &emsp;Why I practiced it:  
 &emsp;Scheduled tasks can be used for normal automation or persistence by an attacker.

 &emsp;Commands used:    
 >systemctl status crond  
 >crontab -l  
 >crontab -e  
 >cat cron-demo.log  

 &emsp;Result:  
 &emsp;I checked that cron was running, created a cron job and confirmed it executed by checking the log file.

 &emsp;What the result means:  
 &emsp;I can check cron jobs and verify when a scheduled command runs.

 &emsp;Why this matters for a SOC analyst:  
 &emsp;It helps when investigating suspicious scheduled tasks or persistence on a Linux system.

<img width="1920" height="1080" alt="Screenshot 2026-08-30 174326" src="https://github.com/user-attachments/assets/d737b753-e9f1-461d-9d1f-1c7e3d776182" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 174912" src="https://github.com/user-attachments/assets/186a8173-12b9-4251-8470-d81895046630" />
