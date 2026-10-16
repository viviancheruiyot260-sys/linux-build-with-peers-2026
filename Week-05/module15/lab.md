 User and Group Management — Labs

## Lab 1: View User Information
```bash
id
cat /etc/passwd
```
**Learned:** How to view user IDs and account details.

## Lab 2: View Groups
```bash
id -G
cat /etc/group
getent group sudo
```
**Learned:** How to check group membership.

## Lab 3: Use Administrative Access
```bash
sudo whoami
whoami
```
**Learned:** The difference between running a command as root and as a regular user.

## Lab 4: Identify System Accounts
```bash
grep nologin /etc/passwd
```
**Learned:** Some accounts are designed for services, not interactive login.

## Lab 5: View Logged-In Users
```bash
who
w
```
**Learned:** How to see current users and their activity.

## Lab 6: Check Login History
```bash
last
```
**Learned:** How to view recorded logins and reboot history.

## Lab 7: Explore Password Information
```bash
getent passwd "$USER"
sudo head -5 /etc/shadow
```
**Learned:** Where account and password-related information is stored.

**Security:** Never publish password hashes or sensitive `/etc/shadow` output.


