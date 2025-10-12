Descripción
	Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 63495 ctf-player@saturn.picoctf.net`. The password is `af86add3`
	
Solución
	
	┌──(kali㉿DESKTOP-B014NUV)-[~]
	└─$ ssh -p 63495 ctf-player@saturn.picoctf.net
	ctf-player@saturn.picoctf.net's password:
	Specialer$
	!          ]]         break      command    coproc     done       esac       false      function   if         local      pushd      return     source     times      ulimit     wait
	./         alias      builtin    compgen    declare    echo       eval       fc         getopts    in         logout     pwd        select     suspend    trap       umask      while
	:          bash       caller     complete   dirs       elif       exec       fg         hash       jobs       mapfile    read       set        test       true       unalias    {
	[          bg         case       compopt    disown     else       exit       fi         help       kill       popd       readarray  shift      then       type       unset      }
	[[         bind       cd         continue   do         enable     export     for        history    let        printf     readonly   shopt      time       typeset    until
	Specialer$ cd
	.bash_history  .hushlogin     .profile       abra/          ala/           sim/
	Specialer$ cd ..
	Specialer$ cd ..
	Specialer$ cd ..
	Specialer$ cd ../..
	Specialer$
	!          ]]         break      command    coproc     done       esac       false      function   if         local      pushd      return     source     times      ulimit     wait
	./         alias      builtin    compgen    declare    echo       eval       fc         getopts    in         logout     pwd        select     suspend    trap       umask      while
	:          bash       caller     complete   dirs       elif       exec       fg         hash       jobs       mapfile    read       set        test       true       unalias    {
	[          bg         case       compopt    disown     else       exit       fi         help       kill       popd       readarray  shift      then       type       unset      }
	[[         bind       cd         continue   do         enable     export     for        history    let        printf     readonly   shopt      time       typeset    until
	Specialer$ cd
	bin/   home/  lib/   lib64/
	Specialer$ cd home/
	Specialer$
	!          ]]         break      command    coproc     done       esac       false      function   if         local      pushd      return     source     times      ulimit     wait
	./         alias      builtin    compgen    declare    echo       eval       fc         getopts    in         logout     pwd        select     suspend    trap       umask      while
	:          bash       caller     complete   dirs       elif       exec       fg         hash       jobs       mapfile    read       set        test       true       unalias    {
	[          bg         case       compopt    disown     else       exit       fi         help       kill       popd       readarray  shift      then       type       unset      }
	[[         bind       cd         continue   do         enable     export     for        history    let        printf     readonly   shopt      time       typeset    until
	Specialer$ cd ctf-player/
	Specialer$ cd
	.bash_history  .hushlogin     .profile       abra/          ala/           sim/
	Specialer$ cd abra/
	Specialer$ cd cada
	cadabra.txt   cadaniel.txt
	Specialer$ cd cada
	cadabra.txt   cadaniel.txt
	Specialer$ echo $(<cadaniel.txt)
	Yes, I did it! I really did it! I'm a true wizard!
	Specialer$ cd ..
	Specialer$ cd ala/
	Specialer$ cd
	kazam.txt  mode.txt
	Specialer$ echo $(<kazam.txt)
	return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_a8567b6f}
	
Notas adicionales
	
	
Referencias
	
	