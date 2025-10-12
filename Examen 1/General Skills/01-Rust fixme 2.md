Descripción
	The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).
	
Solución
	
	┌──(kali㉿DESKTOP-B014NUV)-[~/fixme2]
	└─$ cd src/
	
	┌──(kali㉿DESKTOP-B014NUV)-[~/fixme2/src]
	└─$ nano main.rs
	
	
	
	┌──(kali㉿DESKTOP-B014NUV)-[~/fixme2/src]
	└─$ cargo build
	   Compiling rust_proj v0.1.0 (/home/kali/fixme2)
	    Finished `dev` profile [unoptimized + debuginfo] target(s) in 1.55s
	
	┌──(kali㉿DESKTOP-B014NUV)-[~/fixme2/src]
	└─$ cargo run
	    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.01s
	     Running `/home/kali/fixme2/target/debug/rust_proj`
	Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}
	
Notas adicionales
	
	
Referencias
	
	