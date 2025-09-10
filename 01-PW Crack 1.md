Descripción
	Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py
	--2025-09-10 17:04:31--  https://artifacts.picoctf.net/c/11/level1.py
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.72, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 876 [application/octet-stream]
	Saving to: 'level1.py'
	
	level1.py                        100%[=======================================================>]     876  --.-KB/s    in 0s      
	
	2025-09-10 17:04:31 (9.62 MB/s) - 'level1.py' saved [876/876]
	
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
	--2025-09-10 17:04:44--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.33, 3.170.131.77, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 30 [application/octet-stream]
	Saving to: 'level1.flag.txt.enc'
	
	level1.flag.txt.enc              100%[=======================================================>]      30  --.-KB/s    in 0s      
	
	2025-09-10 17:04:44 (12.4 MB/s) - 'level1.flag.txt.enc' saved [30/30]
	
	evilmachine69-picoctf@webshell:~$ python3 level1.py 
	Please enter correct password for flag: 
	That password is incorrect
	evilmachine69-picoctf@webshell:~$ cat level1.py
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
	
	
	flag_enc = open('level1.flag.txt.enc', 'rb').read()
	
	
	
	def level_1_pw_check():
	    user_pw = input("Please enter correct password for flag: ")
	    if( user_pw == "1e1a"):
	        print("Welcome back... your flag, user:")
	        decryption = str_xor(flag_enc.decode(), user_pw)
	        print(decryption)
	        return
	    print("That password is incorrect")
	
	
	
	level_1_pw_check()
	evilmachine69-picoctf@webshell:~$ python3 level1.py 
	Please enter correct password for flag: 1e1a
	Welcome back... your flag, user:
	picoCTF{545h_r1ng1ng_fa343060}
	
Notas adicionales
	
	
Referencias
	
	