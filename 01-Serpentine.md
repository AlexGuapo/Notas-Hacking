Descripción
	Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/35/serpentine.py
	--2025-09-10 17:28:29--  https://artifacts.picoctf.net/c/35/serpentine.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.77, 3.170.131.33, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 2550 (2.5K) [application/octet-stream]
	Saving to: 'serpentine.py'
	
	serpentine.py                    100%[=======================================================>]   2.49K  --.-KB/s    in 0s      
	
	2025-09-10 17:28:29 (873 MB/s) - 'serpentine.py' saved [2550/2550]
	
	evilmachine69-picoctf@webshell:~$ python3 serpentine.py 
	
	    Y
	  .-^-.
	 /     \      .- ~ ~ -.
	()     ()    /   _ _   `.                     _ _ _
	 \_   _/    /  /     \   \                . ~  _ _  ~ .
	   | |     /  /       \   \             .' .~       ~-. `.
	   | |    /  /         )   )           /  /             `.`.
	   \ \_ _/  /         /   /           /  /                `'
	    \_ _ _.'         /   /           (  (
	                    /   /             \  \
	                   /   /               \  \
	                  /   /                 )  )
	                 (   (                 /  /
	                  `.  `.             .'  /
	                    `.   ~ - - - - ~   .'
	                       ~ . _ _ _ _ . ~
	
	Welcome to the serpentine encourager!
	
	
	a) Print encouragement
	b) Print flag
	c) Quit
	
	What would you like to do? (a/b/c) b
	
	Oops! I must have misplaced the print_flag function! Check my source code!
	
	
	a) Print encouragement
	b) Print flag
	c) Quit
	
	What would you like to do? (a/b/c) c
	evilmachine69-picoctf@webshell:~$ nano serpentine.py 
	evilmachine69-picoctf@webshell:~$ python3 serpentine.py 
	picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
	
Notas adicionales
	
	
Referencias
	
	