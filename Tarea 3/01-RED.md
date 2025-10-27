Descripción
	RED, RED, RED, RED Download the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ file red.png      
	red.png: PNG image data, 128 x 128, 8-bit/color RGBA, non-interlaced
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ strings red.png                         
	IHDR
	tEXtPoem
	Crimson heart, vibrant and bold,
	Hearts flutter at your sight.
	Evenings glow softly red,
	Cherries burst with sweet life.
	Kisses linger with your warmth.
	Love deep as merlot.
	Scarlet leaves falling softly,
	Bold in every stroke.x
	IDATx
	IEND
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ zsteg red.png     
	meta Poem           .. text: "Crimson heart, vibrant and bold,\nHearts flutter at your sight.\nEvenings glow softly red,\nCherries burst with sweet life.\nKisses linger with your warmth.\nLove deep as merlot.\nScarlet leaves falling softly,\nBold in every stroke."
	b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="
	b1,rgba,msb,xy      .. file: OpenPGP Public Key
	b2,g,lsb,xy         .. text: "ET@UETPETUUT@TUUTD@PDUDDDPE"
	b2,rgb,lsb,xy       .. file: OpenPGP Secret Key
	b2,bgr,msb,xy       .. file: OpenPGP Public Key
	b2,rgba,lsb,xy      .. file: OpenPGP Secret Key
	b2,rgba,msb,xy      .. text: "CIkiiiII"
	b2,abgr,lsb,xy      .. file: OpenPGP Secret Key
	b2,abgr,msb,xy      .. text: "iiiaakikk"
	b3,rgba,msb,xy      .. text: "#wb#wp#7p"
	b3,abgr,msb,xy      .. text: "7r'wb#7p"
	b4,b,lsb,xy         .. file: 0421 Alliant compact executable not stripped
	                                                                                                                   
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ echo "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==" | base64 -d           
	picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}  
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=V2sAVn0MM5E
	