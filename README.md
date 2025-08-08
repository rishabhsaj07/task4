Task 4 – Firewall Configuration using UFW 

# Objective
Configure and test basic firewall rules to allow or block traffic using UFW (Uncomplicated Firewall) on Linux.

#Steps Performed

# 1. Checked Firewall Status
sudo ufw status
Output: Status: inactive

2. Enabled UFW
sudo ufw enable
Output: Firewall is active and enabled on system startup

3. Viewed Current Rules
sudo ufw status numbered
Initial rules showed port 80 blocked for outbound traffic.

4. Blocked Port 23 (Telnet)
sudo ufw deny 23/tcp
This blocks all TCP connections on port 23 (Telnet).

5. Tested the Rule
telnet IP_ADDRESS
Output:
Trying IP_ADDRESS...
telnet: Unable to connect to remote host: Connection refused
✅ Connection was blocked successfully.

6. Removed the Block Rule
sudo ufw delete deny 23/tcp
This restores the original firewall configuration.