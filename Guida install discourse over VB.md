1. Installare ubuntu 22.04 su Virtualbox spuntando però l'opzione per **NON** fare una "unattended installation"
   
   [How to run an Ubuntu Desktop virtual machine using VirtualBox 7 | Ubuntu](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview)

2. Errore di mancanza di dipendenze per virtualbox di python in fase di installazione?
   
   - [Download Python | Python.org](https://www.python.org/downloads/)
   
   - Aprire terminal/powershell  
     
     `py -m pip install pywin32`  
     `python.exe -m pip install --upgrade pip`
     

3. Nella finestra di VB, sotto dispositivi, attivare appunti condivisi e trascinamento e rilascio, per poter copiare da e per la vm

4. Riavviare la vm

5. Assicuriamoci che il nostro user sia nella lista dei sudoers: apriamo un terminale (Ctrl+Alt+T) e digitiamo:
   
   
   `su -`
   
   
   ti verra richiesta la password root che in questo caso è la stessa dell utente creato in fase di installazione con virtualbox (in caso non vada provate con `sudo -i`)
   
   una volta inserita la password digitiamo:
   
   
   `sudo adduser [username] sudo` 
   
   (sostituire [username] con il proprio user name)
   
   ![](data:image/png;base64,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) nel mio caso “daniele”

6. Aprire terminal ed eseguire (ora il copia incolla dovrebbe funzionare)
   
   `sudo apt install build-essential dkms`
   

7. Lasciar completare, poi da dispositivi, premere su “Inserisci immagine CD Guests Additions…”

8. Sulla barra a sinistra, premere sull’icona del cd

9. Cliccare su **autorun.sh** e fare “esegui come programma”, lasciar eseguire fino a termine.

10. Copiate il contenuto di [https://raw.githubusercontent.com/DanieleMancini/install-rails/main/linux](questo link)
    
    aprite un file di testo incollate e salvate come nomefile.sh (magari nel desktop).
    
    adesso tasto destro sul file —> proprietà —> attivate il toggle “eseguire come programma”
    
    ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAbQAAAA7CAYAAAATpX//AAAO3klEQVR4Xu2dB4wUVRjH3ylFkKaCBUjQOyyJgmABgxFiBKQYRYmdZjBUe4wYsYIQQUMRAcUGNsBeolICKETUCEpR7B2UYkMBQe84+b3krcOwu7M7O3O7t/lPQlZvZ95883uz7z9feW9KysrKKo02ERABERABEaiGBCoqKsx+++1n/5W0a9dOglYNO1Emi4AIiIAIGLN582YJmm4EERABERCB6k9Aglb9+1BXIAIiIAIisIeABE23gQiIgAiIQFEQkKAVRTfqIkRABERABCRougdEQAREQASKgoAErSi6URchAiIgAiIgQdM9IAIiIAIiUBQEJGhF0Y26CBEQAREQAQma7gEREAEREIGiICBBK4pu1EWIgAiIgAhI0HQPiIAIiIAIFAUBCVpRdKMuQgREQAREQIKme0AEREAERKAoCEjQiqIbdREiIAIikDmB2rVrmzp16hg+a9asaVeoj3PbvXu3+ffff82uXbvM33//bT/j2CRocVBVmyIgAiJQgAQQsQYNGphatWplZF1JSUlG+2W7E4L2559/WnGLcpOgRUlTbYmACIhAgRI4+OCDzYEHHmitq1u3rmnVqpXZ81Jnc8QRR5h69erZv2/bts38/PPP5uuvvzZr1641O3bssH+PS9g432+//RYZMQlaZCjVkAiIgAgUHgHCiY0bN7bhxcrKSnPWWWeZM844IyNDly1bZhYtWpQQtDiEDW9ty5YthrBkrpsELVeCOl4EREAECpjAoYceasWsSZMm5vzzz7ceWTYbHttLL71kRScubw1R27RpUzZmJd1XgpYzQjUgAiIgAoVJ4KCDDrJhRkStX79+idBittYSGnziiSfsCzTx0uLw1KIIPxaloAH7vPPOM1u3bjVLlizJqO9wy4cOHWp++OEH89prr2V0jHYSAREQgUIlQAEIoUZCeUOGDMnaM/NfF57agw8+mKiIjEPU8AJzKRQpCkGrUaOGfXp4//33zeTJky3wWbNmmXfffddMmzYt6f3mP2b//fc3zzzzjFm8eLF56KGHCvUelV0iIAIikBEBvDKqGbPJmQU17M2pxSFouYYeMxY0jEcs2rdvv881T5061QpKvjYEbOzYsWb16tVm9uzZGQma/xgJWr56T+cVARGImgBChqBRzXjTTTdF2vz48eNt9WNcoUdyaWHnqWUtaICaPn36XoB++umnRMIwUnIhG8vEQ/M3LUELCVuHiYAIFByBhg0b2nzZaaedZrp37x6pfW+++aZ57733rOMQh5fG/LQ//vgjlM1ZC9rOnTuTKr7LW5F4PPzww83vv/9uw32vv/66NYwQ3xVXXGG6detmq20+++wzM3HiRPPpp5/a74FzySWXmN69e9vjeQL45ptvzIQJE+znyy+/bEOCTz/9tN2/adOmZu7cuea6664zH3300V4hRido7EccmfbIjc2YMcO89dZbifN5w5LJBC3IZi9xznn55Zdb+w855BCbPL3rrrvMmjVr7LXBhQoj5oJ8+eWXls2KFSsStnAdp59+un2qYvvwww+trT179jRHH320nR8yZ84c89RTT9nS20yYOvs4/9VXX21LdQ877DAbU//4449taBX7HP8rr7zShidgy6z+++67z7zxxhuB9gf1H9ebqm2YDBo0yPAD5CZ+5ZVXzMMPP2xtxO5suYQ5BvvT2RHql6WDRCCPBBhjWQGkb9++dvyIcuP3/OSTTyYELWpRyyXsGJmgMUFv5syZ5pFHHrHqzcCN64gYsV1zzTWmS5cuVsQ46YABA8yxxx5rRWz79u12UEMQHnvsMTuhj9LSW265xf5bvnx5KEHDm0QAsePss882Xbt2tXYgFn4vLpmgBdnsvUmw/9JLL7XXj0gjapzn119/tcUmF110kRUxePTo0cN07tzZ/n3dunUJWzZs2GCeffZZO5OfgZwnLETn22+/tWJ38cUXm2HDhplVq1ZlxNQraIj3xo0bzXPPPWcOOOAAc8EFF5g2bdqYwYMHm88//zxhA31D2BYePASQCA6yn/Ok6z/i7pw/WdvcN7D666+/zCmnnGLtue2222wxj+ujbLiEOQb709kR5WCgtkQgbgI88DZr1sw++BJurF+/fqSn5LdK2JExIo6wIw+z69evD2Vz1oLmz6Exy/vcc881rVu3tjk2Blz31O8sYoDGw7r33nsN7iobnsLzzz9vRowYYffnezwuns7ZKDd99dVXza233hpa0LxFIQx0iA2DOiIZJGhBNiOybuOGYZ4GeUR/LjHZd9wIjz76qO00ri9ZiLRPnz726eqcc86x3hLijPeCl4Y4ZGNfsvZpjweQL774wtx5550p846Z2I/wpus/J2jpinRgiZ2PP/64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)
    
    adesso ancora tasto destro e “esegui come programma”
    
    se non dovesse funzionare, click destro sul desktop “open in terminal” e poi `./nomefile.sh`
    
    si aprira un terminale e inizierà l'installazione - lasciate runnare.

11. Ora se tutto è andato bene cloniamo il repository di discourse
    
    sempre da terminale:
    `git clone https://github.com/discourse/discourse.git ~/discourse`
    
    **quando avrà terminato** digitiamo in sequenza:
    
    `cd ~/discourse`
    
    `source ~/.bashrc`
    
    `bundle install`
    
    `yarn install --network-timeout 600000`
    
    `bin/rails db:create` 
    
    `bin/rails db:migrate`
    
    `RAILS_ENV=test bin/rails db:create db:migrate`

12. Startiano il server con:
    
    `bin/ember-cli -u`
    
    ora dovresti poter aprire [http://localhost:4200/](http://localhost:4200/)

13. Ora non rimane che creare un account admin:
    da un altra finestra del terminale digitare 
    
    `cd ~/discourse`
    
    `bundle exec rake admin:create`
    
    seguite i prompt e avete fatto.




























