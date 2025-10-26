Descripción
	I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/3944a59474f9f676942282c50b9c3675/Forensics%20is%20fun.pptm)
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ ls
	 1000.tar        capture.pcap  'Forensics is fun.pptm'   mystery        ports.txt   whitepages.txt
	 buildings.png   cookies.txt    garden.jpg               output         server.py
	 canvas.png      flag.txt       message.wav              pico_img.png   sstv                                                   
	 
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ cd macro
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro]
	└─$ ls
	'[Content_Types].xml'   docProps   ppt   _rels
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro]
	└─$ cd ppt  
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro/ppt]
	└─$ ls
	presentation.xml  _rels         slideMasters  tableStyles.xml  vbaProject.bin
	presProps.xml     slideLayouts  slides        theme            viewProps.xml
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro/ppt]
	└─$ cd slideMasters 
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro/ppt/slideMasters]
	└─$ ls
	hidden  _rels  slideMaster1.xml
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro/ppt/slideMasters]
	└─$ cat hidden     
	Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro/ppt/slideMasters]
	└─$ cat hidden | sed 's/ //'
	Zm x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro/ppt/slideMasters]
	└─$ cat hidden | sed 's/ //g'
	ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas/macro/ppt/slideMasters]
	└─$ cat hidden | sed 's/ //g' | base64 -d
	flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}  
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=c5mphZsRvKQ
	