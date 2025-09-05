Descripción
	Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip)
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
	--2025-09-05 03:00:55--  https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
	Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
	Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 4520 (4.4K) [application/octet-stream]
	Saving to: 'Addadshashanammu.zip'
	
	Addadshashanammu.zip           100%[=================================================>]   4.41K  --.-KB/s    in 0s      
	
	2025-09-05 03:00:55 (1.46 GB/s) - 'Addadshashanammu.zip' saved [4520/4520]
	
	evilmachine69-picoctf@webshell:~$ unzip Addadshashanammu.zip 
	Archive:  Addadshashanammu.zip
	   creating: Addadshashanammu/
	   creating: Addadshashanammu/Almurbalarammi/
	   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
	   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
	   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
	   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
	   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
	  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
	evilmachine69-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
	evilmachine69-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis
	/Ularradallaku$ ls
	fang-of-haynekhtnamet
	evilmachine69-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis
	/Ularradallaku$ ./fang-of-haynekhtnamet 
	*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}
	
Notas adicionales
	
	
Referencias
	
	