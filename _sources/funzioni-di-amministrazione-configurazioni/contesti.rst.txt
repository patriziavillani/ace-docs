Contesti
========

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

-  Amministratore del contesto (Ruolo) – Chi ha assegnato questo ruolo è
   abilitato a creare, gestire e ad assegnare tutti i ruoli del
   contesto;

-  Gestore del contesto (Ruolo) – Chi ha assegnato questo ruolo è
   abilitato solo ad assegnare tutti i ruoli del contesto.

-  Il Contesto ‘SISTEMA’, che definisce i ruoli necessari al
   funzionamento di ACE, non è modificabile.

   5. .. rubric:: Ruoli
         :name: ruoli

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
