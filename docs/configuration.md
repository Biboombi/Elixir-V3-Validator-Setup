# Configuration Guide

## VPS Setup
Before running the node, purchase a VPS, such as Cloud 2 from Contabo.

## Proxy Setup (Optional)
If you encounter issues pulling Docker images, configure a proxy:

```bash
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://docker.dadunode.com"]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
