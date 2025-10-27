Descripción
	Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory. [Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz) Access checker program: `nc saturn.picoctf.net 61339`
	
Solución
	
	┌──(gibran㉿vbox)-[/tmp]
	└─$ wget https://artifacts.picoctf.net/c/164/disk.img.gz     
	--2025-10-26 19:21:43--  https://artifacts.picoctf.net/c/164/disk.img.gz
	Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.61, ...
	Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[3.161.55.100]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 29714372 (28M) [application/octet-stream]
	Grabando a: «disk.img.gz»
	
	disk.img.gz                  100%[==============================================>]  28.34M  18.1MB/s    en 1.6s    
	
	2025-10-26 19:21:45 (18.1 MB/s) - «disk.img.gz» guardado [29714372/29714372]
	
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ ls
	config-err-Qx8nrs
	disk.img.gz
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
	└─$ gunzip disk.img.gz     
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ ls
	config-err-Qx8nrs
	disk.img
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
	└─$ mmsl disk.img 
	Orden «mmsl» no encontrada. Quizá quiso decir:
	  la orden «mmls» del paquete deb «sleuthkit»
	Pruebe con: sudo apt install <nombre del paquete deb>
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ mmls disk.img     
	DOS Partition Table
	Offset Sector: 0
	Units are in 512-byte sectors
	
	      Slot      Start        End          Length       Description
	000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
	001:  -------   0000000000   0000002047   0000002048   Unallocated
	002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
	                                                                                                                    
	┌──(gibran㉿vbox)-[/tmp]
	└─$ nc saturn.picoctf.net 61339
	What is the size of the Linux partition in the given disk image?
	Length in sectors: 0000202752
	0000202752
	Great work!
	picoCTF{mm15_f7w!}
	
Notas adicionales
	
	
Referencias
	https://www.youtube.com/watch?v=-5LFcTON8No
	