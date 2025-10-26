Descripción
	We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls   
	capture.pcap  picopico.key
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ssldump -r capture.pcap -k picopico.key -d > output
	Cleaned 4 remaining connection(s) from connection pool
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ nano output 
	
	picoCTF{honey.roasted.peanuts}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=5mX7YkKSAWg
	