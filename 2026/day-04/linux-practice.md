- Check running processes
    - ps -  snapshot of processes running in the background
     -e / -a = list all the running processes
    - ps aux   
        a = all users
        u = user oriented format, provide info like user who won process, CPU/memoruy usuage
        x = extended - inclludes processes that are not attached to a controlling terminal (TTY) such as background services tr=erminal.

        eg: 
        ps aux | grep [process_name]
        ps aux --sort pid
        ps aux --forest / pstree =  These commands display processes in a tree-like structure, showing parent-child relationships

    - top = real-time , dynamic view of running processes updating every 3 seconds by default
    - Inside top, you can use keys for interaction:
        k: to kill a process (requires entering the PID).
        q: to exit.
        M: to sort the list by memory usage.
        P: to sort by CPU usage (default) 

    - htop = advance version of top

    - pgrep =        

- Inspect one systemd service
        
sudo systemctl start <service>
sudo systemctl stop <service>
sudo systemctl restart <service>
sudo systemctl reload <service>
sudo systemctl enable <service> =  if enabled it will load at boottime
sudo systemctl disable <serv
sudo systemctl status <service>
sudo journalctl
sudo journalctl -u <service> -f
sudo systemctl reboot
sudo systemctl poweroff
systemd-analyze
systemctl list-units --type=service  = list all active services
systemctl list-unit-files --type=service = list all disabled services
sudo systemctl mask <service> = if masked it cann =ot start 
sudo systemctl unmask <service>

- Capture a small troubleshooting flow
    Check the system health using top/htop
    check disk usuage = df
    check if service is running : systemctl startus <service>
    check for logs : journalctl -u <service> -f
    check if it needs restart : systemctl restart



- Run and record output for **at least 6 commands**
- Include **2 process commands** (`ps`, `top`, `pgrep`, etc.)
- Include **2 service commands** (`systemctl status`, `systemctl list-units`, etc.)
- Include **2 log commands** (`journalctl -u <service>`, `tail -n 50`, etc.)
- Pick **one service on your system** (example: `ssh`, `cron`, `docker`) and inspect it
- Keep it **simple and actionable**
