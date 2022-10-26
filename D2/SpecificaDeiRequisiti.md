# Documento di specifica dei requisiti

### TODO: indice elementi

### TODO: scopo del documento


##  <ins> **Use Cases** </ins>





##  <ins> **Attore: Utente Non Autenticato** </ins>
![alt text](/Images/UtenteNonAutenticato.png "Use case Diagram")

## **1. Registrarsi al sito**
![image not found](/Images/RegistrarsiSito.png "Use case Diagram")

**Titolo**
Registrarsi al sito.

**Riassunto**
Questo use case descrive la registrazione al sito da parte di un utente anonimo.

**Descrizione**
1.	L’utente sceglie uno username alfanumerico [EXCEPTION 1-2].
2.	L’utente sceglie una password alfanumerica [EXCEPTION 3].
3.	L'utente inserisce una propria mail valida [EXCEPTION 4].
    
**Exceptions**
1.	Se lo username scelto è già stato usato da un altro utente, verrà chiesto di scegliere uno nuovo username.
2.	Se lo username scelto contiene meno di 4 e/o più di 16 caratteri, verrà chiesto di scegliere uno nuovo username.
3.	Se la password scelta contiene meno di 6 e/o più di 12 caratteri, verrà chiesto di scegliere una nuova password.
4.	Se la mail inserita non contiene almeno un carattere '@' ed almeno un carattere '.' tra i caratteri che seguono '@', verrà chiesto di inserire una mail valida.

## **2. Accedere al sito**
![image not found](/Images/AccedereSito.png "Use case Diagram")

**Titolo**
Accedere al sito.

**Riassunto**
Questo use case descrive l’accesso al sito di un utente anonimo precedentemente registrato.

**Descrizione**
1.	L’utente inserisce il proprio username [EXCEPTION 1].
2.	L’utente inserisce la propria password [EXCEPTION 2].
    
**Exceptions**
1.	Se lo username inserito non appartiene ad alcun utente, verrà chiesto di riprovare inserendo uno username esistente.
2.	Se la password inserita non è corretta, verrà chiesto di riprovare inserendo una nuova password.

## **1. Ricerca viaggio**
![image not found](Images/RicercaViaggio.png "Use case Diagram")

**titolo**
Ricerca viaggi.

**Riassunto**
Questo use case descrive la ricerca di specifici viaggi da parte dell'utente non autenticato

**Descrizione**
1. All'utente viene presentata una barra di ricerca.
1. L'utente inserisce il titolo del viaggio desiderato o il luogo in cui si svolge.
1. L'utente seleziona da un menù a tendina la lunghezza del viaggio, da una serie di range di lunghezze predefiniti.
1. All'utente vengono mostrate le preview [EXTENSION 1] dei risultati della ricerca [EXCEPTION 1].
1. L'utente puà selezionare uno dei risultati per visualizzare il post completo.

**Exception**
1.	In caso la ricerca non producesse risultati pertinenti il sito mostra il seguente messaggio di errore: “Nessun risultato”.

Extensions
1.	La preview comprende:
    a.	Titolo viaggio;
    b.  Fotografia;
    c.	Nome utente che l’ha pubblicata;
    d.	Descrizione (se presente).

## **2. Visualizzazione viaggi consigliati**
![image not found](/Images/VisualizzazioneViaggiConsigliati.png "Use case Diagram")

**titolo**
Visualizzazione viaggi consigliati.

**Riassunto**
Questo use case descrive la presentazione di post consigliati all'utente non autenticato

**Descrizione**
1. L’utente accede alla pagina del sito chiamata "Luoghi".
1. Il sito mostra una preview [EXTENSION 1] di 10 viaggi selezionati casualmente dal database.
1. Selezionando uno di questi viene presentato l'intero viaggio nel dettaglio.


Extensions
1.	La preview comprende:
    a.	Titolo viaggio;
    b.  Fotografia;
    c.	Nome utente che l’ha pubblicata;
    d.	Descrizione (se presente).







##  <ins> **Attore: Utente  Autenticato** </ins>
![alt text](/Images/UtenteAutenticato.png "Use case Diagram")
## **1. Gestione Profilo**
![alt text](/Images/GestioneProfilo.png "Use case Diagram")

**Titolo**
Gestione profilo.

**Riassunto**
Questo use case descrive la gestione del profilo di un utente registrato.

**Descrizione**
1.	L’utente ha la possibilità di cambiare la propria password. Ciò avviene:
    1. Inserendo la password attuale [EXCEPTION 1];
    2. Inserendo la nuova password desiderata [EXCEPTION 2];
    3. Inserendo una seconda volta la nuova password, in modo da verificarne la correttezza [EXCEPTION 3].
2.	L'utente ha la possibilità di cambiare la propria email. Ciò avviene andando a specificare in un apposito campo la nuova email che si desidera utilizzare [EXCEPTION 4].
3.	L'utente ha la possibilità di eliminare il proprio profilo. Per confermare l'eliminazione verrà chiesto all'utente di inserire la propria password [EXCEPTION 1].
    
**Exceptions**
1.	Se la password inserita non corrisponde alla password attuale, verrà chiesto all’utente di riprovare inserendo la password corretta.
2.	Se la password scelta contiene meno di 6 e/o più di 12 caratteri, verrà chiesto di scegliere una nuova password.
3.	Se la password inserita non coincide con quella del punto 2, verrà comunicata la non coincidenza delle due password e verrà chiesto di riprovare.
4.	Se la mail inserita non contiene almeno un carattere '@' ed almeno un carattere '.' tra i caratteri che seguono '@', verrà chiesto di inserire una mail valida.


## **2. Ricerca viaggio**
![image not found](/Images/RicercaViaggioAutenticato.png "Use case Diagram")

**titolo**
Ricerca viaggi.

**Riassunto**
Questo use case descrive la ricerca di specifici viaggi da parte dell'utente autenticato

**Descrizione**
1. All'utente viene presentata una barra di ricerca.
1. L'utente inserisce il titolo del viaggio desiderato o il luogo in cui si svolge.
1. L'utente seleziona da un menù a tendina la lunghezza del viaggio, da una serie di range di lunghezze predefiniti.
1. All'utente vengono mostrate le preview [EXTENSION 1] dei risultati della ricerca [EXCEPTION 1].
1. L'utente puà selezionare uno dei risultati per visualizzare il post completo.
1. L'utente può decidere di seguire il profilo che ha postato il viaggio [EXTENSION 2]

**Exception**
1.	In caso la ricerca non producesse risultati pertinenti il sito mostra il seguente messaggio di errore: “Nessun risultato”.

Extensions
1.	La preview comprende:
    a.	Titolo viaggio;
    b.  Fotografia;
    c.	Nome utente che l’ha pubblicata;
    d.	Descrizione (se presente).
2.	L'utente sarà inserito nella lista follower del poster ed inizierà a visualizzare i suoi contenuti nella finestra "seguiti"



## **3. Visualizzazione viaggi consigliati**
![image not found](/Images/VisualizzazioneViaggiConsigliatiAutenticato.png "Use case Diagram")

**titolo**
Visualizzazione viaggi consigliati.

**Riassunto**
Questo use case descrive la presentazione di post consigliati all'utente autenticato

**Descrizione**
1. L’utente accede alla pagina del sito chiamata "Luoghi".
1. Il sito mostra una preview [EXTENSION 1] di 10 viaggi selezionati casualmente dal database.
1. Selezionando uno di questi viene presentato l'intero viaggio nel dettaglio.
1. L'utente può decidere di seguire il profilo che ha postato il viaggio [EXTENSION 2]


Extensions
1.	La preview comprende:
    a.	Titolo viaggio;
    b.  Fotografia;
    c.	Nome utente che l’ha pubblicata;
    d.	Descrizione (se presente).
2.	L'utente sarà inserito nella lista follower del poster ed inizierà a visualizzare i suoi contenuti nella finestra "seguiti"



## **4. Visualizzazione Profilo**
![alt text](/Images/VisualizzazioneProfilo.png "Use Case Diagram")

**Titolo** 
Visualizzazione Profilo.

**Riassunto**
Questo use case descrive come avviene la visualizzazione del profilo di un altro utente.

**Descrizione**
1.	L’Utente può accedere alla funzione di visualizzazione profilo in diversi modi:
    1.	Mentre visualizza i viaggi ricercati (cfr….) cliccando sull’username del proprietario;
    2.	Mentre visualizza i viaggi consigliati (cfr…) cliccando sull’username del proprietario;
    3.	Mentre visualizza i viaggi dei profili seguiti (cfr…) cliccando sull’username del proprietario;
    4.	Quando cerca i profili  degli utenti registrati (cfr..) cliccando su uno degli username dei risultati.


2.	Una volta che l’utente ha selezionato il bottone per visualizzare il profilo il sito mostra la foto dell’utente selezionato, lo username ed i viaggi pubblicati. [EXTENSION 1].

**Extensions**
1.	Se il profilo visualizzato è un profilo seguito dall’utente, viene visualizzata anche questa informazione.



## **4. Ricerca utenti registrati**
![alt text](/Images/RicercaUtentiRegistrati.png "Use case Diagram")

**Titolo**
Ricerca utenti registrati.

**Riassunto**
Questo use case descrive in che modo l’utente registrato può ricercare e visualizzare gli altri utenti registrati. 

**Descrizione**
1.	L’utente registrato accede alla pagina del sito “Seguiti”.
2.	Il sito mostra nella pagina una lista con le foto profilo degli utenti che segue ed una foto
con una “+”.
3.	L’utente clicca sulla “+”.
4.	Il sito mostra una tendina con una barra di ricerca.
5.	L’utente inserisce una stringa per ricercare l’username voluto e clicca sul tasto cerca.
6.	Il sito cerca e mostra gli username 5 utenti pertinenti [EXCEPTION 1].
7.	L’utente può visualizzare il profilo cliccando sull’username (CFR “Visualizzazione Profilo”).

**Exception**
1.	In caso la ricerca non producesse risultati pertinenti il sito mostra il seguente messaggio di errore: “Nessun risultato”.


## **5. Visualizzazione viaggi profili seguiti**
![alt text](/Images/VisualizzazioneViaggiProfiliSeguiti.png "Use case Diagram")

**Titolo**
Visualizzazione viaggi profili seguiti.

**Riassunto**
Questo use case descrive in che modo l’utente registrato visualizza i viaggi degli utenti che segue. 

**Descrizione**
1.	L’utente registrato accede alla pagina del sito “Seguiti”.
2.	Il sito mostra una preview [EXTENSION 1] dei 10 viaggi più recenti ricercati tra le pubblicazione amici.
3.	L’utente può ora effettuare 2 azioni:
I.	Visualizzare per intero uno o più viaggi presentati dal sito estendendo la preview;
II.	Visualizzare tutti i viaggi di un utente che segue [EXTENSION 2].

Extensions
1.	La preview comprende:
    a.	Titolo viaggio;
    b.	Nome utente che l’ha pubblicata;
    c.	Descrizione (se presente).
2.	Per visualizzare i viaggi di un utente nella parte superiore della pagina “Seguiti” ci sono le foto degli utenti seguiti, cliccandone una si accede alla funzione “Visualizzazione profilo” descritta nello Use case XXXXX.




## **6. Pubblicazione contenuti**
![alt text](/Images/PubblicazioneContenutius.png "Use Case Diagram")

**Titolo** 
Pubblicazione contenuti.

**Riassunto**
Questo use case descrive come avviene la pubblicazione di un contenuto da parte di un utente registrato.

**Descrizione**
1.	L’utente registrato accede alla pagina del sito chiamata “Crea”.

2.	Il sito mostra 4 Sezioni:
    1. Aggiunta titolo;
    2. Aggiunta descrizione generale;
    3. Selezione tappe;
    4. Mappa delle tappe.

3.	L’utente inserisce il nome del titolo del viaggio che sta creando [EXCEPTION 1].

4.	L’utente procede con la selezione delle tappe, in particolare [EXCEPTION 2]:
    1.	Sceglie la posizione (tramite API Google Maps), ciò comporta la creazione di una nuova tappa;
    2.	Aggiunge una foto (opzionale);
    3.	Aggiunge una descrizione (opzionale) [EXCEPTION 3].

5.	Terminata la creazione delle tappe l’utente conferma la creazione e pubblicazione del viaggio tramite apposito bottone.

**Exceptions**:
1.	Se il nome del titolo del viaggio supera i 80 caratteri viene visualizzato un messaggio d’errore e non è possibile pubblicare confermare la creazione del viaggio.
2.	Se l’utente seleziona meno di 2 tappe o più di 10 viene visualizzato un messaggio d’errore e non è possibile     pubblicare confermare la creazione del viaggio.
3.	Se il nome del titolo del viaggio supera i 1000 caratteri viene visualizzato un messaggio d’errore e non è possibile pubblicare confermare la creazione del viaggio.



![alt text](/Images/PubblicazioneContenuti.png "Use case Activity Diagram")






##  <ins> **Attore: Google Maps** </ins>
![alt text](/Images/GoogleMaps.png "Use case Diagram")
## **1. Creazione tappe viaggio**
![image not found](/Images/CreazioneTappeViaggio.png "Use case Diagram")

**titolo**
Creazione tappe viaggio.

**Riassunto**
Questo use case descrive l'interazione con l'API Google Maps di JavaScript per selezionare le tappe del viaggio

**Descrizione**
1. L'utente inserisce il nome o l'indirizzo del luogo desiderato.
1. Con l'API Google Maps viene ricercato il luogo in input [EXCEPTION 1].
1. L'utente seleziona uno tra i possibili risultati.
1. Con l'API Google Maps vengono esportate le informazioni del luogo in un file JSON.

**Exceptions**
1. Se la ricerca non produce risultati, l'utente viene allertato


## **2. Visualizzazione percorso**
![image not found](/Images/VisualizzazionePercorso.png "Use case Diagram")

**titolo**
Visualizzazione percorso.

**Riassunto**
Questo use case descrive l'interazione con l'API Google Maps di JavaScript per visualizzare il percorso del viaggio all'interno di un post

**Descrizione**
1. Con l'API Google Maps vengono importate le tappe dai file JSON del viaggio.
1. Con l'API Google Maps viene generata una mappa che mostri il luogo in cui si svolge il viaggio.
1. Con l'API Google Maps vengono aggiunte una ad una le tappe alla mappa.
1. Man mano che vengono aggiunte le tappe, vengono disegnate delle linee che le uniscono e che indicano sommariamente l'itinerario


##  <ins> **Attore: Database** </ins>
![alt text](/Images/Database.png "Use case Diagram")
## **2. Creazione Dati   **
![image not found](/Images/CreazioneDati.png "Use case Diagram")

**titolo**
Creazione Dati

**Riassunto**
Questo use case descrive quali sono gli elementi da inserire nel database necessari per implementare le funzioni descritte negli altri use case.

**Descrizione**
1. Quando l'utente non autenticato decide di registrarsi al sito tramite l'apposta funzione (cfr A1.U1) il database deve imagazzinare in modo corretto i dati dell'utente quali username, password, mail e foto profilo.
2. Quando l'utente autenticato pubblica un contentuto (cfr A2.U6) quest'ultimo dovrà essere immagazzinato nel database includendo nome del viaggio, descrizioni e le tappe.


## **2. Aggiornamento Dati   **
![image not found](/Images/AggiornamentoDati.png "Use case Diagram")

**titolo**
Aggiornamento Dati

**Riassunto**
Questo use case descrive quali sono gli elementi da aggiornare nel database a seguiti di azioni dell'utente descritte negli altri use case.

**Descrizione**
1. Quando l'utente non autenticato decide di modificare il proprio profilo (foto, mail o password) tramite l'apposta funzione (cfr A2.U??) il database deve aggiornare i dati cambiati.[EXTENSION 1]

**Extension**
1. Il ontrollo dell'integrità di questi dati non viene eseguito in questo use case bensì da quello che implementa la funzione di modifica profilo (cfr A2.U??).


## **3. Lettura Dati   **
![image not found](/Images/LatturaDati.png "Use case Diagram")

**titolo**
Lettura Dati

**Riassunto**
Questo use case descrive quali sono i dati da estrarre dal database per permettere all'utente di usufruire delle funzionalità descritte negli use case di cui sopra.

**Descrizione**
In particolare sarà richiesta la lettura di dati nei seguenti use case:
1. Visualizzazione viaggi consigliati utente non autenticato. (cfr A1.??).
2. Ricerca viaggio utente non autenticato. (cfr A1.??).
3. Accedere al sito.(cfr A1.??).
5. Ricerca viaggio utente autenticato. (cfr A2.??).
6. Visualizzazione profilo. (cfr A2.??).
7. Ricerca utenti registrati. (cfr A2.??).
8.  Visualizzazione viaggi profili seguiti. (cfr A2.??).
9.  Visualizzazione viaggi consigliati utente autenticato. (cfr A2.??).


## **4. Eliminazione Dati   **
![image not found](/Images/EliminazioneDati.png "Use case Diagram")

**titolo**
Eliminazione Dati

**Riassunto**
Questo use case descrive quali sono i dati da eliminare dal database a seguito di determinate azioni compiute dall'utente e descritte nei precedenti use case.

**Descrizione**
In particolare sarà richiesta l'eliminazione di dati quando l'utente autenticato decide di cancellare il proprio profilo. (cfr A2.??)