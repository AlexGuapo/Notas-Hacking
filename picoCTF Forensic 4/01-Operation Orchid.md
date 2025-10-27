Descripción
	Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
	- [Download compressed disk image](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)
	
Solución
	
	┌──(gibran㉿vbox)-[/tmp]
	└─$ wget https://artifacts.picoctf.net/c/70/disk.img.gz
	--2025-10-26 18:49:08--  https://artifacts.picoctf.net/c/70/disk.img.gz
	Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.100, ...
	Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[3.161.55.61]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 48132743 (46M) [application/octet-stream]
	Grabando a: «disk.img.gz»
	
	disk.img.gz                  100%[==============================================>]  45.90M  8.19MB/s    en 4.7s    
	
	2025-10-26 18:49:14 (9.86 MB/s) - «disk.img.gz» guardado [48132743/48132743]
	
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ ls -la
	total 47020
	drwxrwxrwt 14 root   root        360 oct 26 18:49 .
	drwxr-xr-x 19 root   root       4096 sep  8 11:40 ..
	-rw-------  1 gibran gibran        0 oct 26 16:26 config-err-Qx8nrs
	-rw-rw-r--  1 gibran gibran 48132743 ago  4  2023 disk.img.gz
	drwxrwxrwt  2 root   root         40 oct 26 16:26 .font-unix
	drwxrwxrwt  2 root   root         60 oct 26 16:26 .ICE-unix
	drwx------  2 gibran gibran       60 oct 26 16:26 ssh-Kchkuw4Rs61C
	drwx------  3 root   root         60 oct 26 16:26 systemd-private-8e5e0205e02d46959183a380c5a3625e-colord.service-lByvTX
	drwx------  3 root   root         60 oct 26 16:26 systemd-private-8e5e0205e02d46959183a380c5a3625e-haveged.service-QHyWm5
	drwx------  3 root   root         60 oct 26 16:26 systemd-private-8e5e0205e02d46959183a380c5a3625e-ModemManager.service-AV2fNn
	drwx------  3 root   root         60 oct 26 16:26 systemd-private-8e5e0205e02d46959183a380c5a3625e-polkit.service-vdVJ66
	drwx------  3 root   root         60 oct 26 16:26 systemd-private-8e5e0205e02d46959183a380c5a3625e-systemd-logind.service-8ScP7A
	drwx------  3 root   root         60 oct 26 16:26 systemd-private-8e5e0205e02d46959183a380c5a3625e-upower.service-FUQyuE
	drwx------  2 gibran gibran       40 oct 26 16:27 Temp-b219822c-4489-4163-bd8c-1a5166b2bb0e
	-r--r--r--  1 root   root         11 oct 26 16:26 .X0-lock
	drwxrwxrwt  2 root   root         60 oct 26 16:26 .X11-unix
	-rw-------  1 gibran gibran      398 oct 26 16:26 .xfsm-ICE-D2GXE3
	drwxrwxrwt  2 root   root         40 oct 26 16:26 .XIM-unix
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ gzip -d disk.img.gz
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ mmls disk.img      
	DOS Partition Table
	Offset Sector: 0
	Units are in 512-byte sectors
	
	      Slot      Start        End          Length       Description
	000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
	001:  -------   0000000000   0000002047   0000002048   Unallocated
	002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
	003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ fls -o 471039 disk.img        
	Cannot determine file system type
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ ls    
	config-err-Qx8nrs
	disk.img
	ssh-Kchkuw4Rs61C
	systemd-private-8e5e0205e02d46959183a380c5a3625e-colord.service-lByvTX
	systemd-private-8e5e0205e02d46959183a380c5a3625e-haveged.service-QHyWm5
	systemd-private-8e5e0205e02d46959183a380c5a3625e-ModemManager.service-AV2fNn
	systemd-private-8e5e0205e02d46959183a380c5a3625e-polkit.service-vdVJ66
	systemd-private-8e5e0205e02d46959183a380c5a3625e-systemd-logind.service-8ScP7A
	systemd-private-8e5e0205e02d46959183a380c5a3625e-upower.service-FUQyuE
	Temp-b219822c-4489-4163-bd8c-1a5166b2bb0e
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ rm  disk.img 
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ ls
	config-err-Qx8nrs
	ssh-Kchkuw4Rs61C
	systemd-private-8e5e0205e02d46959183a380c5a3625e-colord.service-lByvTX
	systemd-private-8e5e0205e02d46959183a380c5a3625e-haveged.service-QHyWm5
	systemd-private-8e5e0205e02d46959183a380c5a3625e-ModemManager.service-AV2fNn
	systemd-private-8e5e0205e02d46959183a380c5a3625e-polkit.service-vdVJ66
	systemd-private-8e5e0205e02d46959183a380c5a3625e-systemd-logind.service-8ScP7A
	systemd-private-8e5e0205e02d46959183a380c5a3625e-upower.service-FUQyuE
	Temp-b219822c-4489-4163-bd8c-1a5166b2bb0e
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ wget https://artifacts.picoctf.net/c/214/disk.flag.img.gz
	--2025-10-26 18:54:51--  https://artifacts.picoctf.net/c/214/disk.flag.img.gz
	Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.61, ...
	Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[3.161.55.64]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 44360927 (42M) [application/octet-stream]
	Grabando a: «disk.flag.img.gz»
	
	disk.flag.img.gz             100%[==============================================>]  42.31M  15.8MB/s    en 2.7s    
	
	2025-10-26 18:54:54 (15.8 MB/s) - «disk.flag.img.gz» guardado [44360927/44360927]
	
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ ls
	config-err-Qx8nrs
	disk.flag.img.gz
	ssh-Kchkuw4Rs61C
	systemd-private-8e5e0205e02d46959183a380c5a3625e-colord.service-lByvTX
	systemd-private-8e5e0205e02d46959183a380c5a3625e-haveged.service-QHyWm5
	systemd-private-8e5e0205e02d46959183a380c5a3625e-ModemManager.service-AV2fNn
	systemd-private-8e5e0205e02d46959183a380c5a3625e-polkit.service-vdVJ66
	systemd-private-8e5e0205e02d46959183a380c5a3625e-systemd-logind.service-8ScP7A
	systemd-private-8e5e0205e02d46959183a380c5a3625e-upower.service-FUQyuE
	Temp-b219822c-4489-4163-bd8c-1a5166b2bb0e
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ gunzip disk.flag.img.gz 
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ file disk.flag.img    
	disk.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x82, start-CHS (0xc,223,20), end-CHS (0x19,159,6), startsector 206848, 204800 sectors; partition 3 : ID=0x83, start-CHS (0x19,159,7), end-CHS (0x32,253,11), startsector 411648, 407552 sectors
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ mmls disk.flag.img 
	DOS Partition Table
	Offset Sector: 0
	Units are in 512-byte sectors
	
	      Slot      Start        End          Length       Description
	000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
	001:  -------   0000000000   0000002047   0000002048   Unallocated
	002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
	003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
	004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ mkdir foo                                             
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ ls
	config-err-Qx8nrs
	disk.flag.img
	foo
	ssh-Kchkuw4Rs61C
	systemd-private-8e5e0205e02d46959183a380c5a3625e-colord.service-lByvTX
	systemd-private-8e5e0205e02d46959183a380c5a3625e-haveged.service-QHyWm5
	systemd-private-8e5e0205e02d46959183a380c5a3625e-ModemManager.service-AV2fNn
	systemd-private-8e5e0205e02d46959183a380c5a3625e-polkit.service-vdVJ66
	systemd-private-8e5e0205e02d46959183a380c5a3625e-systemd-logind.service-8ScP7A
	systemd-private-8e5e0205e02d46959183a380c5a3625e-upower.service-FUQyuE
	Temp-b219822c-4489-4163-bd8c-1a5166b2bb0e
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ sudo mount disk.flag.img                              
	[sudo] contraseña para gibran: 
	sudo: a password is required
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ sudo mount disk.flag.img /tmp/foo -o offset=$((411648*512))
	[sudo] contraseña para gibran: 
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ cd foo 
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp/foo]
	└─$ ls
	bin  boot  dev  etc  home  lib  lost+found  media  mnt  opt  proc  root  run  sbin  srv  swap  sys  tmp  usr  var
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp/foo]
	└─$ ls -alps
	total 40
	 1 drwxr-xr-x 22 root root  1024 oct  6  2021 ./
	 0 drwxrwxrwt 15 root root   380 oct 26 18:57 ../
	 3 drwxr-xr-x  2 root root  3072 oct  6  2021 bin/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 boot/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 dev/
	 3 drwxr-xr-x 27 root root  3072 oct  6  2021 etc/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 home/
	 1 drwxr-xr-x  9 root root  1024 oct  6  2021 lib/
	12 drwx------  2 root root 12288 oct  6  2021 lost+found/
	 1 drwxr-xr-x  5 root root  1024 oct  6  2021 media/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 mnt/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 opt/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 proc/
	 1 drwx------  2 root root  1024 oct  6  2021 root/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 run/
	 5 drwxr-xr-x  2 root root  5120 oct  6  2021 sbin/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 srv/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 swap/
	 1 drwxr-xr-x  2 root root  1024 oct  6  2021 sys/
	 1 drwxrwxrwt  4 root root  1024 oct  6  2021 tmp/
	 1 drwxr-xr-x  8 root root  1024 oct  6  2021 usr/
	 1 drwxr-xr-x 11 root root  1024 oct  6  2021 var/
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp/foo]
	└─$ sudo su                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# cd root 
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# la
	.ash_history  flag.txt.enc
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# ls -alps
	total 4
	1 drwx------  2 root root 1024 oct  6  2021 ./
	1 drwxr-xr-x 22 root root 1024 oct  6  2021 ../
	1 -rw-------  1 root root  202 oct  6  2021 .ash_history
	1 -rw-r--r--  1 root root   64 oct  6  2021 flag.txt.enc
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# cat .ash_history 
	touch flag.txt
	nano flag.txt 
	apk get nano
	apk --help
	apk add nano
	nano flag.txt 
	openssl
	openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
	shred -u flag.txt
	ls -al
	halt
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# file flag.txt.enc 
	flag.txt.enc: openssl enc'd data with salted password
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# openssl aes256 -d -in flag.txt.enc -out decrypt.tst
	enter AES-256-CBC decryption password:
	*** WARNING : deprecated key derivation used.
	Using -iter or -pbkdf2 would be better.
	bad decrypt
	40A72C1A307F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# openssl aes256 -d -in flag.txt.enc -out decrypt.tst
	enter AES-256-CBC decryption password:
	bad password read
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# ls      
	decrypt.tst  flag.txt.enc
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# cat decrypt.tst 
	picoCTF{h4un71ng_p457_1d02081e} 
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=XlBBTAZlPFQ
	