Descripción
	My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:
	- [challenge.zip](https://artifacts.picoctf.net/c_titan/70/challenge.zip)
	
Solución
	
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/70/challenge.zip
	--2025-09-29 16:27:11--  https://artifacts.picoctf.net/c_titan/70/challenge.zip
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.18, 3.170.131.33, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 24662 (24K) [application/octet-stream]
	Saving to: 'challenge.zip.2'
	
	challenge.zip.2             100%[========================================>]  24.08K  --.-KB/s    in 0.01s   
	
	2025-09-29 16:27:11 (2.27 MB/s) - 'challenge.zip.2' saved [24662/24662]
	
	evilmachine69-picoctf@webshell:~$ unzip challenge.zip.2
	Archive:  challenge.zip.2
	replace drop-in/.git/description? [y]es, [n]o, [A]ll, [N]one, [r]ename: A
	  inflating: drop-in/.git/description  
	  inflating: drop-in/.git/hooks/applypatch-msg.sample  
	  inflating: drop-in/.git/hooks/commit-msg.sample  
	  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
	  inflating: drop-in/.git/hooks/post-update.sample  
	  inflating: drop-in/.git/hooks/pre-applypatch.sample  
	  inflating: drop-in/.git/hooks/pre-commit.sample  
	  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
	  inflating: drop-in/.git/hooks/pre-push.sample  
	  inflating: drop-in/.git/hooks/pre-rebase.sample  
	  inflating: drop-in/.git/hooks/pre-receive.sample  
	  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
	  inflating: drop-in/.git/hooks/update.sample  
	  inflating: drop-in/.git/info/exclude  
	 extracting: drop-in/.git/refs/heads/main  
	   creating: drop-in/.git/refs/heads/feature/
	 extracting: drop-in/.git/refs/heads/feature/part-1  
	  inflating: drop-in/.git/refs/heads/feature/part-2  
	 extracting: drop-in/.git/refs/heads/feature/part-3  
	 extracting: drop-in/.git/HEAD       
	  inflating: drop-in/.git/config     
	 extracting: drop-in/.git/objects/77/d6ceca6fe23b57d88cf16f20003e10d6715690  
	   creating: drop-in/.git/objects/b9/
	 extracting: drop-in/.git/objects/b9/32e8c048154a46d224cd7691c99dc8cb88164a  
	 extracting: drop-in/.git/objects/54/c7842e34d03976ddc080a9dd76742751024358  
	 extracting: drop-in/.git/objects/6e/17fb3a35364b4f9bb8bef8b5e6a5af2d3e7dfa  
	 extracting: drop-in/.git/objects/43/e44dd37ba0c0adc3d78d0b85d699859ec8d75c  
	   creating: drop-in/.git/objects/f6/
	 extracting: drop-in/.git/objects/f6/5544e4f1511fe1d1dfff03c4d65869da039b8e  
	 extracting: drop-in/.git/objects/7a/b4e25c0cd108374b2275fdb1fcdf635e591833  
	 extracting: drop-in/.git/objects/d1/f3407cee4479c075997b497fa290ca636fe258  
	 extracting: drop-in/.git/objects/d3/563a2c62ab2c95c5c13f3377cc6d79b2411c22  
	 extracting: drop-in/.git/objects/45/6656eef7d5d6b8b7d49dc4f7fe6ff456c0bb91  
	 extracting: drop-in/.git/objects/0a/e601af6790d90cf89319f9a6520b4e2f15db35  
	 extracting: drop-in/.git/objects/5c/00b43f48516d7cc81ea1f497b4d43ae6a84c4c  
	  inflating: drop-in/.git/index      
	 extracting: drop-in/.git/COMMIT_EDITMSG  
	  inflating: drop-in/.git/logs/HEAD  
	  inflating: drop-in/.git/logs/refs/heads/main  
	   creating: drop-in/.git/logs/refs/heads/feature/
	  inflating: drop-in/.git/logs/refs/heads/feature/part-1  
	  inflating: drop-in/.git/logs/refs/heads/feature/part-2  
	  inflating: drop-in/.git/logs/refs/heads/feature/part-3  
	  inflating: drop-in/flag.py         
	evilmachine69-picoctf@webshell:~$ cd drop-in/
	evilmachine69-picoctf@webshell:~/drop-in$ git reflog
	evilmachine69-picoctf@webshell:~/drop-in$ git checkout f65544e
	Note: switching to 'f65544e'.
	
	You are in 'detached HEAD' state. You can look around, make experimental
	changes and commit them, and you can discard any commits you make in this
	state without impacting any branches by switching back to a branch.
	
	If you want to create a new branch to retain commits you create, you may
	do so (now or later) by using -c with the switch command. Example:
	
	  git switch -c <new-branch-name>
	
	Or undo this operation with:
	
	  git switch -
	
	Turn off this advice by setting config variable advice.detachedHead to false
	
	HEAD is now at f65544e add part 1
	evilmachine69-picoctf@webshell:~/drop-in$ cat flag.py 
	print("Printing the flag...")
	print("picoCTF{t3@mw0rk_", end='')evilmachine69-picoctf@webshell:~/drop-in$ git reflog
	evilmachine69-picoctf@webshell:~/drop-in$ git checkout d3563a2
	Previous HEAD position was f65544e add part 1
	HEAD is now at d3563a2 add part 2
	evilmachine69-picoctf@webshell:~/drop-in$ cat flag.py 
	print("Printing the flag...")
	
	print("m@k3s_th3_dr3@m_", end='')evilmachine69-picoctf@webshell:~/drop-in$ git reflog 
	evilmachine69-picoctf@webshell:~/drop-in$ git checkout 5c00b43
	Previous HEAD position was d3563a2 add part 2
	HEAD is now at 5c00b43 add part 3
	evilmachine69-picoctf@webshell:~/drop-in$ cat flag.py 
	print("Printing the flag...")
	
	print("w0rk_7ffa0077}")
	
	picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ffa0077}
	
Notas adicionales
	
	
Referencias
	
	