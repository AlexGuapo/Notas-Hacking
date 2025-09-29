Descripción
	How to automate tasks to run at intervals on linux servers?
	Additional details will be available after launching your challenge instance.
	
Solución
	
	evilmachine69-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 65450
	picoplayer@saturn.picoctf.net's password: 
	Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1035-aws x86_64)
	
	 * Documentation:  https://help.ubuntu.com
	 * Management:     https://landscape.canonical.com
	 * Support:        https://ubuntu.com/advantage
	
	This system has been minimized by removing packages and content that are
	not required on a system that users do not log into.
	
	To restore this content, you can run the 'unminimize' command.
	Last login: Sun Sep 14 22:04:29 2025 from 3.140.102.47
	picoplayer@challenge:~$ cd ..
	picoplayer@challenge:/home$ cd ..
	picoplayer@challenge:/$ grep -r pico *
	grep: challenge: Permission denied
	grep: etc/.pwd.lock: Permission denied
	etc/group:picoplayer:x:1000:
	grep: etc/gshadow: Permission denied
	etc/passwd:picoplayer:x:1000:1000::/home/picoplayer:/bin/bash
	grep: etc/security/opasswd: Permission denied
	grep: etc/shadow: Permission denied
	etc/subgid:picoplayer:100000:65536
	etc/subuid:picoplayer:100000:65536
	grep: etc/ssh/ssh_host_ecdsa_key: Permission denied
	grep: etc/ssh/ssh_host_ed25519_key: Permission denied
	grep: etc/ssh/ssh_host_rsa_key: Permission denied
	grep: etc/ssh/ssh_host_dsa_key: Permission denied
	etc/crontab:# picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}
	
Notas adicionales
	
	
Referencias
	
	