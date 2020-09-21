**Manuale ACE**

**Introduzione**

ACE – Anagrafica Centralizzata

Il modulo software ACE gestisce le anagrafiche del CNR relativamente
alle strutture, dati anagrafici del personale CNR (strutturato e non) e
ruoli assegnati ad essi.

I ruoli gestiti sono sempre riferiti al personale e possono riguardare:

-  Ruoli Istituzionali (definiti da appositi provvedimenti e pubblicati
   in Albo);

-  Ruoli Istituzionali non pubblicati in Albo (incarichi che danno
   diritto ad indennità ma non sono pubblicati in Albo);

-  Ruoli Applicativi e gestionali (utili alle diverse applicazioni
   dell’Ente per definire le autorizzazioni di accesso ai dati e le
   modalità di utilizzo delle funzioni).

ACE comprende alcune funzionalità utilizzabili esclusivamente da
personale tecnico per la configurazione necessaria al corretto
funzionamento dell’applicazione, e altre funzionalità utili alla
Gestione Sedi e Gestione Personale CNR, utilizzabili dal personale
Amministrativo dell’Ente. Successivamente sarà possibile creare
funzionalità, con opportune abilitazioni, utilizzabili dalle strutture
decentrate dell’Ente per la gestione autonoma di alcune informazioni.

**Scopo del modulo ACE**

La creazione di un modulo software per la gestione delle anagrafiche
centralizzate nasce dal fatto che le informazioni di ‘base’ per
molteplici applicazioni in uso presso l’Ente risultavano frammentate e
duplicate con la conseguenza di possibili disallineamenti e frequenti
duplicazioni che richiedevano uno sforzo continuo affinchè fossero
congruenti e corrette. ACE ha l’obiettivo di uniformare e gestire in
maniera centralizzata e univoca queste informazioni rendendole poi
disponibili ai vari applicativi che ne hanno necessità per completare le
proprie funzionalità specifiche.

Il lavoro di progettazione e implementazione di ACE consiste nel
valutare singolarmente gli applicativi CNR in produzione che gestiscono
‘anagrafiche comuni’ e gradualmente passare all’utilizzo delle sole
informazioni ‘centralizzate’ invece di attingere alle diverse fonti
utilizzate o duplicare i dati.

Nella valutazione delle integrazioni da realizzare è possibile lasciare
la proprietà di alcuni dati (e quindi la gestione) ai singoli
applicativi di competenza per poi ‘centralizzare’ le informazioni al
fine di renderle disponibili agli altri applicativi che le utilizzano.

**Funzionalità**

Le funzionalità di ACE sono distinte fondamentalmente in:

1. Funzioni di Amministrazione;

2. Gestione dati Centralizzati;

1. **Funzioni di Amministrazione (Configurazioni)**

Questa sezione comprende le funzionalità di parametrizzazione del
sistema ad uso esclusivo degli *Amministratori del Sistema*.

Le parametrizzazioni possibili si riferiscono a:

1. **Tipi entità organizzative**

Questa funzionalità si occupa di censire le tipologie delle Entità
Organizzative qualificandole, oltre che per colore, descrizione e sigla,
anche per categorie di appartenenza. Abbiamo quindi un raggruppamento
delle entità organizzative in ‘Tipi’ e ogni tipo entità organizzativa
appartiene ad una o più categorie.

In questa anagrafica vengono specificati anche i Ruoli che possono
essere associati elle Entità Organizzative appartenenti ad una specifica
Tipologia.

E’ indicata inoltre una data di inizio e fine validità del Tipo Entità
Organizzativa.

2. **Tipi gerarchia e Struttura Tipi gerarchia**

Il tipo gerarchia qualifica la gerarchia che viene descritta nel
paragrafo di ‘Gestione della Gerarchia’ e rappresenta un dominio di
valori, predefiniti e non modificabili, utili balle applicazioni esterne
ad ACE che richiedono servizi per una specifica gerarchia.

Anche il Tipo Gerarchia è raggruppato in Categorie.

La struttura dei tipi gerarchia consente di definire un ‘ordine di
visualizzazione e di gestione’ delle entità organizzative all’interno
della gerarchia. La struttura dei tipi obbliga, infatti, è utile a
definire come le entità organizzative possono essere poste in gerarchia
tra di loro nella costruzione e modifica della gerarchia stessa.

3. **Tipi entità locali e gestione Entità locali**

Le Entità locali includono le Strutture territoriali (Nazioni, Province,
Comuni, indirizzi e le relative informazioni correlate. Questi dati
dovranno essere aggiornati *in modalità periodica e automatica dai file
dell’ISTAT, quindi la loro gestione deve restare ad uso esclusivo
dell’amministratore del sistema.*

Per Entità locale in ACE si intende una specifica collocazione
geografica incluso l’attributo ‘Presso’ che specifica se l’indirizzo è
collocato presso altra struttura. Le sedi di ACE sono legate all’entità
locale (che comprende un indirizzo) e non direttamente ad un indirizzo
specifico.

4. **Contesti**

I contesti raggruppano i ruoli per in modo da poter accedere ad essi
dalla specifica applicazione. Ogni contesto resta autonomamente gestito,
per la definizione dei ruoli, dall’applicazione che si integra ad ACE.

I contesti ‘Istituzionali’ (per ruoli istituzionale inseriti o meno
nell’Albo dell’ente) vengono definiti e gestiti da ACE perché
rappresentano ruoli ufficiali a cui accedono tutte le applicazioni. I
ruoli invece ‘applicativi’ includono specifiche esigenze
dell’applicazione che si integra ad ACE e non sono relativi a nomine
‘ufficiali’.

All’interno di un contesto vengono quindi indicati i ruoli che ne fanno
parte. Un ruolo potrebbe essere associato anche a più contesti.

Per ogni contesto è specificato:

-  Amministratore del contesto (Ruolo)– Chi ha assegnato questo ruolo è
   abilitato a creare, gestire e ad assegnare tutti i ruoli del
   contesto;

-  Gestore del contesto (Ruolo) – Chi ha assegnato questo ruolo è
   abilitato solo ad assegnare tutti i ruoli del contesto.

-  Il Contesto ‘SISTEMA’, che definisce i ruoli necessari al
   funzionamento di ACE, non è modificabile.

   5. **Ruoli**

Il ruolo in ACE qualifica funzioni di tipo Istituzionali e mansioni di
tipo Applicativo, come specificato al paragrafo precedente.

Ci sono poi alcuni ruoli di SISTEMA per l’amministrazione del sistemai
ACE:

-  SUPERUTENTE: Gestore dell’Applicazione. Abilitato a tutto;

-  ADMIN: Amministratore del Sistema. Abilitato a gestire tutte le
   ‘configurazioni’;

-  DEVELOPER: Ruolo di sviluppo utilizzato da applicazioni esterne ad
   ACE. Abilitato in lettura a tutti i dati;

Sui contesti abbiamo indicato ruoli che *concedono* particolari
abilitazioni.

Per i ruoli Istituzionali è prevista una gestione centralizzata e per i
ruoli applicativi, invece, ACE ne cura la definizione che sarà poi
utilizzata dagli applicativi secondo le logiche interne.

Le informazioni previste nella definizione di un Ruolo sono, oltre a
descrizione e sigla:

Ruolo padre: utile alla gestione del raggruppamento dei ruoli;

L’indicazione dell’associazione del ruolo ai contesti. In questa sezione
possono essere specificati i contesti ai quali il ruolo appartiene e
vengono visualizzate le associazioni eventualmente gestite anche dalla
funzione dei contesti.

Vengono inoltre gestite le informazioni del ‘Gestore del contesto’ e
‘Amministratore del contesto’ gestibili anche dalla funzione dei
contesti (vedi Contesti).

E’ possibile inoltre specificare i Tipi entità organizzative che possono
utilizzare il Ruolo ed è specificato l’utilizzo del ruolo: Assegnabile a
livello globale. Questa informazione specifica se nell’associazione
Persona-Ruolo-Entità organizzativa è possibile o meno assegnare il ruolo
ad una persona senza specificare l’entità organizzativa. L’assenza
dell’entità organizzativa in questa associazione da la possibilità
all’utente (persona) di espletare il Ruolo su tutte le entità
organizzative dell’Ente.

Diversa invece è l’abilitazione ‘Ruolo Utente’ (funzionalità specifica
utilizzabile solo dagli Amministratori del Sistema). Questa abilitazione
serve per poter assegnare un Ruolo ad un Utente che non sia una Persona
fisica (riservata ad esempio alle applicazioni che interrogano ACE)
oppure per assegnare ad utenti/persone fisiche i Ruoli del contesto
SISTEMA. Tramite questa abilitazione vengono anche gestiti i servizi di
ACE che restituiscono informazioni centralizzate andando anche a
controllare a quali contesti è abilitato l’Utente (ad esempio Scrivania
Digitale potrebbe interrogare ACE per avere i ruoli sia del contesto
‘Scrivania’ sia del contesto ‘Missioni’ perché avvia flussi anche per
conto di altre applicazioni).

Il Gruppo dei Ruoli invece rappresenta una ulteriore parametrizzazione
per poter gestire i Ruoli ‘Ereditati’. Ogni contesto può gestire i suoi
raggruppamenti creando appunto un gruppo di ruoli che hanno
caratteristiche simili. Ciò è possibile definendo dei Ruoli di tipo
‘raggruppatore’ e assegnando a questi i ruoli che ne fanno parte.

2. **Funzioni per la gestione dei dati centralizzati**

Questa sezione comprende le funzionalità di gestione, quasi tutte ad uso
degli uffici dell’Amministrazione centrale dell’Ente. Esse si riassumono
in:

Entità organizzative

Gerarchie

Persone

Ruoli

1. **Gestione Sedi (incluso nelle Entità Organizzative)**

La gestioni delle Sedi, effettuata dall’ufficio Risorse Umane, si occupa
di inserire, modificare e completare le informazioni correlate, relative
ad una Sede istituita o modificata da un apposito Provvedimento
cartaceo.

Le funzionalità prevedono la creazione di una sede e la sua collocazione
in Gerarchia e la modifica/chiusura di una Sede.

L’entità Organizzativa di tipo Sede può essere creata tramite la
funzionalista specifica di gestione anagrafica oppure direttamente in
gestione Gerarchia attraverso le funzionalità disponibili:

**Crea Entità Organizzativa;**

**Associa Entità esistente;**

**Associa copiando da …**

Queste funzionalità consentono di creare e/o associare alla gerarchia la
sede contemporaneamente.

E’ previsto in futuro l’automatizzazione del processo amministrativo di
Istituzione e chiusura della sede, con invio automatico all’ufficio
preposto del Provvedimento specifico.

Il processo funzionale attuale di creazione e chiusura sedi prevede
l’aggiornamento automatico e notturno delle informazioni nel Sistema
NSIP che continua la sua attività di gestione per tutte le problematiche
legate alla Gestione del Personale.

Le informazioni fondamentali della gestione Sede sono:

**Progressivo Sede**: assegnato automaticamente dal sistema;

**Codice NSIP**: codice gestito e indispensabile alla procedura NSIP.
Questo codice viene attribuito manualmente dall’utente che segue logiche
di progressività necessarie alla procedura NSIP

**Denominazione**: denominazione specificata nel provvedimento di
istituzione;

**Denominazione breve**;

**Sigla**: Acronimo della Sede

**Codice Contabile**: codice attribuito alla struttura dall’ufficio
bilancio (CDS_UO)

**Tipo entità organizzativa**: Tipologia Sede (da lista predefinita)

**Indirizzo**: relazione all’entità locale (gestita con apposite
anagrafiche e contenente oltre all’indirizzo anche il ‘Presso’).

**Data Istituzione**: Data inizio validità (indicata nel provvedimento)

**Data Disabilitazione**: Data fine validità Sede

Nel chiudere una Sede bisogna sempre tener conto che:

1. La sede che si chiude non sarà più visibile in nessuna gerarchia;

2. Esistono ruoli e/o deleghe legati alla sede che si chiude che
   automaticamente vengono chiusi secondo le regole definite.

**Carattere**: ad oggi disponibili solo 2 valori: Amministrativo/Ricerca

Tale informazione viene utilizzata dagli utenti di NSIP per produrre
delle liste di Sedi CNR a carattere di Ricerca piuttosto che a carattere
Amministrativo (la tipologia di attività al momento non corrisponde alla
gerarchia di appartenenza in ACE: Strutture Scientifica/Amministrazione
Centrale).

**Allegati:** Gli allegati sono necessari per poter inserire i
provvedimenti di istituzione e disabilitazione delle strutture, ed
eventualmente altri documenti utili. In seguito i provvedimenti
potrebbero essere resi disponibili già in formato digitale dagli uffici
che li definiscono.

La creazione di una sede (nell’elenco delle Entità Organizzative) deve
poi essere completata dall’associazione della stessa nelle gerarchie. La
creazione della sede senza l’associazione in gerarchia comunque rende
già utilizzabile e operativa la sede alla procedura NSIP.

**Le abilitazioni che consentono la creazione e la modifica delle sedi
è:**

**‘Ufficio Gestione Sedi’. Questa abilitazione consente anche la
ricezione di una mail per ogni sede creata o modificata (solo per
tipologie entità organizzative specifiche: Sede Principale Istituto e
Sede Secondaria Istituto).**

2. **Gestione delle Gerarchie**

Per gestione delle Gerarchia si intende l’organizzazione delle Entità
Organizzative secondo una ‘vista gerarchica’ con una tipologia
predefinita.

Le gerarchie già identificate e ‘ufficiali’ al momento sono:

1. **Struttura scientifica**. Rappresenta l’organizzazione attuale dei
   dipartimenti, Istituti e Sedi secondarie con la quale opera la
   struttura scientifica del CNR. Questa gerarchia ospita anche le AREE
   di Ricerca poste non in gerarchia ma allo stesso livello dei
   Dipartimenti.

2. **Amministrazione Centrale**. Rappresenta l’organizzazione degli
   Uffici della Sede Centrale come da organigramma attuale del CNR.

3. **Rappresentanza Sindacale Unitaria**. Rappresenta l’organizzazione
   delle RSU dislocate su tutto il territorio nazionale, alle quali
   afferiscono tutte le sedi del CNR. La gerarchia RSU viene definita in
   genere ogni tre anni ed eventualmente modificata anche nel corso del
   triennio di validità magari per chiusura/apertura di una nuova sede
   RSU o per modifica assegnazione sede CNR a sede RSU.

Mentre la gerarchia relativa alla Struttura Scientifica e quella
relativa all’Amministrazione Centrale vengono gestite dallo stesso
ufficio (gestione Sedi), la gerarchia RSU viene gestita dall’ufficio
Relazioni Sindacali.

**Abilitazioni**

**L’ufficio Gestione Sedi** è abilitato, come specificato anche nel
paragrafo relativo alle Sedi, a gestire le entità organizzative
appartenenti alla categoria sedi.

In ogni caso l’utente potrà:

-  Cercare una sede per visualizzarla o modificarla, oltre che
   dall’anagrafica delle entità organizzative, anche direttamente dalla
   gerarchia a cui risulta assegnata. L’albero della gerarchia viene
   aperto per mostrare i dettagli evidenziati che rispondono alla
   ricerca effettuata. Nelle gerarchie Amministrativa e Scientifica è
   consentito solo creare sedi nella medesima tipologia.

-  Creare una nuova Sede;

-  Modificare una Sede esistente (sempre tra quelle modificabili);

-  Annullare una Sede (specificando data fine validità dell’entità
   organizzativa);

-  Gestire le associazioni delle sedi alle gerarchie (data inizio e fine
   associazione alla gerarchia).

**L’ufficio RSU** è abilitato a:

-  Inserire o modificare una sede di tipo ‘RSU’ (gestione gerarchia
   ‘RSU’);

-  Gestire la gerarchia RSU (associando le sedi Amministrative e
   Scientifiche alla rispettiva sede RSU);

-  Indicare tra le sedi CNR associate ad una sede RSU l’istituto guida
   (uno solo per sede RSU, primo livello gerarchia RSU). Informazione
   dell’associazione alla gerarchia e non della Sede stessa.

**La funzione di Gestione Gerarchia,** quindi, consente come prima cosa
di scegliere la gerarchia su cui lavorare (secondo le abilitazioni).
Viene mostrato l’elenco delle sedi in ordine di gerarchia (definito
parametricamente nella Struttura Tipi Entità Organizzative) e secondo i
filtri di ricerca indicati dall’utente. Sulla riga vengono visualizzati
i dati fondamentali (Descrizione della sede, sigla, codice NSIP, data
associazione alla gerarchia) ed è consentito effettuare varie
operazioni:

1. Cercare un’entità organizzativa specifica, indicando nel campo di
   ricerca predisposto, la descrizione oppure il codice NSIP o il codice
   contabile. E’ possibile impostare come filtro di ricerca il Tipo
   Sede);

2. Creare una nuova entità organizzativa e porla nella gerarchia al
   primo livello (funzionalità posta in alto nella mappa);

3. Posizionarsi su un ramo esistente della gerarchia e creare una nuova
   entità organizzativa che sarà posta come ramo figlio rispetto a dove
   si è posizionati;

4. Modificare o visualizzare le unità organizzative navigando nella
   gerarchia e aprendo la funzione di modifica (pulsante posto sul
   dettaglio della gerarchia);

5. Chiudere una sede ponendo in modifica la data fine validità (la sede
   chiusa risulterà tale in tutte le gerarchie in cui è stata inserita);

6. Disassociare la sede dalla specifica gerarchia ponendo in modifica la
   data fine validità sull’associazione Entità Organizzativa alla
   gerarchia (in questo caso la sede non sarà più visibile per la
   gerarchia in questione, ma sarà eventualmente visibile e associabile
   in altre gerarchie);

7. Spostare una sede ponendola in un ramo diverso della gerarchia.
   Questa operazione consiste nel mettere una data fine validità
   sull’associazione della sede al ramo da cui viene tolta e nel creare
   una nuova associazione della sede ad un altro ramo della gerarchia.

Inserendo la data di inizio validità e il nuovo ramo padre, è possibile
in un’unica operazione disassociare l’entità organizzativa e associarla
al nuovo ramo indicato.

Questa operazione vale solo per la gerarchia su cui si sta lavorando
(nulla cambia per l’anagrafica dell’entità organizzativa);

8. Visualizzare i ruoli associati alla sede (nel caso l’utente fosse
   abilitato a più contesti potrà scegliere nella funzione di
   visualizzazione ruoli il contesto per il quale filtrare i ruoli,
   altrimenti in automatico saranno mostrati i ruoli dell’unico contesto
   abilitato);

9. Visualizzare le persone associate alla Sede (per appartenenza
   Sede/UO).

Sulla riga della gerarchia, quindi, è possibile **creare** una nuova
sede (associata automaticamente alla gerarchia stessa), **associare**
una sede già esistente cercandola nella lista delle sedi valide alla
data indicata in alto nella mappa, **modificare** alcune informazioni
della sede o dell’associazione alla gerarchia, **cancellare** una sede
indicando la data fine validità entrando sempre in modifica.

E’ importante tener conto che nel momento in cui viene visualizzata una
gerarchia con tutte le informazioni delle Sedi, bisogna indicare la data
alla quale si desidera gestire la gerarchia stessa.

Questa data (posta tra i filtri di ricerca in alto nella mappa) è
proposta in automatico come la data del giorno (quindi tutte le sedi non
più valide o le associazioni alla gerarchia non più valide non saranno
visibili). Per consultare una situazione precedente bisogna modificare
la data proposta con la data alla quale si desidera consultare la
gerarchia.

La creazione di un Nuovo Istituto è stata semplificata attraverso la
funzionalità ‘Crea Istituto con Sede Principale’ (per la gerarchia
Scientifica).

Questa funzionalità consente di creare contemporaneamente il ramo
‘Istituto’ con entità organizzativa di tipo ‘Istituto’ (livello
gerarchico padre di tutte le sedi dell’Istituto) e la sua sede
principale/secondaria, in un’unica soluzione (mappa unica in cui si
specificano tutti i dati compreso le sedi principali e secondarie). In
questo modo si evita all’utente la ripetizione di alcune informazioni
disposte su tutte le sedi del nuovo Istituto. Questa opzione riguarda
solo la struttura scientifica.

**Funzione di utilità relativa a: Crea Sede copiando da…**

La copia di una sede è utile per creare velocemente una nuova sede
utilizzando i dati di una sede esistente.

Bisogna però tener conto che i dati proposti (Descrizione, descrizione
breve, Sigla, UO, Indirizzo ….) devono essere opportunamente modificati
per la sede che si sta creando. Il codice NSIP, univoco per tutte le
sedi, deve essere specificato dall’utente secondo le regole di
assegnazione. E’ possibile anche contestualmente chiudere la sede da cui
si sta copiando (nel caso in cui ci fosse un cambio denominazione e/o
cambio indirizzo di una sede) ed in tal caso sarà proposta come data di
chiusura il giorno antecedente l’inizio validità della nuova sede. Se si
sceglie di chiudere la sede da cui si copia bisogna tener conto di tutte
le conseguenze indicate per la chiusura di una sede.

La funzione di copia è stata resa disponibile su tutti i rami della
gerarchia parametrizzando l’anagrafica dei Tipi entità organizzative. In
questa anagrafica per ogni Tipo entità organizzativa è possibile
specificare una o più ‘categorie’. La categoria che rende disponibile la
funzione di copia sui rami della gerarchia, per l’entità organizzativa
dello specifico tipo, è: **Livello Padre Sedi**.

3. **Persone**

Questa sezione riguarda tutto il personale, strutturato e non
strutturato, che collabora a vario titolo con il CNR (dipendenti,
borsisti, assegnisti, collaboratori, professionisti ecc.). In questa
sezione sono inclusi i Dipendenti CNR, che ad oggi sono gestiti
dall’attuale procedura del Personale NSIP, ed i collaboratori che ogni
Direttore di Istituto censisce sulla Intranet (nell’applicazione
Gestione Istituti).

A questo scopo, per i dipendenti, vengono migrate in ACE quotidianamente
le informazioni dalla procedura NSIP e per i collaboratori, in tempo
reale, la procedura di Gestione Istituti invia le informazioni quando
queste vengono gestite sulla Intranet.

Tutte le informazioni di dipendenti e collaboratori sono fondamentali
all’individuazione della **Persona** che a vario titolo lavora nel CNR e
sono indispensabili per la gestione dei Ruoli.

I dati fondamentali delle persone al momento visualizzati sono:

Matricola (solo Dipendenti);

Nome;

Cognome;

Codice Fiscale.

Uo (sede) di appartenenza;

Eventuale data di cessazione;

Tipo contratto;

Livello/Profilo;

Dipendente S/N.

A completamento delle informazioni di una Persona, in ACE è stata
gestita l’\ **Appartenenza**.

La gestione dell’appartenenza riguarda l’assegnazione di una risorsa
alla sua sede di afferenza (Sede Amministrativa di riferimento) e alla
sua sede di lavoro (entità locale ove presta servizio) e la gestione di
tali informazioni che possono cambiare nel tempo.

La sede di afferenza e la sede di lavoro nella maggior parte dei casi
coincidono, sono invece diverse quando si parla di ‘assegnazione’
temporanea a una sede diversa da quella di appartenenza o di distacco /
mobilità temporanea.

Per quanto riguarda **l’assegnazione del personale alle Sedi** vengono
gestiti due ruoli specifici, precaricati e non modificabili, e definiti
in fase di immatricolazione (NSIP) o censimento del collaboratore
(Gestione Istituti):

AFFERENZA;

SEDE LAVORO;

Ogni Persona (Dipendente/non dipendente) avrà sicuramente in ACE questi
due ruoli definiti rispetto alle Sedi, con l’indicazione della data
inizio e fine di validità. Tali dati sono gestiti nelle procedure di
origine già indicate per la gestione delle persone e vengono riportati
in ACE con le stesse modalità indicate per le Persone.

4. **Ruoli**

Una delle funzionalità principali di ACE, al fine di centralizzare
informazioni comuni alle sedi e alle persone, è la Gestione dei Ruoli.

Fondamentalmente questa gestione si può distinguere in tre macrogruppi:

Ruoli di Sistema

Ruoli Istituzionali

Ruoli Applicativi

Le gestioni relative si riconducono ai relativi contesti, di cui abbiamo
parlato nella descrizione della funzionalità dei contesti.

I primi due, infatti, inclusi ognuno nel rispettivo contesto,
rappresentano Ruoli non modificabili dall’utente.

I primi sono ad uso esclusivo degli Amministratori di ACE.

I secondi sono utilizzabili dalla funzionalità di ‘Ruoli Assegnati’ per
gestione o solo per assegnazione a seconda del ruolo stesso dell’utente
ACE (vedi funzionalità dei contesti).

I ruoli Applicativi invece sono tutti quei ruoli di cui ha bisogno ogni
Applicazione esterna ad ACE per poter abilitare tutte le Persone a
svolgere le corrette operazioni all’interno dell’applicazione stessa.
Ogni applicazione esterna (equivalente ad un contesto ACE) interrogherà
ACE, per ogni utente che accede alla specifica applicazione, per
conoscere di quali ruoli dispone, siano essi Istituzionali o dello
specifico contesto.

La funzionalità ‘Ruoli Assegnati’ permette quindi, a seconda delle
abilitazioni, di assegnare ruoli a persone per la propria struttura/sede
(o tutte le strutture), per un determinato periodo di validità (data
inizio e fine), allegando lo specifico provvedimento o altri documenti
utili.

Questa funzionalità è utilizzabile anche direttamente dalla gerarchia
(ovviamente per le strutture abilitate e per i ruoli/contesti
abilitati).