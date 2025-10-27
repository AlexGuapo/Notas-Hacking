Descripción
	Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/257/flag.png).
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	flag.png
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ binwalk flag.png 
	
	DECIMAL       HEXADECIMAL     DESCRIPTION
	--------------------------------------------------------------------------------
	0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
	41            0x29            Zlib compressed data, compressed
	39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
	39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2959, uncompressed size: 3108, name: secret/flag.png
	42998         0xA7F6          End of Zip archive, footer length: 22
	
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ binwalk -e flag.png
	
	DECIMAL       HEXADECIMAL     DESCRIPTION
	--------------------------------------------------------------------------------
	41            0x29            Zlib compressed data, compressed
	39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
	39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2959, uncompressed size: 3108, name: secret/flag.png
	
	WARNING: One or more files failed to extract: either no utility was found or it's unimplemented
	
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	flag.png  _flag.png.extracted
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ cd _flag.png.extracted 
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/_flag.png.extracted]
	└─$ ls
	29  29.zlib  9B3B.zip  secret
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/_flag.png.extracted]
	└─$ cd secret             
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/_flag.png.extracted/secret]
	└─$ ls
	flag.png
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas/_flag.png.extracted/secret]
	└─$ open flag.png  
	
	picoCTF{Hiddinng_An_imag3_within_@n_ima9e_dc2ab58f}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=ctaIPMcbAXg
	