# ISPW · Tutoraggio BCE
 
Materiale di supporto per il **tutoraggio del corso di Ingegneria del Software e Progettazione Web (ISPW)**,
Università degli Studi di Roma "Tor Vergata", A.A. 2026-2027.
 
Il repository raccoglie alcuni casi d'uso modellati secondo il pattern architetturale **BCE**
(Boundary – Control – Entity) e implementati in Java. Ogni caso d'uso parte da una versione
volutamente essenziale e viene **raffinato una tappa alla volta**, introducendo concetti nuovi di volta
in volta.
 
---
 
## Come è organizzato
 
Ogni caso d'uso ha la propria catena di branch. Ogni branch è una tappa e parte da quella precedente:
 
```
<caso-d-uso>/fase-0  →  <caso-d-uso>/fase-1  →  <caso-d-uso>/fase-2  →  ...
```
 
Il branch `main` contiene soltanto questa pagina.
 
---
 
## Esempio di evoluzione
 
| Fase | Cosa introduce |
|:----:|----------------|
| **0** | BCE di base: interfaccia a riga di comando, nessun bean, nessuna persistenza, nessuna eccezione, nessun pattern GoF |

Le fasi successive verranno pubblicate man mano.
 
---
 
## Casi d'uso
 
| Caso d'uso | Branch | Fase attuale |
|------------|--------|:------------:|
| Verbalizzazione esame | `verbalizzazione/fase-0` | 0 |
 
---
 
## Fase 0, in breve
 
- **Solo CLI**: le uniche classi che leggono da tastiera e stampano a schermo sono quelle del package `view`.
- **Niente bean**: boundary e controller si scambiano solo tipi semplici, mai entity.
- **Niente persistenza**: i dati vivono in memoria finché l'applicazione resta aperta; lo strato di persistenza è simulato.
- **Niente eccezioni**: i casi di errore sono segnalati da commenti nel codice.
---