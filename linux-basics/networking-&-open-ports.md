## [ RHEL Lab ]

// Network and Process Investigation

 &emsp;What I practiced:  
 &emsp;Running a local web server, checking its open port and identifying the process behind it.

 &emsp;Why I practiced it:    
 &emsp;A security analyst may need to find which process is listening on a port and check its activity.

 &emsp;Commands used:        
 >python -m http.server  
 >ss -tlpn  
 >curl  
 >wget  
 >ps -fp  
 >readlink  
 >cat  
 >kill

 &emsp;Result:    
 &emsp;I started a web server on port 8080, confirmed it was listening, checked the process and logs, then stopped it.

 &emsp;What the result means:  
 &emsp;I can trace an open port back to its process and check what that process is doing.

 &emsp;Why this matters for a SOC analyst:  
 &emsp;It helps when investigating unknown services, open ports and suspicious processes.
 
<img width="1920" height="1080" alt="Screenshot 2026-08-30 170353" src="https://github.com/user-attachments/assets/8d47f8d2-6fe1-493c-8de6-dd50316b69dd" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 171453" src="https://github.com/user-attachments/assets/4677173e-f11f-4ee8-b49c-b71972d7d6d8" />
<img width="1920" height="1080" alt="Screenshot 2026-08-30 172519" src="https://github.com/user-attachments/assets/638fc6df-30a8-46c9-ba70-ba90c71f9b74" />

