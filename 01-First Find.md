Descripción
	Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)
	
Solución
	evilmachine69-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/502/files.zip
	--2025-09-05 03:25:43--  https://artifacts.picoctf.net/c/502/files.zip
	Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.77, 3.170.131.33, ...
	Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 3995553 (3.8M) [application/octet-stream]
	Saving to: 'files.zip'
	
	files.zip                  100%[========================================>]   3.81M  1.82MB/s    in 2.1s    
	
	2025-09-05 03:25:46 (1.82 MB/s) - 'files.zip' saved [3995553/3995553]
	
	evilmachine69-picoctf@webshell:~$ ls
	Addadshashanammu      big-zip-files      files.zip  retogrep                  static.ltdis.x86_64.txt
	Addadshashanammu.zip  big-zip-files.zip  flag       static                    strings
	README.txt            enc_flag           ltdis.sh   static.ltdis.strings.txt  warm
	evilmachine69-picoctf@webshell:~$ unzip files.zip 
	Archive:  files.zip
	   creating: files/
	   creating: files/satisfactory_books/
	   creating: files/satisfactory_books/more_books/
	  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
	  inflating: files/satisfactory_books/23765.txt.utf-8  
	  inflating: files/satisfactory_books/16021.txt.utf-8  
	  inflating: files/13771.txt.utf-8   
	   creating: files/adequate_books/
	   creating: files/adequate_books/more_books/
	   creating: files/adequate_books/more_books/.secret/
	   creating: files/adequate_books/more_books/.secret/deeper_secrets/
	   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
	 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
	  inflating: files/adequate_books/more_books/1023.txt.utf-8  
	  inflating: files/adequate_books/46804-0.txt  
	  inflating: files/adequate_books/44578.txt.utf-8  
	   creating: files/acceptable_books/
	   creating: files/acceptable_books/more_books/
	  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
	  inflating: files/acceptable_books/17880.txt.utf-8  
	  inflating: files/acceptable_books/17879.txt.utf-8  
	  inflating: files/14789.txt.utf-8   
	evilmachine69-picoctf@webshell:~$ ls
	Addadshashanammu      big-zip-files      files      ltdis.sh  static.ltdis.strings.txt  warm
	Addadshashanammu.zip  big-zip-files.zip  files.zip  retogrep  static.ltdis.x86_64.txt
	README.txt            enc_flag           flag       static    strings
	evilmachine69-picoctf@webshell:~$ cd files/
	evilmachine69-picoctf@webshell:~/files$ find . uber-secret.txt
	.
	./satisfactory_books
	./satisfactory_books/more_books
	./satisfactory_books/more_books/37121.txt.utf-8
	./satisfactory_books/23765.txt.utf-8
	./satisfactory_books/16021.txt.utf-8
	./13771.txt.utf-8
	./adequate_books
	./adequate_books/more_books
	./adequate_books/more_books/.secret
	./adequate_books/more_books/.secret/deeper_secrets
	./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets
	./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
	./adequate_books/more_books/1023.txt.utf-8
	./adequate_books/46804-0.txt
	./adequate_books/44578.txt.utf-8
	./acceptable_books
	./acceptable_books/more_books
	./acceptable_books/more_books/40723.txt.utf-8
	./acceptable_books/17880.txt.utf-8
	./acceptable_books/17879.txt.utf-8
	./14789.txt.utf-8
	find: 'uber-secret.txt': No such file or directory
	evilmachine69-picoctf@webshell:~/files$ cat ./adequate_books/more_books/.secret/deeper_secrets/uber-secret.txt
	cat: ./adequate_books/more_books/.secret/deeper_secrets/uber-secret.txt: No such file or directory
	evilmachine69-picoctf@webshell:~/files$ cat ./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
	picoCTF{f1nd_15_f457_ab443fd1}
	
Notas adicionales
	
	
Referencias
	
	