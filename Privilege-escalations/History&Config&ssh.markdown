After landing any machine we should look for these files
### History file
- ls -al
- look any history file(specially .bash_history)  and cat it to see secret info like credentials.
### Config file
- ls -al
- look for any config file like .config .ovpn etc and cat it to see any secret information.
### ssh key
Here we create ssh key(public,private both) and and we will store the public key into victim machine so that we can
login without password.
- key generation command "ssh-keygen -t rsa" we escape passphrase pressing enter.
- we go to .ssh folder to see public & private keys.
- We will generate ssh key in both machines(attacker & victim)
- we copy the attacker public key and save it into victim machine using vim and name the file authorized_keys and save
  it in .ssh folder
- we use "ssh user@10.10.12.172 -oHostKeyAlgorithms=+ssh-rsa " to login.We can avoid "-oHostKeyAlgorithms=+ssh-rsa "
  when it doesn't support,mordern ssh doesn't support it.

### Resoures
- https://www.youtube.com/watch?v=z_4xOfA9VfI&list=PL-DxAN1jsRa818Ew7WI1_ngpULwDDESSI&index=8
- https://steflan-security.com/linux-privilege-escalation-exploiting-misconfigured-ssh-keys/
