# Set up for inventory kiosk

With etcher, flash new sd card with minimal raspbian image

Log into pi with following creds:
```
u: pi
p: raspberry
```

turn on networking

`sudo raspi-config`

enable ssh

`sudo systemctl start ssh && sudo systemctl enable ssh`

copy-ssh-id to pi@ip

`ssh-copy-id pi@ip.address.x.x`

add new pi to pi group in ansible inventory

run playbook (become password is raspberry):

`ansible-playbook playbooks/kiosk_setup.yml --ask-become-pass`


