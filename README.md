### Ansible playbook for pgBackrest [pb-pgbackrest]  

This playbook runs with 3 server:
- Primary PostgreSQL Server (primary)
- Standby PostgreSQL Server (standby)
- Backup Server (backup)

You can change IP addresses inside 'hosts' file to your server IP's. Then you can execute the playbook with this command:
```bash
$ ansible-playbook launch.yml
```
NOTE: IP addresses in hosts file belongs to my test servers. They don't exist anymore. At least for me. :)
