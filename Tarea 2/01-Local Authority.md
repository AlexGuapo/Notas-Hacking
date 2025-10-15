Descripción
	Can you get the flag? Go to this [website](http://saturn.picoctf.net:53109/) and see what you can discover.
	
Solución
	
	|   |
	|---|
	|<!DOCTYPE html>|
	|<html lang="en">|
	|<head>|
	|<meta charset="UTF-8">|
	|<meta name="viewport" content="width=device-width, initial-scale=1.0">|
	|<meta http-equiv="X-UA-Compatible" content="ie=edge">|
	|<link rel="stylesheet" href="[style.css](http://saturn.picoctf.net:53109/style.css)">|
	|<title>Secure Customer Portal</title>|
	|</head>|
	|<body>|
	||
	|<h1>Secure Customer Portal</h1>|
	||
	|<p>Only letters and numbers allowed for username and password.</p>|
	||
	|<form role="form" action="login.php" method="post">|
	|<input type="text" name="username" placeholder="Username" required|
	|autofocus></br>|
	|<input type="password" name="password" placeholder="Password" required>|
	|<button type="submit" name="login">Login</button>|
	|</form>|
	|</body>|
	|</html>|
	||
	
	entrar al link del style.css y cambiar la ultima ruta por secure.js y da los datos del login:
	  
	function checkPassword(username, password)
	{
	  if( username === 'admin' && password === 'strongPassword098765' )
	  {
	    return true;
	  }
	  else
	  {
	    return false;
	  }
	}
	
	loguearse y da la bandera:
	picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}
	
Notas adicionales
	
	
Referencias
	
	