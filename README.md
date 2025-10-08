# RHEL 9 Sysadmin Project

## Objective
Demonstrate real-world Red Hat Linux 9 sysadmin skills, including hostname configuration, NTP, timezone, Apache web server deployment, firewall and SELinux configuration, and automation using Ansible.

## Tasks Performed
1. Configured hostname: `rhel-admin.localdomain`
2. Set timezone: `Asia/Kolkata`
3. Enabled NTP (chronyd) and verified synchronization
4. Installed Apache Web Server (`httpd`)
5. Created website folder `/var/www/admin.local` with a test HTML page
6. Configured SELinux context for the website folder
7. Enabled and configured FirewallD to allow HTTP traffic
8. Enabled Apache and FirewallD on system boot
9. Verified website accessibility using `curl http://localhost`
10. Automated all tasks using Ansible playbook

## Commands Used
```bash
hostnamectl
timedatectl
chronyc tracking
dnf install -y httpd chrony
systemctl enable --now httpd chronyd firewalld
firewall-cmd --permanent --add-service=http
firewall-cmd --reload
curl http://localhost
=======
# RHEL9-SysAdmin-Project
Red Hat Linux 9 Sysadmin Practice Project
# 🧰 Project 3 – Secure Apache Web Server with SSL (RHEL 9)

## 🔹 Objective
Set up a secure HTTPS web server using Apache and mod_ssl with a custom DocumentRoot on RHEL 9.

## 🔹 Tasks Performed
- Installed Apache and mod_ssl
- Created custom DocumentRoot `/var/www/webapp`
- Configured SSL in `/etc/httpd/conf.d/ssl.conf`
- Enabled HTTPS service in firewall
- Restarted and verified Apache HTTPS service

## 🔹 Validation
```bash
curl -k https://localhost

>>>>>>> 4929ed12c9a104b8d3c5344c34246dd8690b3409
