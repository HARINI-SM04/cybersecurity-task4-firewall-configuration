# Task 4 – Setup and Use a Firewall on Linux Using UFW

## Objective

To configure and test basic firewall rules using UFW (Uncomplicated Firewall) in Kali Linux.

## Tools Used

* Kali Linux
* UFW (Uncomplicated Firewall)

## Procedure

### 1. Installed UFW

Updated package repositories and installed UFW.

Command:
sudo apt install ufw -y

### 2. Checked Firewall Status

Verified the current firewall configuration.

Command:
sudo ufw status verbose

### 3. Enabled Firewall

Activated UFW.

Command:
sudo ufw enable

### 4. Blocked Telnet Port 23

Added a firewall rule to block incoming Telnet connections.

Command:
sudo ufw deny 23

### 5. Allowed SSH Port 22

Configured the firewall to permit SSH access.

Command:
sudo ufw allow 22

### 6. Verified Firewall Rules

Displayed all active firewall rules.

Command:
sudo ufw status numbered

### 7. Tested Firewall Rule

Attempted to connect to Telnet port 23 and confirmed that the connection was blocked.

Command:
telnet localhost 23

### 8. Removed Test Rule

Deleted the Telnet block rule and restored the firewall configuration.

Command:
sudo ufw delete deny 23

## Results

Successfully configured firewall rules using UFW. Verified that Telnet traffic on port 23 was blocked while SSH traffic on port 22 was allowed.

## Conclusion

This task demonstrated the basic use of UFW for managing firewall rules. Firewalls help protect systems by controlling inbound and outbound network traffic according to predefined security rules.

