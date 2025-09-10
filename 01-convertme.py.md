Descripción
	Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
	--2025-09-10 16:36:44--  https://artifacts.picoctf.net/c/23/convertme.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.18, 3.170.131.77, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 1189 (1.2K) [application/octet-stream]
	Saving to: 'convertme.py'
	
	convertme.py                 100%[============================================>]   1.16K  --.-KB/s    in 0s      
	
	2025-09-10 16:36:44 (48.5 MB/s) - 'convertme.py' saved [1189/1189]
	
	evilmachine69-picoctf@webshell:~$ python3 convertme.py 
	If 58 is in decimal base, what is it in binary base?
	Answer: 00111010                 
	That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
	
Notas adicionales
	Se uso la calculadora de Windows para la conversión 
	
Referencias
	Calculadora de Windows
	