Descripción
	What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:
	- [challenge.zip](https://artifacts.picoctf.net/c_titan/162/challenge.zip)
	
Solución
	
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/162/challenge.zip
	--2025-09-29 16:14:23--  https://artifacts.picoctf.net/c_titan/162/challenge.zip
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.18, 3.170.131.33, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 17739 (17K) [application/octet-stream]
	Saving to: 'challenge.zip'
	
	challenge.zip               100%[========================================>]  17.32K  --.-KB/s    in 0.005s  
	
	2025-09-29 16:14:23 (3.63 MB/s) - 'challenge.zip' saved [17739/17739]
	
	evilmachine69-picoctf@webshell:~$ ls
	Addadshashanammu      codebook.txt  flag                 level3.hash.bin  static.ltdis.strings.txt
	Addadshashanammu.zip  convertme.py  issues               level3.py        static.ltdis.x86_64.txt
	README.txt            enc_flag      level1.flag.txt.enc  ltdis.sh         strings
	big-zip-files         files         level1.py            retogrep         warm
	big-zip-files.zip     files.zip     level2.flag.txt.enc  runme.py         wget-log
	challenge.zip         fixme1.py     level2.py            serpentine.py
	code.py               fixme2.py     level3.flag.txt.enc  static
	evilmachine69-picoctf@webshell:~$ cd challenge.zip
	-bash: cd: challenge.zip: Not a directory
	evilmachine69-picoctf@webshell:~$ cd challenge.zip/
	-bash: cd: challenge.zip/: Not a directory
	evilmachine69-picoctf@webshell:~$ unzip challenge.zip 
	Archive:  challenge.zip
	   creating: drop-in/
	  inflating: drop-in/message.txt     
	   creating: drop-in/.git/
	   creating: drop-in/.git/branches/
	  inflating: drop-in/.git/description  
	   creating: drop-in/.git/hooks/
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
	   creating: drop-in/.git/info/
	  inflating: drop-in/.git/info/exclude  
	   creating: drop-in/.git/refs/
	   creating: drop-in/.git/refs/heads/
	 extracting: drop-in/.git/refs/heads/master  
	   creating: drop-in/.git/refs/tags/
	 extracting: drop-in/.git/HEAD       
	  inflating: drop-in/.git/config     
	   creating: drop-in/.git/objects/
	   creating: drop-in/.git/objects/pack/
	   creating: drop-in/.git/objects/info/
	   creating: drop-in/.git/objects/43/
	 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
	   creating: drop-in/.git/objects/25/
	 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
	   creating: drop-in/.git/objects/71/
	 extracting: drop-in/.git/objects/71/2314f105348e295f8cadd7d7dc4e9fa871e9a2  
	  inflating: drop-in/.git/index      
	 extracting: drop-in/.git/COMMIT_EDITMSG  
	   creating: drop-in/.git/logs/
	  inflating: drop-in/.git/logs/HEAD  
	   creating: drop-in/.git/logs/refs/
	   creating: drop-in/.git/logs/refs/heads/
	  inflating: drop-in/.git/logs/refs/heads/master  
	evilmachine69-picoctf@webshell:~$ ls
	Addadshashanammu      codebook.txt  fixme2.py            level3.flag.txt.enc  static
	Addadshashanammu.zip  convertme.py  flag                 level3.hash.bin      static.ltdis.strings.txt
	README.txt            drop-in       issues               level3.py            static.ltdis.x86_64.txt
	big-zip-files         enc_flag      level1.flag.txt.enc  ltdis.sh             strings
	big-zip-files.zip     files         level1.py            retogrep             warm
	challenge.zip         files.zip     level2.flag.txt.enc  runme.py             wget-log
	code.py               fixme1.py     level2.py            serpentine.py
	evilmachine69-picoctf@webshell:~$ cd drop-in/
	evilmachine69-picoctf@webshell:~/drop-in$ git status
	On branch master
	nothing to commit, working tree clean
	evilmachine69-picoctf@webshell:~/drop-in$ git log
	
	commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
	Author: picoCTF <ops@picoctf.com>
	Date:   Tue Mar 12 00:07:26 2024 +0000
	
	    picoCTF{t1m3m@ch1n3_e8c98b3a}
Notas adicionales
	
	
Referencias
	
	