## Install the OpenSSH server:
sudo apt install openssh-server
sudo systemctl start ssh
sudo systemctl enable ssh
sudo systemctl status ssh

# configuration file located at

/etc/ssh/sshd_config

# SSH from another machine, use:

ssh username@ip_address

## Verify SSH Daemon Configuration:

# Ensure PasswordAuthentication and ChallengeResponseAuthentication are set to yes
PasswordAuthentication yes
ChallengeResponseAuthentication yes

# Restart the SSH service
sudo systemctl restart ssh

# Check if the user account exists
sudo cat /etc/passwd

# Ensure port 22 is allowed through the firewall (UFW)
sudo ufw allow 22/tcp
sudo ufw reload