# User Management for linux

This repository includes multiple playbooks that manages users in linux.

---

## tasks: 

- Create User
- Change usename
- Change password
- Delete User
- Lock User
- Unlock User

---

## Using in AAP

### General Config :
1. **Inventory:** create from file or manually  
2. **Credential:** SSH username/password + sudo

### Create User
Before running the playbook add a survey to define these variables :
1. username
2. user_password
3. user_group

### Change username :
Before running the template add a survey to define these variables :
1. old_username
2. new_username

### Change password
Before running the template add a survey to define these variables :
1. username
2. password

### Delete user
Before running the template add a survey to define these variables :
1. user_to_delete
2. backup_dir (directory to backup user files) => path : /backupdir/data (example)

### Lock users
Before running the template add a survey to define these variables :
1. users (list of users to lock , example : james,john ) comma seperated

### Unlock users
Before running the template add a survey to define these variables :
1. users (list of users to lock , example : james,john ) comma seperated

---

## Variables
### hosts variables : (in hosts.ini or create manuaaly in AAP)(inventory related)
- `ansible_host` – ip address of the host
- `ansible_user` – username of the host user
