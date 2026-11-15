# pesca-sub-dati

Archivio giornaliero delle grafiche di previsione del bot **pesca-sub-salento** (solo immagini meteo-mare, nessun dato personale).

## Struttura

```
archivio/AAAA-MM-GG/<mattina|sera>/*.png
```

Esempio:

```
archivio/2026-11-15/mattina/1_migliore_ionio_oggi.png
archivio/2026-11-15/mattina/2_migliore_adriatico_oggi.png
archivio/2026-11-15/mattina/3_classifica_salento.png
archivio/2026-11-15/sera/1_migliore_ionio_domani.png
```

La data è quella italiana (`Europe/Rome`). Le cartelle vengono create dal workflow al primo invio: finché il bot non gira, `archivio/` non esiste ancora.

## Cosa contengono le immagini

Le schede che il bot manda su Telegram due volte al giorno: punteggio delle condizioni del mare per zona del Salento (vento, onde sotto costa, corrente, visibilità stimata, meteo), finestra oraria migliore, e la classifica delle zone.

Il punteggio misura **sicurezza e comodità in acqua**, non la resa di pesca. Le previsioni sono indicative e non vanno usate per la navigazione.

## Da dove arrivano

Le immagini sono pubblicate automaticamente dal workflow `daily.yml` della repo (privata) `pesca-sub-salento`, dopo l'invio su Telegram. Dati meteo-marini: Open-Meteo (DWD, Météo-France, ECMWF, Copernicus Marine).

Questa repo è di sola lettura per chi la consulta: viene scritta solo dal bot.
