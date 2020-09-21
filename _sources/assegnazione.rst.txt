=============================
Gestione Assegnazione Persone
=============================
La gestione che si vuole realizzare in ACE, a completamento delle funzionalità inerenti i compiti dell’Ufficio Sedi, 
riguarda l’assegnazione di una risorsa alla sua sede di afferenza (Sede Amministrativa di riferimento) e alla sua sede di lavoro 
(entità locale ove presta servizio) e la gestione di tali informazioni che possono cambiare nel tempo.

La sede di afferenza e la sede di lavoro nella maggior parte dei casi coincidono, sono invece diverse quando si parla di ‘assegnazione’ 
temporanea a una sede diversa da quella di appartenenza o di distacco / mobilità temporanea. Questo aspetto viene gestito in ACE 
attraverso i RUOLI che specificano un’appartenenza precisa, in questo caso, che ha un dipendente rispetto ad una Sede 
(l’appartenenza potrebbe essere verso le Sedi, come in questo caso, o verso un’entità organizzativa diversa, ad esempio un progetto).

In questo momento analizziamo esclusivamente **l’assegnazione dei dipendenti alle Sedi** (quindi l’associazione di un Dipendente a 
Tipi Ruolo specifici: Tipologia ‘Sede’ e ‘Afferenza UO’, verso entità organizzative specifiche, Sedi) e non altri aspetti funzionali che 
comunque riguarderanno le Persone, i Ruoli e le Entità Organizzative di ACE.

Allo scopo, quindi, tratteremo due tipologie ruoli specifici (visibili nella funzione attuale di ACE: APPARTENENZA) ad oggi migrati da NSIP e gestiti solo in visualizzazione:

- SEDE
- AFFERENZA UO

Ogni dipendente avrà sicuramente in ACE questi due ruoli definiti rispetto alle Sedi (con l’indicazione della data inizio e fine di validità). 
Questa informazione viene definita per la prima volta in fase di Immatricolazione (si rimanda per questo all’analisi delle funzioni di Immatricolazione).

```
Al momento la fase di Immatricolazione resta gestita interamente in NSIP e, attraverso procedure di migrazione, i dati si rendono periodicamente disponibili in ACE.
- Come lasciare la prima assegnazione in ACE?
- Come migrare solo la prima assegnazione in ACE?
- Il processo dovrebbe essere bidirezionale ……
```

La funzionalità in oggetto si pone l’obiettivo di gestire queste informazioni in ACE, dopo l’assegnazione iniziale prevista in fase di immatricolazione, per due motivi fondamentali:

Trasferimento
=============

L’esigenza è determinata dalla nascita di nuove sedi (di tipo istituzionali) a cui assegnare personale, oppure dalla chiusura/accorpamento di sedi già esistenti che prevedono di conseguenza lo spostamento del relativo personale. In questo ultimo caso si ha che per la chiusura di una sede il personale ad essa assegnato viene distribuito ad una o più sedi (di solito geograficamente vicine) con l’eccezione che ogni dipendente potrebbe scegliere una sede diversa da quella assegnatagli facendo valere il ‘diritto di opzione’.
Allo stesso modo l’accorpamento di più sedi porterebbe ad un conseguente spostamento del personale verso la sede che ha accorpato altre sedi, anche se come il caso precedente il dipendente potrebbe chiedere di essere assegnato ad una sede diversa da quella prevista.
Questo aspetto è importante perché la relativa funzionalità di Assegnazione non può seguire una logica standard ma deve lasciare all’utente la possibilità di veicolare le persone provenienti da una stessa Sede, verso Sedi diverse.

I casi appena descritti si traducono comunque in un ‘Trasferimento’ definitivo del personale ad una nuova sede. 
Anche la richiesta di ‘Trasferimento volontario’ cade nella stessa casistica di cui al punto precedente.

Mobilità
========

Diverso invece è il caso di ‘Mobilità’ che si può verificare per diversi motivi:
    1. Assegnazione temporanea;
    2. Comando;
    3. Distacco TREU;
    4. Assegnazione internazionale;
    5. Assegnazione temporanea per Convenzione (ad esempio per le convenzioni con le Università).

Per quanto riguarda il Trasferimento, basta specificare, oltre alla matricola:
Data inizio;
UO di afferenza di destinazione;
Sede di lavoro di destinazione;
Data e numero Provvedimento (e relativo allegato)

Siccome più persone possono essere trasferite in una specifica nuova sede, deve essere possibile selezionare più persone contemporaneamente ed indicare i dati per la nuova assegnazione, compreso il provvedimento relativo.

Potrebbe servire, come requisito di consultazione delle assegnazioni, avere la possibilità di consultare la storia delle assegnazioni per persona, visualizzando le informazioni principali quali data, tipo di assegnazione, dati del provvedimento con relativo allegato, vecchia/nuova sede-UO di riferimento. Potrebbe essere utile anche poter consultare la ‘storia di una sede’ con le modifiche relative al cambio denominazione, cambio tipologia, persone assegnate e poi trasferite ……(da vedere dopo)

**Nel caso di Trasferimento la sede di afferenza e la sede di lavoro sono sempre uguali.**

Per quanto riguarda la **Mobilità**, invece, bisogna specificare, oltre alla matricola in esame:

**Codice Fascicolo**: (che potrebbe essere specificato sulla persona), per il fascicolo documentale NEPI che sembra ancora in uso per le Persone, diversamente dalle Sedi; ???

* **Tipo Mobilità**: una delle tipologie di Mobilità elencate prima;
* **Data inizio;**
* **UO di afferenza di destinazione;**
* **Sede di lavoro di destinazione;**
* **Data e numero Provvedimento** (di cui bisogna conservare l’allegato)
* **Oneri del comando**: che possono essere di tre tipi: ???
- Oneri Carico CNR;
- Stipendio Metropolitano;
- Oneri Carico Amministrazione Ricevente

**Nel caso di mobilità la sede di afferenza e la sede di lavoro sono sempre diverse.**

Funzionalità previste in ACE
============================

La nuova funzionalità ACE ‘Assegnazione Persone alle Sedi’, quindi, dovrebbe essere strutturata in modo da impostare informazioni di ‘Testata’:

Consentire la scelta del Tipo operazione (Trasferimento / Mobilità) e data operazione;
Consentire di specificare data e numero provvedimento e di allegare il relativo documento;
Consentire la scelta della UO/Sede di partenza e della UO/Sede di arrivo;

I dati della UO/Sede di partenza sono esclusivamente dati utili alla ricerca del personale afferente quindi potrebbe anche non essere specificata la UO o la Sede di partenza e in questo caso la ricerca successiva andrebbe a mostrare l’elenco del personale utilizzando i soli filtri indicati.

Dopo aver specificato i dati di testata la funzionalità presenterà il risultato della ricerca e quindi l’elenco del personale secondo i filtri indicati di UO e Sede (da tab. persona_entita_organizzativa utilizzando  tipo_appartenenza SEDE/APPARTENENZA UO, dominio fisso, e entita_organizzativa_id a seconda di quanto indicato dall’utente come filtro di ricerca)

Sarà, a questo punto, proposta la lista dei dipendenti assegnati alla UO/Sede di partenza indicata, con tutte le informazioni di ‘partenza’: 

Lista dati della persona in ordine alfabetico Cognome:
    • Matricola/Cognome/Nome, Profilo, Livello, Uo e Sede di appartenenza, tipo di assegnazione attuale alla sede (da migrare perché attualmente il dato non è in ACE);

Dovrà essere possibile a questo punto, selezionare una o più persone dalla lista e spostarle in un’area di modifica:
    • Matricola/Cognome/Nome 	Non modificabili
    • UO/sede di arrivo 		Proposti con UO e Sede di arrivo specificati in testata;
    • Tipo di assegnazione:
        ◦ Nel caso di tipo operazione = ‘Trasferimento’, bisogna proporre la stessa tipologia di partenza non modificabile e controllare che la UO/Sede di arrivo sono sempre uguali tra loro;
        
        ◦ Nel caso di tipo operazione = ‘Mobilità’, bisogna proporre la stessa tipologia di partenza, modificabile, con le tipologie di Mobilità previste e inoltre specificare gli Oneri della Mobilità (da migrare perché attualmente il dato non è in ACE);


A seconda del tipo operazione sarà modificata, per la lista dei dipendenti selezionati, l’Appartenenza in ACE che poi dovrà essere migrata in NSIP.
Decidere se migrare lo storico delle assegnazioni pregresse in ACE
Definire come aggiornare in NSIP i dati che non sono nella tab. pea_assegnazione (

Si potrebbe prevedere partendo dalla gerarchia sedi (gerarchia scientifica e amministrazione centrale) che alla chiusura di una sede si possa automaticamente passare alla funzione di assegnazione del personale impostando data di trasferimento, e Sede da cui spostare il personale (sede che è stata chiusa).
In questo modo si avrebbe anche già disponibile la ricerca del personale da spostare (afferente alla sede che si chiude) e si potrebbe direttamente proseguire con la selezione delle persone da spostare e la specifica delle informazioni rimanenti per procedere con le nuove assegnazioni.

Dopo la prima operazione di spostamento, che potrebbe non riguardare tutto il personale afferente, alla conferma, sarà rieseguita la ricerca della lista persone, lasciando invariati i dati di testata in modo da mostrare la lista aggiornata del personale ancora assegnato alla sede di partenza e dare la possibilità all’utente di proseguire con la nuova selezione e nuovi spostamenti.

La modifica delle informazioni inerenti il Trasferimento e la Mobilità, gestite in ACE, saranno poi periodicamente e automaticamente trasferite in NSI
Note
L’utente ha espresso alcuni nuovi requisiti rispetto a quanto gestito oggi in NSIP, da tenere in conto per la gestione in ACE:

• Oltre alla data fine validità della creazione associazione persona/entità organizzativa deve essere gestita una data prevista fine delle assegnazioni (per i contratti non a tempo indeterminato) in modo da poter inviare mail di segnalazione un mese prima di queste scadenze. Probabilmente questo aspetto potrà essere gestito con la data di scadenza contratto-persona, ad oggi indicata sulla Persona.
• Si chiede di poter gestire l’assegnazione alle Sedi in percentuale. C’è l’esigenza di poter tracciare le ‘assegnazioni’ di persone che lavorano contemporaneamente per più sedi.

