Descripción
	This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	capture.pcap  cookies.txt  flag.txt  garden.jpg  pico_img.png  server.py
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ file flag.txt                                        
	flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ eog flag.txt
	
	En imagen:
	picoCTF{now_you_know_about_extensions}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=sGjhB2vi_Fo
	
	