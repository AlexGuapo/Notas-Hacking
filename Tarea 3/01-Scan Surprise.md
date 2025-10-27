Descripción
	I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? You can download the challenge files here:
	- [challenge.zip](https://artifacts.picoctf.net/c_atlas/16/challenge.zip)
	The same files are accessible via SSH here: `ssh -p 59226 ctf-player@atlas.picoctf.net` Using the password `6abf4a82`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
	
Solución
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	challenge.zip
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ unzip challenge.zip 
	Archive:  challenge.zip
	   creating: home/ctf-player/drop-in/
	 extracting: home/ctf-player/drop-in/flag.png  
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	challenge.zip  home
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ cd home     
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/home]
	└─$ ls
	ctf-player
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/home]
	└─$ cd ctf-player 
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/home/ctf-player]
	└─$ ls
	drop-in
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/home/ctf-player]
	└─$ cd drop-in   
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/home/ctf-player/drop-in]
	└─$ ls
	flag.png
	
	picoCTF{p33k_@_b00_7843f77c}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=ELPCHk2VUsk
	https://scanqr.org/