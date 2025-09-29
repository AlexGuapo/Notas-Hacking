Descripción
	Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py
	--2025-09-10 17:17:29--  https://artifacts.picoctf.net/c/17/level3.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.18, 3.170.131.33, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 1337 (1.3K) [application/octet-stream]
	Saving to: 'level3.py'
	
	level3.py                        100%[=======================================================>]   1.31K  --.-KB/s    in 0s      
	
	2025-09-10 17:17:29 (98.5 MB/s) - 'level3.py' saved [1337/1337]
	
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
	--2025-09-10 17:17:39--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.77, 3.170.131.72, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 31 [application/octet-stream]
	Saving to: 'level3.flag.txt.enc'
	
	level3.flag.txt.enc              100%[=======================================================>]      31  --.-KB/s    in 0s      
	
	2025-09-10 17:17:39 (7.85 MB/s) - 'level3.flag.txt.enc' saved [31/31]
	
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
	--2025-09-10 17:17:47--  https://artifacts.picoctf.net/c/17/level3.hash.bin
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.18, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 16 [application/octet-stream]
	Saving to: 'level3.hash.bin'
	
	level3.hash.bin                  100%[=======================================================>]      16  --.-KB/s    in 0s      
	
	2025-09-10 17:17:47 (12.4 MB/s) - 'level3.hash.bin' saved [16/16]
	evilmachine69-picoctf@webshell:~$ nano level3.py
	evilmachine69-picoctf@webshell:~$ python3 level3.py 
	Please enter correct password for flag: 
	That password is incorrect
	.n;hS|33moa460`ii9X;chb<5;e%
	|:akODag7lS5n5b43jk
	                   a`:6f6i1
	picoCTF{m45h_fl1ng1ng_cd6ed2eb}
	,<c5F!1a523lk2214;
	c>j0dh97}
	k0hLV|b6foPd?6aebih]0c9g75j`.
	{g4<HZ(f:b;Th;beif=lQ47=k3anl*
	.o74R 32a3`8j0ae59Y7?hc0i;d)
	
Notas adicionales
	
	
Referencias
	
	