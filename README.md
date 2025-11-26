# OwnCloud Enterprise Implementation – Project Documentation






This repository contains a production‑ready OwnCloud deployment designed for enterprise environments. The setup includes:
---
- Dockerized OwnCloud 10.x
- Active Directory authentication (LDAP)
- NGINX reverse proxy with valid SSL certificates
- Shared folder accessible by all users
- Web + terminal access via WebDAV (davfs2)
- Hardened security configuration

### **Project Structure**
```
docker/               → docker‑compose environment
nginx/                → reverse proxy configs and certificates
docs/                 → technical documentation (AD, NGINX, shared storage)
```

### **Key Features**
- Secure authentication via Active Directory (LDAP)
- Single sign‑on behavior for Linux/Windows users via WebDAV
- External local storage mounted for all authenticated users
- Production‑grade SSL termination
- Modular and easy to extend

### **Quick Start**
```bash
cd docker
cp env.example .env
docker-compose up -d
```

### **Documentation**
- [Active Directory Integration](docs/ad-integration.md)
- [NGINX Reverse Proxy Setup](docs/nginx-setup.md)
- [Shared Folder Setup](docs/shared-folder-setup.md)

---
