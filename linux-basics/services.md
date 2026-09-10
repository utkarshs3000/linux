## [ RHEL Lab ]

// Services and Logs

&emsp;What I practiced:  
&emsp;Checking running services and viewing service logs in RHEL.

&emsp;Why I practiced it:  
&emsp;A security analyst needs to check service status and review logs during an investigation.

&emsp;Commands used:    
>systemctl list-units --type=service --state=running  
> systemctl status NetworkManager  
> journalctl -u NetworkManager

&emsp;Result:    
&emsp;I listed the running services, checked the NetworkManager status and reviewed its logs.

&emsp;What the result means:    
&emsp;I can check whether a service is running and view its recent activity from logs.

&emsp;Why this matters for a SOC analyst:    
&emsp;It helps when checking suspicious service activity, failures or unusual system behavior. 

<img width="1920" height="1080" alt="Screenshot 2026-08-30 115225" src="https://github.com/user-attachments/assets/1d02228a-5324-469a-bf54-bd32eb7dc2a6" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 115516" src="https://github.com/user-attachments/assets/9016d674-029b-4484-a607-d700d3d8b33e" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 115733" src="https://github.com/user-attachments/assets/74306678-0453-4560-ac46-2f185ad06e4c" />

