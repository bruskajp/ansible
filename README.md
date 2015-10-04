This is COSI's [ansible](http://ansible.com) playbook repository.

This is how we automate our infrastructure, and also how we pass down
information from generation to generation. Our collective best practices are
encoded here.

# `ansible` user's public key

`ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIEale3rgwFlUeyFUCGtSFnYC0gHJpl1+qFv0hmy+hU/C ansible`

# Setting up a new machine with ansible

Add the IP or hostname in `inventory`. Then, run `./setup $ip
$desired-username $user-sshkey`. This assumes the machine is "fresh". A fresh
machine has Python and an SSH server, a root user, and an ansible user with
the key above in `~/ansible/authorized_keys`, but doesn't need anything
else. A minimal Debian install works, for example.

This script will install everything necessary on that server, set its
hostname, configure its firewall, etc.
