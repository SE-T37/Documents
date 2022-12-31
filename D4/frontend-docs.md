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
Notare come l'accesso alle pagine 'Seguiti' e 'Crea' sia negato all'utente qualora esso non sia autenticato; in caso un utente del sito che non abbia effettuato l'accesso clicchi su uno dei due pulsanti corrispondenti, esso sarà invece reindirizzato alla pagina 'Profilo', dove sarà presente un form per il login.

## Luoghi


