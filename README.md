# YU-GI-OH API

#### CONSEGNA DELL'ESERCIZIO 

```
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare
 il layout come da screenshot allegato.

Al caricamento della pagina, effettuate una chiama ajax all'API di Yu Gi Oh: 

https://db.ygoprodeck.com/api/v7/cardinfo.php

e con i dati restituiti, stampate una card per ogni carta. Oggi non preoccupatevi per la ricerca.

PS: usate il font che preferite ;)

*ATTENZIONE*: l’api restituisce tutti i risultati in un colpo solo. Per evitare attese e/o 
rallentamenti nelle richieste, potete diminuire il numero di risultati sfruttando i parametri 
num e offset

https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0

*Bonus:*
Creare un componente loader da visualizzare fintantoché i risultati non sono pronti.

*Documentazione*: https://ygoprodeck.com/api-guide/
```

#### SVOLGIMENTO

Cominciamo con l'importare bootstrap, sass e axios nel nostro progetto.

In questo esercizio creaimo 2 macro-componenti che sono header e main.

L'header è composto da un componenete logo e un h1 che sarà il titolo della nostra pagina.

Il main invece sarà composto da un container bootstrap, che al suo interno avrà una select 
che andremo a far funzionare nell'esercizio successivo.

Dentro il nostro container ci sarà un div che conterrà la lista delle carte, composta da 
un header e dalla lista stessa.

Attraverso uno store dichiariamo un array vuoto al quale assegneremo il response desiderato 
della chiamata ajax che faremo nel nostro componenete lista. Una volta effettuata la chiamata 
e l'assegnazione, stampiamo il numero di carte trovate nell'header, e creiamo un componente 
per la singola carta, che andremo a ciclare dentro un *li*. Gli passiamo le props che ci servono 
per visualizzare l'immagine, il nome e il tipo di carta. Stilizziamo i componenti per avere delle
file da 5 elementi.

Per aggiungere una pagina di caricamento ci basterà spostare la chiamata ajax nell'App principale, 
importare li lo store, in modo che abbiamo accesso direttamente alla lunghezza dell'array, che ci 
servirà come condizione per dichiare un v-if nel loadingScreen e un v-else in un div che conterrà 
i nostri macro-componenti.

Nella schermata di loadingScreen possiamo ridimensionare il componente Logo passandogli una stringa 
che applicheremo come classe per ingrandirlo. La classe sarà presente nel nostro file utilities.css.

Possiamo aggiungere un footer a nostro piacimento.