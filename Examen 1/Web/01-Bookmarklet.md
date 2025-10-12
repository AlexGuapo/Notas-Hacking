Descripción
	Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:49317/), and find the flag!
	
Solución
	
	        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÔÅÐÙí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    
	picoCTF{p@g3_turn3r_1d1ba7e0}
	
Notas adicionales
	
	
Referencias
	
	