Descripción
	We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ssldump -r capture.pcap -k picopico.key -d > output
	Cleaned 3 remaining connection(s) from connection pool
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls                
	capture.pcap  output  picopico.key
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ nano output   
	
	picoCTF{nongshim.shrimp.crackers}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=m73DxHLfBxE
	