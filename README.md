# speedtest2DynamoDB-ansible-playbook

Ansible playbook to provision my Raspberry Pi (running [OSMC](https://osmc.tv/)) to configure and run [speedtest2DynamoDB](https://github.com/ujuettner/speedtest2DynamoDB).

Entry point is `site.yml` - run it with `ansible-playbook site.yml` (or dry-run it with `ansible-playbook site.yml --check`).

The playbook relies on several variables being set. Therefore, my hosts file looks like this:
```
[raspberry-pi]
10.1.1.9 ansible_ssh_user=osmc ansible_user=osmc ansible_ssh_pass=sEcReT aws_region=eu-west-1 aws_access_key_id=MY_ACCESS_KEY_ID aws_secret_access_key=MY_SECRET_ACCESS_KEY
```
