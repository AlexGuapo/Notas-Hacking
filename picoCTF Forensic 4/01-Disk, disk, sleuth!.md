Descripción
	Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz)
	
Solución
	
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ curl https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz >> dds1-alpine.flag.img.gz
	  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
	                                 Dload  Upload   Total   Spent    Left  Speed
	100 28.3M  100 28.3M    0     0  3274k      0  0:00:08  0:00:08 --:--:-- 2234k
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ gzip -d dds1-alpine.flag.img.gz                 
	
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ 
	                                                                                                                    
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ strings dds1-alpine.flag.img | grep pico           
	ffffffff81399ccf t pirq_pico_get
	ffffffff81399cee t pirq_pico_set
	ffffffff820adb46 t pico_router_probe
	  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_564ff1a0}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=HPv5oURNtWQ
	