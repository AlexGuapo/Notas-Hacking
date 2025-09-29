Descripción
	Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
	--2025-09-10 17:00:18--  https://artifacts.picoctf.net/c/4/fixme2.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.72, 3.170.131.77, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 1029 (1.0K) [application/octet-stream]
	Saving to: 'fixme2.py'
	
	fixme2.py                        100%[=======================================================>]   1.00K  --.-KB/s    in 0s      
	
	2025-09-10 17:00:19 (953 MB/s) - 'fixme2.py' saved [1029/1029]
	
	evilmachine69-picoctf@webshell:~$ python3 fixme2.py 
	  File "/home/evilmachine69-picoctf/fixme2.py", line 22
	    if flag = "":
	       ^^^^^^^^^
	SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
	evilmachine69-picoctf@webshell:~$ nano fixme2.py 
	evilmachine69-picoctf@webshell:~$ python3 fixme2.py 
	That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
	
Notas adicionales
	
	
Referencias
	
	