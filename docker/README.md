## Docker Environment
This folder contains everything required to run OwnCloud using Docker.

### Files
- **docker-compose.yml** – OwnCloud + MariaDB + Redis + Cron
- **env.example** – Sample environment variables to copy into `.env`

### Usage
```bash
cp env.example .env
docker-compose up -d
```

### Stopping Services
```bash
docker-compose down
```

