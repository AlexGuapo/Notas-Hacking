Descripción
	Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg)
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	dolls.jpg
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ file dolls.jpg 
	dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ binwalk dolls.jpg
	
	DECIMAL       HEXADECIMAL     DESCRIPTION
	--------------------------------------------------------------------------------
	0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
	3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
	272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383938, name: base_images/2_c.jpg
	651612        0x9F15C         End of Zip archive, footer length: 22
	
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ unzip dolls.jpg
	Archive:  dolls.jpg
	warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
	  (attempting to process anyway)
	  inflating: base_images/2_c.jpg     
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ cd base_images 
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/base_images]
	└─$ binwalk 2_c.jpg  
	
	DECIMAL       HEXADECIMAL     DESCRIPTION
	--------------------------------------------------------------------------------
	0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
	3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
	187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196043, uncompressed size: 201445, name: base_images/3_c.jpg
	383805        0x5DB3D         End of Zip archive, footer length: 22
	383916        0x5DBAC         End of Zip archive, footer length: 22
	
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/base_images]
	└─$ cd ..         
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	base_images  dolls.jpg
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls      
	base_images  dolls.jpg
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ rm -rf base_images 
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ binwalk dolls.jpg 
	
	DECIMAL       HEXADECIMAL     DESCRIPTION
	--------------------------------------------------------------------------------
	0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
	3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
	272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383938, name: base_images/2_c.jpg
	651612        0x9F15C         End of Zip archive, footer length: 22
	
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ for i in {0..100}; do unzip *.jpg; cd base_images; done
	Archive:  dolls.jpg
	warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
	  (attempting to process anyway)
	  inflating: base_images/2_c.jpg     
	Archive:  2_c.jpg
	warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
	  (attempting to process anyway)
	  inflating: base_images/3_c.jpg     
	Archive:  3_c.jpg
	warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
	  (attempting to process anyway)
	  inflating: base_images/4_c.jpg     
	Archive:  4_c.jpg
	warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
	  (attempting to process anyway)
	  inflating: flag.txt                
	cd: no existe el fichero o el directorio: base_images
	Archive:  4_c.jpg
	warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
	  (attempting to process anyway)
	replace flag.txt? [y]es, [n]o, [A]ll, [N]one, [r]ename: ^Zzsh: suspended  unzip *.jpg
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/base_images/base_images/base_images]
	└─$ ls
	4_c.jpg  flag.txt
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/base_images/base_images/base_images]
	└─$ cat flag.txt                         
	picoCTF{bf6acf878dcbd752f4721e41b1b1b66b}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=A9i0XwmDYPU
	