## Indice contenuti
- Scopo del Documento
- Obiettivi del Progetto
- Requisiti Funzionali
- Requisiti Non funzionali



# Scopo del Documento

Lo scopo del presente documento è di riportare l’analisi dei requisiti del progetto “NomadBees”.
Nello specifico verranno esposti:
- Obiettivi e scopo del progetto
- Requisiti funzionali
- Design e mockup del Front-End
- Requisiti ed organizzazione del Back-End



# Obiettivi del Progetto

L’obiettivo di NomadBees è realizzare un sito che permetta di cercare e condividere viaggi con i propri amici e con gli altri utenti.  Si vuole creare una rete di persone che hanno in comune la passione per le escursioni. Il punto di forza di questo progetto è la sua visione: conoscere le persone attraverso le esperienze che hanno vissuto.

Nello specifico il sito avrà i seguenti obbiettivi:
    OB 1. Consentire ad un utente di registrarsi ed accendere al sito con le proprie credenziali
    OB 2. Poter cercare e seguire altri utenti
    OB 3. Visualizzare i viaggi dei propri amici
    OB 4. Cercare e visualizzare viaggi pubblicati da altri utenti
    OB 5. Creare il proprio viaggio, esso presenterà la possibilità di aggiungere:
            - Suddivisione in tappe
            - Descrizione dei luoghi visitati
            - Foto



# Requisiti Funzionali

Nella presente sezione vengono presentati i requisiti funzionali (RF) del sito.

### RF 1. accesso al sistema di utente anonimo
Il sistema deve permettere ad un utente non autenticato di usufruire solamente della funzioni di cui RF 2 e RF 5.

### RF 2. Registrazione al sistema di utente anonimo
Il sistema deve fornire all’utente anonimo la possibilità di registrarsi al sito. (Cfr. OB 1).

### RF 3. Gestione profilo
Il sistema deve permettere all’utente autenticato di visualizzare e modificare le proprie credenziali ed il proprio profilo.

### RF 4. Accesso al sistema di utente anonimo
Il sistema deve permettere all’utente anonimo di accedere al sito con le proprie credenziali precedentemente registrate. (Cfr. OB 1).

### RF 5. Ricerca utenti registrati
Il sistema deve permettere all’utente autenticato di ricercare e visualizzare gli altri utenti registrati. (Cfr. OB 2).

### RF 6. Visualizzazione Utenti ricercati
Il sistema deve permettere all’utente di visualizzare i profili che ha ricercato tramite la funzione ricerca utenti di cui RF 8. (Cfr. OB 2).

### RF 7. Seguire utenti registrati
Il sistema deve permettere all’utente autenticato di seguire gli altri utenti registrati.
(Cfr. OB 2).

### RF 8. Visualizzazione Contenuti profili seguiti
Il sistema deve permettere all’utente di visualizzare i contenuti pubblicati dagli utenti che segue. (Cfr. OB 3).

### RF 9. Ricerca contenuti
Il sistema deve permettere all’utente di cercare i viaggi degli altri utenti per luogo e per tipologia di viaggio. (Cfr. OB 4).

### RF 10. Visuallizazione contenuti ricercati
Il sistema deve permettere di mostrare all’utente i viaggi che ha ricercato tramite le funzione di cui ricerca contenuti di cui RF6. (Cfr. OB 4).

### RF 11. Pubblicazione contenuti
Il sistema deve permettere all’utente autenticato di pubblicare il proprio viaggio suddiviso in tappe, aggiungendo, se voluto, descrizione e foto. (Cfr. OB 5).



# Requisiti Non funzionali

Nella presente sezione vengono ridati i requisiti non funzionali (RF) del sito. Per una miglior fruibilità di essi alcuni sono stati raggruppati nonostante rappresentino entità a sé stanti.

### RNF 1. Sicurezza registrazione
La registrazione di un utente (Cfr. RF 2) deve comprendere:
- RNF 1.1. Uno username alfanumerico unico per un minimo di 4 ed un massimo di 16 caratteri.
- RNF 1.2. Una password alfanumerica di minimo 6 caratteri ed un massimo di 12 caratteri.


### RNF 2. Compatibilità
Il sito deve poter funzionare sui seguenti browser: Chrome, Edge e Safari.

### RNF 3. Usabilità
- RNF 3.1. Un utente autenticato che utilizza il sito per la prima volta deve essere capace di pubblicare un viaggio entro 5 minuti.
- RNF 3.2. Un utente non autenticato deve essere capace di cercare un viaggio pertinente entro 5 minuti.

### RNF 4. Prestazioni
- RNF 4.1. La ricerca di un viaggio deve essere completata entro 10 secondi.
- RNF 4.2. La ricerca di una persona deve essere completata entro 5 secondi.

### RNF 5. Gestione della privacy
L’archiviazione ed il trattamento di dati e contenuti degli utenti deve rispettare il regolamento [GDPR-2016/679](https://www.garanteprivacy.it/trattamento-dei-dati).

### RNF 6. Ricerca profili
La funzione di ricerca utenti (Cfr. RF 5) deve essere effettuata inserendo una stringa di massimo di 16 caratteri corrispondente all’username.

### RNF 7. Visualizzazione profili
La funzione di visualizzazione profili ricercati (Cfr. RF 6) deve essere effettuata mostrando un massimo di 15 utenti, correlati alla ricerca (Cfr. RF 5).

### RNF 8. Ricerca contenuti
- RNF 8.1. La funzione di ricerca contenuti (Cfr. RF 9)   deve essere effettuata inserendo una stringa di caratteri per un massimo di 16 caratteri corrispondente al nome del luogo o di una tappa.
- RNF 8.2. La funzione di ricerca contenuti (Cfr. RF 9)   deve inoltre permettere di selezionare il range di km della lunghezza del viaggio.


### RNF 9. Visualizzazione contenuti
- RNF 9.1. La  visualizzazione dei contenuti (Cfr. RF 8 e  RF10) deve fornire una mappa del tragitto creata tramite l’API di Google Maps:
- RNF 9.2. Il contenuto può avere una descrizione contente al massimo 1000 caratteri.

### RNF 10. Pubblicazione contenuti
Il contenuto che descriverà il viaggio (Cfr. RF 11) deve rispettare i seguenti vincoli:
- RNF 10.1. Deve essere diviso in un minimo di 2 e massimo di 10 tappe.
- RNF 10.2. Ogni tappa può contenere al massimo una foto.
- RNF 10.3. La selezione della tappa deve essere gestita dall’API di Google Maps.
- RNF 10.4. Durante la selezione, verrà mostrata un'anteprima di ciascuna tappa su una mappa, gestita da Google Maps.
- RNF 10.5. Il contenuto può avere una descrizione contente al massimo 1000 caratteri.


# Front-end

### Homepage
Il sito presenterà all'utente una schermata 'home', conterrà al centro dello schermo una barra di ricerca, in cui poter digitare il nome della zona in cui ricercare con, al suo fianco, un menù a tendina da cui selezionare la lunghezza desiderata tra diverse fasce. Al di sotto della barra di ricerca verrà presentata inizialmente una selezione di viaggi consigliati, che verrà sostituita dai risultati della ricerca dell'utente.
Inoltre, in alto, a fianco del nome e logo del sito, saranno presenti una serie di link (sotto forma di testo o icone) che condurranno l'utente alle altre sezioni del sito, descritte in seguito

### Seguiti
La maggior parte della pagina sarà dedicata a mostrare all'utente una lista composta da ciascun profilo seguito ed il proprio ultimo post.
Sopra a questa lista  saranno dei cerchi contenenti le foto profilo dei profili seguiti; selezionando uno di questi profili, la lista di viaggi mostrerà tutti i post appartenenti ad esso.
Selezionando l'ultimo a destra di questi cerchi sarà possibile cercare un altro utente non seguito. Una volta trovato la lista dei suoi post verrà mostrata come sopra e, selezionando di nuovo lo stesso cerchio, sarà possibile confermare di voler seguire questo utente o cancellare e visualizzare nuovamente i post dei propri amici nella lista

### Crea
Questa schermata permette agli utenti di comporre il proprio viaggio, selezionando ciascuna tappa da una barra di ricerca; una volta confermata una tappa, essa sostituisce la barra di ricerca nell'interfaccia, mentre la barra di ricerca viene spostata sotto di essa, in modo da aggiungere un'ulteriore tappa. Inoltre, a fianco delle tappe confermate, è presente un pulsante che permetta all'utente di allegare a ciascuna tappa un'immagine.
Sulla destra della pagina compare una mappa, che mostra l'anteprima delle tappe man mano che vengono inserite e confermate.

### Profilo
La schermata 'profilo' conterrà sulla sinistra la foto profilo e l'username dell'utente, seguiti da un pulsante dedicato alla modifica delle due. Inoltre, accanto a questa sezione, sarà presente la lista di tutti i post dell'utente


# Back-End
Nel presente capitolo vengono riportati i sistemi esterni con cui il sistema dovrà interfacciarsi per poter funzionare ed una loro descrizione.

Il sistema dovrà interfacciarsi con:
- Google Maps
- Database

### Google Maps
Verranno implementate le API Javascript di Google Maps; le quali serviranno per le seguenti funzionalità del sistema:
- Selezionare una tappa per un viaggio
- Visualizzare la mappa di un viaggio, la quale avrà un pin per ogni tappa ed un collegamento tra le varie tappe
- Calcolare la lunghezza totale del viaggio in km


### Database
Il sistema si interfaccerà con il database per:
- Memorizzare le credenziali dei vari utenti
- Memorizzare tutti i viaggi pubblicati con le relative caratteristiche

Il luogo di ciascuna tappa, grazie all’API di Google Maps, verrà salvato nel database in formato json. Il file json verrà inoltre modificato, in modo da contenere il collegamento alla foto che è stata caricata dall’utente nella relativa tappa.
Ciò consentirà una più facile e veloce creazione della mappa nel momento in cui verrà visualizzato un post.
