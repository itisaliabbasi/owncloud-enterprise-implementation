# Shared Folder Setup

## 1. Create Shared Folder on Host
```bash
sudo mkdir -p /mnt/shared-folder
sudo chmod 777 /mnt/shared-folder
```

## 2. Mount into Docker
Already mapped in `docker-compose.yml`:
```
/mnt/shared-folder:/shared
```

## 3. Add as External Storage in OwnCloud
- Storage type: **Local**
- Folder: `/shared`
- Permissions: **Read/Write for all users**

## 4. WebDAV Access for Linux
```bash
sudo mount -t davfs https://cloud.example.com/remote.php/dav/files/<username>/ /mnt/mycloud
```
