Descripción
	Connect to this PostgreSQL server and find the flag! `psql -h saturn.picoctf.net -p 59313 -U postgres pico` Password is `postgres`
	
Solución
	
	┌──(gibran㉿vbox)-[~]
	└─$ psql -h saturn.picoctf.net -p 59313 -U postgres pico
	Contraseña para usuario postgres: 
	psql (17.5 (Debian 17.5-1), servidor 15.2 (Debian 15.2-1.pgdg110+1))
	Digite «help» para obtener ayuda.
	
	pico=# \dt
	        Listado de relaciones
	 Esquema | Nombre | Tipo  |  Dueño   
	---------+--------+-------+----------
	 public  | flags  | tabla | postgres
	(1 fila)
	
	pico=# select * from flags;
	 id | firstname | lastname  |                address                 
	----+-----------+-----------+----------------------------------------
	  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
	  2 | Leia      | Organa    | Alderaan
	  3 | Han       | Solo      | Corellia
	(3 filas)
	
Notas adicionales
	
	
Referencias
	
	