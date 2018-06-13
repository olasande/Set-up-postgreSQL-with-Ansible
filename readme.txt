Starting VM with vagrant

Manual work in order to get postgres_db running:
1. Need to ssh into ansible_control to run playbook.yml
2. Need to ssh into postgres_server as well: ssh vagrant@172.28.128.4 pw: vagrant.
3. Change the fields on postgres_server's pg_hba.conf file (/etc/postgresql/9.3/main) from peer to trust.
4. Restart postgresql server like this: sudo service postgresql restart
5. Trying to check status on db_server on postgres_server's side is not possible at the moment. Unable to login. No password set.
This is a problem because the user is connecting from another session /VM

Then it should work fine.
Next goal is to automate as many of these steps as possible.
