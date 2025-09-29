Descripción
	Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
	--2025-09-10 16:54:36--  https://artifacts.picoctf.net/c/25/fixme1.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.72, 3.170.131.18, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 837 [application/octet-stream]
	Saving to: 'fixme1.py'
	
	fixme1.py                        100%[=======================================================>]     837  --.-KB/s    in 0s      
	
	2025-09-10 16:54:36 (198 MB/s) - 'fixme1.py' saved [837/837]
	
	evilmachine69-picoctf@webshell:~$ nano fixme1.py 
	evilmachine69-picoctf@webshell:~$ python3 fixme1.py 
	That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
	
Notas adicionales
	
	
Referencias
	
	