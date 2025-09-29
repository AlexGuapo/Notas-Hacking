Descripción
	Run the Python script `code.py` in the same directory as `codebook.txt`.
	- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
	- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py
	--2025-09-10 16:34:12--  https://artifacts.picoctf.net/c/2/code.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.33, 3.170.131.18, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 1278 (1.2K) [application/octet-stream]
	Saving to: 'code.py'
	
	code.py                      100%[============================================>]   1.25K  --.-KB/s    in 0s      
	
	2025-09-10 16:34:12 (471 MB/s) - 'code.py' saved [1278/1278]
	
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt
	--2025-09-10 16:34:23--  https://artifacts.picoctf.net/c/2/codebook.txt
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.18, 3.170.131.77, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 27 [application/octet-stream]
	Saving to: 'codebook.txt'
	
	codebook.txt                 100%[============================================>]      27  --.-KB/s    in 0s      
	
	2025-09-10 16:34:23 (10.2 MB/s) - 'codebook.txt' saved [27/27]
	
	evilmachine69-picoctf@webshell:~$ ls
	Addadshashanammu      big-zip-files      codebook.txt  files.zip  retogrep  static.ltdis.strings.txt  warm
	Addadshashanammu.zip  big-zip-files.zip  enc_flag      flag       runme.py  static.ltdis.x86_64.txt   wget-log
	README.txt            code.py            files         ltdis.sh   static    strings
	evilmachine69-picoctf@webshell:~$ python3 code.py
	picoCTF{c0d3b00k_455157_7d102d7a}
	
Notas adicionales
	
	
Referencias
	
	