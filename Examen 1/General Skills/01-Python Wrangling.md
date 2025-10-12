Descripción
	Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py) using [this password](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/pw.txt) to get [the flag](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/flag.txt.en)?
	
Solución

		PS C:\Users\greye\OneDrive\Documentos\7mo Semestre\Seguridad en Redes> pip install cryptography
	Defaulting to user installation because normal site-packages is not writeable
	Collecting cryptography
	  Downloading cryptography-46.0.2-cp311-abi3-win_amd64.whl.metadata (5.7 kB)
	Collecting cffi>=2.0.0 (from cryptography)
	  Downloading cffi-2.0.0-cp312-cp312-win_amd64.whl.metadata (2.6 kB)
	Collecting pycparser (from cffi>=2.0.0->cryptography)
	  Downloading pycparser-2.23-py3-none-any.whl.metadata (993 bytes)
	Downloading cryptography-46.0.2-cp311-abi3-win_amd64.whl (3.5 MB)
	   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.5/3.5 MB 26.0 MB/s eta 0:00:00
	Downloading cffi-2.0.0-cp312-cp312-win_amd64.whl (183 kB)
	Downloading pycparser-2.23-py3-none-any.whl (118 kB)
	Installing collected packages: pycparser, cffi, cryptography
	Successfully installed cffi-2.0.0 cryptography-46.0.2 pycparser-2.23
	
	[notice] A new release of pip is available: 25.0.1 -> 25.2
	[notice] To update, run: C:\Users\greye\AppData\Local\Microsoft\WindowsApps\PythonSoftwareFoundation.Python.3.12_qbz5n2kfra8p0\python.exe -m pip install --upgrade pip
	PS C:\Users\greye\OneDrive\Documentos\7mo Semestre\Seguridad en Redes> python .\ende.py -d .\flag.txt.en
	Please enter the password:6008014f6008014f6008014f6008014f
	picoCTF{4p0110_1n_7h3_h0us3_6008014f}
	
Notas adicionales
	
	
Referencias
	
	