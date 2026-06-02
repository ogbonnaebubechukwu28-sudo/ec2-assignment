cat > README.md << 'EOF'
# EC2 Provisioning Assignment

## Objective
Provision an AWS EC2 instance and securely connect to it using SSH.

## Steps Performed
1. Launched an Ubuntu EC2 instance on AWS
2. Created and downloaded a Key Pair (myec2key.pem)
3. Configured Security Group to allow SSH (Port 22) and HTTP (Port 80)
4. Connected to the instance via SSH
5. Ran server information commands
6. Updated server packages
7. Installed and started Nginx web server
8. Verified Nginx welcome page via public IP
9. Created a custom HTML page

## Commands Used

### SSH Connection
ssh -i ~/myec2key.pem ubuntu@16.171.133.47

### Server Information Commands
whoami
hostname
pwd
uptime
free -h
df -h

### Update Server
sudo apt update && sudo apt upgrade -y

### Install Nginx
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl status nginx
EOF