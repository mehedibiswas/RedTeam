#### suid=set user id
If any file has the suid set(s) the file will run with all the privileges have the owner of the file.Doesn't matter
who run the file.
#### ls -al /bin/ping
-rwsr-xr-x 1 root root 156136 Sep 24  2024 /bin/ping
#### Find which binary has suid set permission
- find / -type f -perm -4000 2>/dev/null
#### Resoureces
- https://freedium.cfd/https://medium.com/@amaraltohami30/suid-environmental-variable-privilege-escalation-linux-priv-esc-a3bfc44eeb14
- https://www.youtube.com/watch?v=v_IpB98OzeI&list=PL-DxAN1jsRa818Ew7WI1_ngpULwDDESSI&index=6
