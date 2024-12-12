# ProgettoSAD: gruppo B1,task R2
# Membri del gruppo: 
Esposito Andrea M63001650 andrea.esposito66@studenti.unina.it
Papale Livio M63001824 li.papale@studenti.unina.it
Sorrentino Carmine M63001819 carmine.sorrentino4@studenti.unina.it
Vallefuoco Roberto M63001443 roberto.vallefuoco@studenti.unina.it


# Descrizione del lavoro svolto: 
Le modifiche assegnate impattano nella loro totalità sul microservizio
T5, in quanto, oltre ad essere in esso situato il Page Builder, che ab-
biamo usato per estendere le funzionalità offerte da T5 aggiungendo
la pagina della classifica, abbiamo poi aggiunto un database non re-
lazionale mongoDB sempre in T5 per la gestione dei dati relativi alla classifica, in modo da poter rispettare il requisito funzionale di fornire
a ciascun utente che lo richieda la classifica e i requisiti non funzionali
legati alla robustezza nel gestire una maggiore quantità di richieste.
L’uso di un database aggiuntivo nonostante la ridondanza dei dati
(parzialmente già presenti in altri database in altri microservizi del
software), permette di ottenere una significativa robustezza nel con-
testo di un’architettura a microservizi, come quella in cui abbiamo
operato.
Per quanto riguarda le decisioni di progetto che abbiamo preso, innanz-
itutto, nella ristrutturazione del microservizio T5 realizzata al fine di
soddisfare i requisiti, abbiamo introdotto un database non relazionale
mongoDB in T5 al fine di gestire i dati relativi alla classifica.
Questa scelta è stata presa sia al fine di rispettare il requisito funzionale
"Il sistema deve aggiornare tutte le classifiche ad ogni nuova partita registrata" e i requisiti non funzionali "Il sistema deve essere robusto
alla ricezione di molte richieste di aggiornamento delle classifiche" e
"Il sistema deve essere robusto alla ricezione di molte richieste di vi-
sualizzazione delle classifiche", in quanto tale robustezza è garantita
proprio dal fatto che, avvenendo il salvataggio della classifica in esso,
ciò non pesa sui terminali dei giocatori che richiedono di visualizzare
la leaderboard.
