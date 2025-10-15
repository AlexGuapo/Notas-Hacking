Descripción
	I don't like scrolling down to read the code of my website, so I've squished it. As a bonus, my pages load faster! Browse [here](http://titan.picoctf.net:57999/), and find the flag!
	
Solución
	
	El sitio tenía un link a un archivo llamado about.html, este sitio tenía la línea:
	
	 <section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMWY4MzI2MTV9">
	
	Al pasarle esa cadena a la página cyberchef , me dio la llave:
	picoCTF{pr3tty_c0d3_b99eb82e}
	
Notas adicionales
	
	
Referencias
	
	