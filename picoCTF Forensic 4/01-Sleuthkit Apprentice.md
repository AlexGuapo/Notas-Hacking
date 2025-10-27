Descripción
	Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
	- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)
	
Solución
	
	┌──(root㉿vbox)-[/tmp]
	└─# wget https://artifacts.picoctf.net/c/137/disk.flag.img.gz
	--2025-10-26 19:08:32--  https://artifacts.picoctf.net/c/137/disk.flag.img.gz
	Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.26, ...
	Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[3.161.55.100]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 47534568 (45M) [application/octet-stream]
	Grabando a: «disk.flag.img.gz»
	
	disk.flag.img.gz             100%[==============================================>]  45.33M  14.9MB/s    en 3.0s    
	
	2025-10-26 19:08:36 (14.9 MB/s) - «disk.flag.img.gz» guardado [47534568/47534568]
	
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# gunzip disk.flag.img.gz 
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# file disk.flag.img 
	disk.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x82, start-CHS (0xc,223,20), end-CHS (0x16,111,25), startsector 206848, 153600 sectors; partition 3 : ID=0x83, start-CHS (0x16,111,26), end-CHS (0x26,62,24), startsector 360448, 253952 sectors
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# mmls disk.flag.img 
	DOS Partition Table
	Offset Sector: 0
	Units are in 512-byte sectors
	
	      Slot      Start        End          Length       Description
	000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
	001:  -------   0000000000   0000002047   0000002048   Unallocated
	002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
	003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
	004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# rm -r /tmp/foo  
	rm: no se puede borrar '/tmp/foo': Dispositivo o recurso ocupado
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# rm -r foo     
	rm: no se puede borrar 'foo': Dispositivo o recurso ocupado
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# rm -rf foo
	rm: no se puede borrar 'foo': Dispositivo o recurso ocupado
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# ls
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
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# rm -rf foo 
	rm: no se puede borrar 'foo': Dispositivo o recurso ocupado
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# cd foo  
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# la
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# ls
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# cd ..   
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# sudo mount disk.flag.img /tmp/foo -o offset=$((360448*512))
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp]
	└─# cd foo 
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# ls
	bin  boot  dev  etc  home  lib  lost+found  media  mnt  opt  proc  root  run  sbin  srv  swap  sys  tmp  usr  var
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# ls -alps
	total 40
	 1 drwxr-xr-x 22 root root  1024 sep 29  2021 ./
	 0 drwxrwxrwt 15 root root   380 oct 26 19:09 ../
	 3 drwxr-xr-x  2 root root  3072 sep 29  2021 bin/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 boot/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 dev/
	 3 drwxr-xr-x 27 root root  3072 sep 29  2021 etc/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 home/
	 1 drwxr-xr-x  9 root root  1024 sep 29  2021 lib/
	12 drwx------  2 root root 12288 sep 29  2021 lost+found/
	 1 drwxr-xr-x  5 root root  1024 sep 29  2021 media/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 mnt/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 opt/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 proc/
	 1 drwx------  3 root root  1024 sep 29  2021 root/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 run/
	 5 drwxr-xr-x  2 root root  5120 sep 29  2021 sbin/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 srv/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 swap/
	 1 drwxr-xr-x  2 root root  1024 sep 29  2021 sys/
	 1 drwxrwxrwt  4 root root  1024 sep 29  2021 tmp/
	 1 drwxr-xr-x  8 root root  1024 sep 29  2021 usr/
	 1 drwxr-xr-x 11 root root  1024 sep 29  2021 var/
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# ls -l home
	total 0
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# sudo su                                                    
	┌──(root㉿vbox)-[/tmp/foo]
	└─# cd root 
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root]
	└─# cd my_folder 
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root/my_folder]
	└─# ls
	flag.uni.txt
	                                                                                                                    
	┌──(root㉿vbox)-[/tmp/foo/root/my_folder]
	└─# cat flag.uni.txt 
	picoCTF{by73_5urf3r_adac6cb4}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=itZAJftRXJM
	