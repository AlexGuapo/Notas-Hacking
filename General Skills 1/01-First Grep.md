Descripción
	Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
	
Solución
	En la terminal ponemos lo siguiente:
	```evilmachine69-picoctf@webshell:~/retogrep$ wget https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
	--2025-09-03 04:02:02--  https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
	Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
	Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 14551 (14K) [application/octet-stream]
	Saving to: 'file.1'
	
	file.1                            100%[=============================================================>]  14.21K  --.-KB/s    in 0s      
	
	2025-09-03 04:02:02 (407 MB/s) - 'file.1' saved [14551/14551]
	
	evilmachine69-picoctf@webshell:~/retogrep$ ls
	file  file.1
	evilmachine69-picoctf@webshell:~/retogrep$ grep picoCTF file.1
	picoCTF{grep_is_good_to_find_things_dba08a45}
	
Notas adicionales
	
	
Referencias
	
	