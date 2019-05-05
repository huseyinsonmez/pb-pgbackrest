### Ansible playbook for pgBackrest

This playbook runs with 3 server:
- Primary PostgreSQL Server (primary)
- Standby PostgreSQL Server (standby)
- Backup Server (backup)

You can change IP addresses inside 'hosts' file to your server IP's and pgBackrest setting for your setup. Then you can execute the playbook with this command:
```bash
$ ansible-playbook launch.yml
```

Then in your "/var/lib/pgsql/11/data/postgresql.conf" file, you need to uncomment two line and change it like below:

```bash
archive_mode = on
archive_command = "/usr/bin/pgbackrest --stanza=db-primary archive-push %p
```

NOTE: IP addresses in hosts file belongs to my test servers. They don't exist anymore. At least for me. :)
