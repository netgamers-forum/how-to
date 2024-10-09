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
   
   (sostituire [username] con il proprio user name (la parte prima del @ - per esempio daniele@ldp-2353 lo username è daniele)

6. Aprire terminal ed eseguire (ora il copia incolla dovrebbe funzionare)
   
   `sudo apt install build-essential dkms`
   

7. Lasciar completare, poi da dispositivi, premere su “Inserisci immagine CD Guests Additions…”

8. Sulla barra a sinistra, premere sull’icona del cd

9. Cliccare su **autorun.sh** e fare “esegui come programma”, lasciar eseguire fino a termine.

10. Copiate il contenuto di [questo link](https://raw.githubusercontent.com/DanieleMancini/install-rails/main/linux)
    
    aprite un file di testo incollate e salvate come nomefile.sh (magari nel desktop).
    
    adesso tasto destro sul file —> proprietà —> attivate il toggle “eseguire come programma”
       
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




























