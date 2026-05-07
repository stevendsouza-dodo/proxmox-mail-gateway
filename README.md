# Proxmox Mail Gateway Installation

## Step 1 - Update Server

apt update && apt upgrade -y

## Step 2 - Add Proxmox Repository

echo "deb http://download.proxmox.com/debian/pmg bookworm pmg-no-subscription" > /etc/apt/sources.list.d/pmg-install-repo.list

## Step 3 - Add Repository Key

wget https://enterprise.proxmox.com/debian/proxmox-release-bookworm.gpg -O /etc/apt/trusted.gpg.d/proxmox-release-bookworm.gpg

## Step 4 - Install PMG

apt update
apt install proxmox-mailgateway -y

## Step 5 - Open Web Panel

https://SERVER-IP:8006
