## Install the OpenSSH server:
```bash
    sudo apt install openssh-server
    sudo systemctl start ssh
    sudo systemctl enable ssh
    sudo systemctl status ssh
```
## SSH from another machine, use:
```bash
    ssh username@ip_address
```
## configuration file located at:
```bash
    cd /etc/ssh/sshd_config
```
## Verify SSH Daemon Configuration:
**Ensure PasswordAuthentication and ChallengeResponseAuthentication are set to yes**

`PasswordAuthentication yes`

`ChallengeResponseAuthentication yes`

## Restart the SSH service
```bash
    sudo systemctl restart ssh
```

## Check if the user account exists

```bash
    sudo cat /etc/passwd
```

## Ensure port 22 is allowed through the firewall (UFW)
```bash
    sudo ufw reload
    sudo ufw allow 22/tcp
```