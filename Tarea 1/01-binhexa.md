Descripción
	How well can you perfom basic binary operations?
	Additional details will be available after launching your challenge instance.
	
Solución
	
	┌──(kali㉿DESKTOP-B014NUV)-[~]
	└─$ nc titan.picoctf.net 54150
	
	Welcome to the Binary Challenge!"
	Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.
	
	Binary Number 1: 00010100
	Binary Number 2: 10001111
	
	
	Question 1/6:
	Operation 1: '<<'
	Perform a left shift of Binary Number 1 by 1 bits.
	Enter the binary result: 00101000
	Correct!
	
	Question 2/6:
	Operation 2: '>>'
	Perform a right shift of Binary Number 2 by 1 bits .
	Enter the binary result: 01000111
	Correct!
	
	Question 3/6:
	Operation 3: '&'
	Perform the operation on Binary Number 1&2.
	Enter the binary result: 0100
	Correct!
	
	Question 4/6:
	Operation 4: '*'
	Perform the operation on Binary Number 1&2.
	Enter the binary result: 101100101100
	Correct!
	
	Question 5/6:
	Operation 5: '|'
	Perform the operation on Binary Number 1&2.
	Enter the binary result: 00
	Incorrect. Try again
	Enter the binary result: 10011111
	Correct!
	
	Question 6/6:
	Operation 6: '+'
	Perform the operation on Binary Number 1&2.
	Enter the binary result: 10100011
	Correct!
	
	Enter the results of the last operation in hexadecimal: A3
	
	Correct answer!
	The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}
	
Notas adicionales
	
	
Referencias
	Calculadora de windows
	
	