Descripción
	Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:34561/](http://mercury.picoctf.net:34561/)
	
Solución
	En terminal de linux:
	
	┌──(gibran㉿vbox)-[~]
	└─$ curl -I http://mercury.picoctf.net:34561/
	HTTP/1.1 200 OK
	flag: picoCTF{r3j3ct_th3_du4l1ty_8f878508}
	Content-type: text/html; charset=UTF-8

	
Notas adicionales
	Se uso el comando curl para conectar con una pagina web
	
Referencias
	
	