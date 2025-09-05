Descripción
	Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/475/enc_flag).
	
Solución
	En terminal:
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/475/enc_flag
	--2025-09-05 03:10:09--  https://artifacts.picoctf.net/c/475/enc_flag
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.18, 3.170.131.77, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 349 [application/octet-stream]
	Saving to: 'enc_flag'
	
	enc_flag                   100%[========================================>]     349  --.-KB/s    in 0s      
	
	2025-09-05 03:10:09 (353 MB/s) - 'enc_flag' saved [349/349]
	
	evilmachine69-picoctf@webshell:~$ ls
	Addadshashanammu      README.txt  flag      retogrep  static.ltdis.strings.txt  strings
	Addadshashanammu.zip  enc_flag    ltdis.sh  static    static.ltdis.x86_64.txt   warm
	evilmachine69-picoctf@webshell:~$ cat enc_flag 
	VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
	RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
	MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
	VkpEVGxaYVdFMVhSbFZrTTBKVVZXcE9VazFXV2toT1dHUllDbUY2UWpSWk1GWlhWa2RHZEdWRlZs
	aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
	
	Ahora, usando cyberchef,  como entrada lo anterior y aplicando  from base64 6 veces, se obtiene:
	picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_492767d2}
	
Notas adicionales
	
	
Referencias
	https://gchq.github.io/CyberChef/
	