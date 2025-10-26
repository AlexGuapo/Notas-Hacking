Descripción
	This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.
	
Solución
	
	┌──(gibran㉿vbox)-[~]
	└─$ cd Descargas 
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	cookies.txt  garden.jpg  server.py
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ strings garden.jpg | grep -oE picoCTF{.*}
	picoCTF{more_than_m33ts_the_3y3657BaB2C}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=nPa7DJOwyKs
	