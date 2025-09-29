Descripción
	Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.py
	--2025-09-10 17:09:51--  https://artifacts.picoctf.net/c/13/level2.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.77, 3.170.131.18, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 914 [application/octet-stream]
	Saving to: 'level2.py'
	
	level2.py                        100%[=======================================================>]     914  --.-KB/s    in 0s      
	
	2025-09-10 17:09:51 (34.1 MB/s) - 'level2.py' saved [914/914]
	
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
	--2025-09-10 17:10:02--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.18, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 31 [application/octet-stream]
	Saving to: 'level2.flag.txt.enc'
	
	level2.flag.txt.enc              100%[=======================================================>]      31  --.-KB/s    in 0s      
	
	2025-09-10 17:10:02 (1.02 MB/s) - 'level2.flag.txt.enc' saved [31/31]
	
	evilmachine69-picoctf@webshell:~$ python3 level2.py 
	Please enter correct password for flag: 
	That password is incorrect
	evilmachine69-picoctf@webshell:~$ cat level2.py
	### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
	def str_xor(secret, key):
	    #extend key to secret length
	    new_key = key
	    i = 0
	    while len(new_key) < len(secret):
	        new_key = new_key + key[i]
	        i = (i + 1) % len(key)        
	    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
	###############################################################################
	
	flag_enc = open('level2.flag.txt.enc', 'rb').read()
	
	
	
	def level_2_pw_check():
	    user_pw = input("Please enter correct password for flag: ")
	    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
	        print("Welcome back... your flag, user:")
	        decryption = str_xor(flag_enc.decode(), user_pw)
	        print(decryption)
	        return
	    print("That password is incorrect")
	
	
	
	level_2_pw_check()
	evilmachine69-picoctf@webshell:~$ python3 level2.py 
	Please enter correct password for flag: de76
	Welcome back... your flag, user:
	picoCTF{tr45h_51ng1ng_489dea9a}
	
	Usando cyberchef: https://gchq.github.io/CyberChef/
	Imput:
	0x64
	0x65
	0x37
	0x36
	
	Recipe:
	    From Hex
	Output: de76
	
Notas adicionales
	
	
Referencias
	https://gchq.github.io/CyberChef/
	