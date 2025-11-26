# Active Directory Integration

## 1. LDAP Connection Settings
- Host: LDAP domain controller (e.g., `dc01.domain.local`)
- Port: 389
- Base DN: `DC=domain,DC=local`
- Agent DN: `CN=svc-owncloud,OU=Service Accounts,DC=domain,DC=local`

## 2. Limit Login to a Single Group
```
(&(objectClass=user)(memberOf=CN=OwnCloudUsers,OU=Groups,DC=domain,DC=local))
```

## 3. Username Attribute
```
sAMAccountName
```

## 4. Group Handling
- Maintain group membership from AD
- Only users in `OwnCloudUsers` can log in
