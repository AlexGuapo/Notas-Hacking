Descripción
	Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static)? This [BASH script](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh) might help!
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static
	--2025-09-05 02:48:27--  https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static
	Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
	Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 8376 (8.2K) [application/octet-stream]
	Saving to: 'static'
	
	static                         100%[=================================================>]   8.18K  --.-KB/s    in 0s      
	
	2025-09-05 02:48:27 (323 MB/s) - 'static' saved [8376/8376]
	
	evilmachine69-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh
	--2025-09-05 02:48:55--  https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh
	Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
	Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 785 [application/octet-stream]
	Saving to: 'ltdis.sh'
	
	ltdis.sh                       100%[=================================================>]     785  --.-KB/s    in 0s      
	
	2025-09-05 02:48:55 (537 MB/s) - 'ltdis.sh' saved [785/785]
	
	evilmachine69-picoctf@webshell:~$ ./ltdis.sh static
	-bash: ./ltdis.sh: Permission denied
	evilmachine69-picoctf@webshell:~$ chmod +x static
	evilmachine69-picoctf@webshell:~$ chmod +x ltdis.sh 
	evilmachine69-picoctf@webshell:~$ ./ltdis.sh static
	Attempting disassembly of static ...
	Disassembly successful! Available at: static.ltdis.x86_64.txt
	Ripping strings from binary with file offsets...
	Any strings found in static have been written to static.ltdis.strings.txt with file offset
	evilmachine69-picoctf@webshell:~$ grep picoCTF static.ltdis.strings.txt
	   1020 picoCTF{d15a5m_t34s3r_98d35619}
	
Notas adicionales
	
	
Referencias
	
	