### Make the shell more convinent
#### we need to run the following command in the victim machine to make the shell more useful
python3 -c 'import pty; pty.spawn("/bin/bash");'


then we need to set "TERM=xterm" to execute the previous shell 
