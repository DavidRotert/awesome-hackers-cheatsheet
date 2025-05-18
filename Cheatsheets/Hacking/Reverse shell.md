#bash #pivoting #privilege-escalation

## Stabilizing shell
### With Python
On target host:
```
python3 -c 'import pty; pty.spawn("/bin/bash")'
Ctrl+Z
```

On attacker host:
```
stty raw -echo && fg
```

On target host:
```
export TERM=xterm
```