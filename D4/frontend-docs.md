# Documentazione Front-End

L'implementazione di frontend sviluppata si pone di seguire le linee guida riportate nel documento 1; pertanto è stato scelto di utilizzare 5 distinti documenti .html relativi alle diverse pagine del sito

- Home
- Luoghi
- Seguiti
- Crea
- Profilo

A ciascuna di queste è associato un file .css dallo stesso nome, che ne gestisce lo stile, nonché alcuni script .js che aggiungono funzionalità sia grafiche, quali popup, sia funzionali, quali le chiamate al backend per ottenere i dati necessari al sito.

## Home

La pagina principale del sito consiste in una semplice lista delle proprie informazioni principali. Essa contiene tuttavia, in alto a destra, i pulsanti di navigazione principali, che permettono all'utente di spostarsi nelle 5 pagine e che rimangono anche nel layout delle rimanenti 4.
Notare come l'accesso alle pagine 'Seguiti' e 'Crea' sia negato all'utente qualora esso non sia autenticato; in caso un utente del sito che non abbia effettuato l'accesso clicchi su uno dei due pulsanti corrispondenti, esso sarà invece reindirizzato alla pagina 'Profilo', dove sarà presente un form per il login. Nell'ultimo paragrafo nella schermata iniziale è presente un link che ti porta alla pagina profilo.
Inoltre quando si accede alle diverse pagine è possibile tornare alla schermata Home cliccando sul logo del sito.

## Luoghi
La pagina Luoghi presenta inizialmente 6 viaggi casuali estratti dal databese accompagnati da un titolo e con la relativa foto.
Utilizzando la barra di ricerca, che rimane perennemente visibile durante lo scorrimento della pagina, è possibile cercare il viaggio desiderato in base al titolo. Inoltre è possibile filtrare la ricerca in base alla lunghezza del viaggio, cliccando il pulsante apposito sulla barra di ricerca che mostrerà un popup dove selezionare un range di distanze.
Per maggiori informazioni sulla lista dei viaggi si faccia riferimento all'api /searchViaggio nella documentazione del backend.

## Seguiti
La pagina, come la precedente, presenta una lista di viaggi nello stesso formato, ma i viaggi in questa pagina appartengono esclusivamente ai profili seguiti dall'utente del sito; per ottenere questo risultato è utilizzata l'api /getViaggiAmici. 
Questi ultimi compaiono inoltre come icona in alto nella pagina, in modo che l'utente, nell'implementazione finale, possa filtrare in base al profilo di cui desidera visualizzare i viaggi. Per ottenere dal database la lista di amici è utilizzata l'api /getUsers.

## Crea
Questa pagina permette all'utente di creare il proprio post, costituito da un titolo e descrizione generali seguito da massimo 10 tappe con la loro foto e descrizione.
Nella pagina è presente, in alto a sinistra, un form per il titolo, la descrizione e l'immagine del viaggio, seguita dalla lista di tappe selezionate.
è possibile aggioìungere fino ad un massimo di 10 tappe con il pulsante 'Add'; qui, nell'implementazione finale, sarà possibile cercare il luogo tramite ricerca grazie all'api di google maps, nonché caricare la propria foto con l'apposito pulsante. Nella stessa implementazione sarà infine possibile postare il viaggio finito utilizzando il pulsante 'Post!', che chiamerà l'api /newViaggio per salvarlo nel database.
A destra, nella pagina, è inoltre mostrata una mappa che presenta un'indicazione del percorso svolto, tappa per tappa, dall'utente.
Notare che, data lo stato incompleto della pagina, sono già state inserite due tappe di esempio sia sulla mappa che nella lista.

## Profilo
Nella pagina 'Profilo' è possibile gestire tutto ciò che riguarda l'utente, ovvero:
- Login
- Modifica Profilo
- Logout

è stato deciso di tralasciare la funzione di signup, tramite l'api /newUser, e di invece inserire un account standard, con credenziali:
Username: SteveJobs
Password: Apple1955!
in modo da poter avere utenti seguiti e viaggi personali già inseriti.
Questi ultimi sono presentati a destra nella pagina, qualora si effettui il login.