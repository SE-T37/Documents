# Documento di specifica dei requisiti

### TODO: indice elementi

### TODO: scopo del documento


##  <ins> **Use Cases** </ins>
## **USE CASE 1**
![alt text](PubblicazioneContenuti2.png "Use Case Diagram")

**Titolo** 
Pubblicazione contenuti

**Riassunto**
Questo use case descrive come avviene la pubblicazione di un contenuto da parte di un utente registrato.

**Descrizione**
1.	L’utente registrato accede alla pagina del sito “Crea”

2.	Il sito mostra 4 Sezioni:
    1. Aggiunta titolo;
    2. Aggiunta descrizione generale;
    3. Selezione tappe;Titolo: Pubblicazione contenuti
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



![alt text](PubblicazioneContenuti.png "Use case Activity Diagram")
