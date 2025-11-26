# NGINX Reverse Proxy Setup

## 1. Overview
NGINX handles SSL termination and forwards traffic to the OwnCloud Docker container.

## 2. Install NGINX
```bash
sudo apt install nginx
```

## 3. Use Valid SSL Certificates
Place certificates in: `nginx/certs/`

## 4. Example NGINX Config
```
server {
    listen 443 ssl;
    server_name cloud.example.com;

    ssl_certificate     /etc/nginx/certs/fullchain.pem;
    ssl_certificate_key /etc/nginx/certs/privkey.pem;

    location / {
        proxy_pass http://127.0.0.1:8080/;
        proxy_set_header Host $host;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```