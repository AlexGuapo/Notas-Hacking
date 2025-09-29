Descripción
	This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).
	
Solución
	Usando la terminal ponemos:
	```evilmachine69-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
	--2025-09-03 04:07:57--  https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
	Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
	Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 34 [application/octet-stream]
	Saving to: 'flag'
	
	flag                              100%[=============================================================>]      34  --.-KB/s    in 0s      
	
	2025-09-03 04:07:57 (20.8 MB/s) - 'flag' saved [34/34]
	
	evilmachine69-picoctf@webshell:~$ cat flag
	picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
	
Notas adicionales
	
	
Referencias
	
	