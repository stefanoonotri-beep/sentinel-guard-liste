# Chat intime e compagni virtuali — elenco di blocco

Un elenco pubblico di piattaforme di **conversazione romantica o erotica**, compresi i
personaggi artificiali con cui si intrattiene una relazione simulata: siti e applicazioni
Android.

Esistono ottimi elenchi pubblici per la pornografia ([StevenBlack][sb], [HaGeZi][hz],
[UT1][ut1]), e nessuno per questa categoria. Non è una dimenticanza: è una dipendenza più
recente e meno riconosciuta delle altre, più lenta e più affettiva, e i filtri per adulti non
la intercettano perché tecnicamente non sono siti porno. Questo elenco riempie quel buco.

| file | cosa contiene |
| --- | --- |
| [`compagni.txt`](compagni.txt) | l'elenco: domini e pacchetti Android |
| [`da-rivedere.txt`](da-rivedere.txt) | candidati incerti, **non bloccati**, in attesa che qualcuno li verifichi |

## Come si usa

```
https://raw.githubusercontent.com/stefanoonotri-beep/sentinel-guard-liste/main/compagni.txt
```

Un dominio per riga. Le righe che cominciano con `app:` sono nomi di pacchetti Android, per
i filtri che sanno bloccare anche le applicazioni; chi legge solo domini le ignora. I
commenti cominciano con `#`.

```
character.ai
replika.com
app:ai.character.app
```

Il confronto sui domini è pensato **gerarchico**: chi blocca `character.ai` blocca anche
`beta.character.ai` e qualunque altro sottodominio, che è il modo con cui questi servizi si
spostano quando un blocco ingenuo li raggiunge.

Il formato hosts (`0.0.0.0 esempio.com`) viene letto lo stesso da qualunque lettore scritto
per gli elenchi già esistenti, quindi questo file si può dare in pasto agli stessi strumenti
senza modifiche.

## Cosa non c'è, e non deve esserci

Gli **assistenti generalisti** restano fuori: `chatgpt.com`, `claude.ai`, `gemini.google.com`,
`copilot.microsoft.com`, `perplexity.ai`, `poe.com`. Bloccarli toglierebbe strumenti di
lavoro e di studio, ed è il tipo di errore che fa disinstallare il filtro il giorno stesso.

Fuori anche gli **assistenti per gli appuntamenti**, quelli che aiutano a scrivere a persone
vere. Saranno pure discutibili, ma sono un'altra cosa: qui si raccolgono le relazioni
simulate.

Fuori i **creatori di avatar e di ritratti**, anche quando il nome sembra dire il contrario,
e fuori le **app di incontri** fra persone reali — per quelle esiste già la categoria
`dating` di UT1.

## Come nasce l'elenco

Le voci vengono da una ricerca automatica sulle schede del Google Play Store e dai siti che
quelle schede dichiarano — nessun motore di ricerca — e **nessuna voce entra qui senza essere
stata guardata**. Chi propone trova; chi pubblica decide. I candidati respinti sono respinti
con un motivo scritto, e quelli su cui il nome non basta a decidere finiscono in
`da-rivedere.txt` invece che nell'elenco: meglio un blocco che manca di un'app che un blocco
che colpisce quella sbagliata.

## Se c'è un errore

Se un dominio o un'app sono finiti qui per sbaglio, **apri una issue**: si guarda e si toglie.
Un elenco di blocco che sbaglia e non si corregge smette di essere usato, ed è giusto così.

Vale anche per il verso opposto: se manca qualcosa, segnalalo.

## Licenza

[CC0 1.0](LICENSE) — pubblico dominio. Copiabile, modificabile e riusabile da chiunque,
senza chiedere permesso e senza attribuzione.

[sb]: https://github.com/StevenBlack/hosts
[hz]: https://github.com/hagezi/dns-blocklists
[ut1]: https://gitlab.com/olbat/ut1-blacklists
