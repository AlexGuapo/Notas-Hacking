Descripción
	Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
	
Solución
	
	┌──(kali㉿DESKTOP-B014NUV)-[~]
	└─$ tar -xvzf fixme1.tar.gz
	fixme1/
	fixme1/Cargo.toml
	fixme1/Cargo.lock
	fixme1/src/
	fixme1/src/main.rs
	
	┌──(kali㉿DESKTOP-B014NUV)-[~]
	└─$ cd fixme1/
	
	┌──(kali㉿DESKTOP-B014NUV)-[~/fixme1]
	└─$ cd src
	
	┌──(kali㉿DESKTOP-B014NUV)-[~/fixme1/src]
	└─$ nano main.rs
	
	┌──(kali㉿DESKTOP-B014NUV)-[~/fixme1/src]
	└─$ cargo run
	   Compiling rust_proj v0.1.0 (/home/kali/fixme1)
	    Finished `dev` profile [unoptimized + debuginfo] target(s) in 1.48s
	     Running `/home/kali/fixme1/target/debug/rust_proj`
	picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}:?
	
Notas adicionales
	
	
Referencias
	
	