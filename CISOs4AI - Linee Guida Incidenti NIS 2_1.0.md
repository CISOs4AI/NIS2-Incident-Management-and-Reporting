# Linee Guida per la Gestione e Notifica degli Incidenti NIS 2

## Framework Comunitario Operativo per la

Classificazione e Gestione degli Incidenti di Sicurezza

Versione: 1.0

Data: 17 marzo 2026  

Licenza: Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)

Contributori: Comunità CISOs4AI

Team: **Christian Bassi**, **Giuseppe Maria Blasi**, Giovanni Cerrato, **Domenico Ciervo**, **Giacomo Conti**, **Gerardo Forliano**, Manuela Italia, Paolo Libardi, Alberto Maldino,  
**Gian Fabio Palmerini**, **Andrea Succi**, Marco Tedeschi, Nicola Tigri.

*Contributori chiave indicati in* ***Blu***

## Licenza e Utilizzo

Questo documento è rilasciato sotto licenza Creative Commons Attribuzione-CondividiAlloStessoModo 4.0 Internazionale (CC BY-SA 4.0).

Sei libero di:

* Condividere, riprodurre, distribuire questo materiale con qualsiasi mezzo e formato
* Modificare, remixare, trasformare il materiale e basarti su di esso
* Utilizzarlo per qualsiasi fine, anche commerciale

Alle seguenti condizioni:

* Attribuzione: Devi riconoscere una menzione di paternità adeguata (es. "Basato sulle Linee Guida NIS 2 della Comunità CISOs4AI, CC BY-SA 4.0")
* Stessa Licenza: Se remixi, trasformi il materiale o ti basi su di esso, devi distribuire i tuoi contributi con la stessa licenza dell'originale
* Nessuna restrizione aggiuntiva: Non puoi applicare termini legali o misure tecnologiche che impediscano ad altri di fare ciò che la licenza consente

Come contribuire:

1. Fork del repository ufficiale [https://github.com/CISOs4AI/NIS2-Incident-Management-and-Reporting/](https://github.com/CISOs4AI/NIS2-Incident-Management-and-Reporting/tree/main) .
2. Proposta di modifiche via Pull Request con motivazione allegata.
3. Review da parte della community CISOs4AI.
4. Approvazione e merge nella versione ufficiale.

Tipologie di contributi:

* Nuovi casi d’uso reali (anonimizzati).
* Aggiornamenti normativi (determinazioni ACN, circolari CSIRT).
* Template operativi.
* Traduzioni in altre lingue UE.
* Integrazioni settoriali specifiche.

Governance per i contributori: da definire (es. steering committee CISOs4AI e stakeholder).

## Prefazione

Il presente documento nasce dall'esperienza collettiva della comunità italiana CISOs4AI, costituita da cultori della cybersecurity per affrontare le complessità operative derivanti dall'applicazione della Direttiva NIS 2 (UE 2022/2555) e del relativo decreto di recepimento nazionale (D.Lgs. 4 settembre 2024, n. 138).

L'obiettivo è fornire un framework pragmatico che bilanci compliance normativa, difesa organizzativa e sostenibilità operativa, evitando sia over-reporting inefficace che under-reporting sanzionabile.

## Destinatari

* Chief Information Security Officers (CISO)
* Data Protection Officers (DPO)
* Responsabili IT e Compliance
* Consulenti legali in ambito cybersecurity
* Management di organizzazioni soggette a NIS 2 (essenziali e importanti)

## Principi Fondanti

1. **Gerarchia normativa vincolante**: la legge primaria (D.Lgs. 138/2024) prevale su determinazioni, FAQ e linee guida attuative
2. **Evidenza oggettiva**: classificazioni basate su metriche misurabili, non interpretazioni soggettive
3. **Integrazione GDPR**: coordinamento obblighi privacy e cybersecurity
4. **Difendibilità**: ogni decisione deve essere documentabile e giustificabile in sede di audit
5. **Collaborazione aperta**: condivisione conoscenza per innalzare maturità settoriale

## Disclaimer e Limitazioni

Il presente documento:

* È frutto di interpretazione collettiva e non costituisce parere legale vincolante.
* Ogni organizzazione deve adattare il framework al proprio contesto e appetito di rischio.
* I pesi degli assi di impatto e le soglie di Punteggio sono indicativi e richiedono calibrazione aziendale.
* In caso di dubbio, consultare sempre il legale interno e/o consulenti specializzati.
* Gli autori e i contributori non assumono responsabilità per decisioni prese basandosi esclusivamente su questo documento.

Raccomandazione: utilizzare questo documento come baseline, integrare con le policy aziendali specifiche e validare con Legal/DPO.

## Quadro Normativo di Riferimento

### Gerarchia delle Fonti Normative

1. Direttiva (UE) 2022/2555 (NIS 2) - Fonte normativa primaria (UE)
2. D.Lgs. 4 settembre 2024, n. 138 - Fonte normativa primaria (nazionale)
3. Regolamento (UE) 2016/679 (GDPR) - Fonte normativa primaria e nazionale (UE, ambito dati personali)
4. Determinazioni ACN (es. 379907/2025, 164179/2025) Fonte normativa attuativa (subordinata a livelli 1-2)
5. FAQ ACN, Linee Guida CSIRT Italia \& Interpretativa

**Principio interpretativo fondamentale**: in caso di contrasto tra livelli, prevale la fonte normativa superiore. Le determinazioni ACN e le FAQ sono strumenti applicativi che **non possono ampliare** gli obblighi definiti dal D.Lgs. 138/2024.

### Definizione Legale di "Incidente Significativo"

Il **D.Lgs. 138/2024, Art. 25, commi 1 e 4** stabilisce:

**Comma 1**: I soggetti essenziali e i soggetti importanti notificano, senza ingiustificato ritardo, al CSIRT Italia ogni incidente che, ai sensi del comma 4, **ha un impatto significativo** sulla fornitura dei loro servizi \[...]

**Comma 4**: Un incidente è considerato significativo se:

a) ha causato o è in grado di causare una **grave perturbazione operativa** dei servizi o **perdite finanziarie** per il soggetto interessato;

b) ha avuto ripercussioni o è idoneo a provocare ripercussioni su altre persone fisiche o giuridiche causando **perdite materiali o immateriali considerevoli**.

### Tassonomia ACN: Incidenti Significativi di Base (IS)

La Determinazione ACN 379907/2025 identifica quattro categorie di incidenti significativi di base per soggetti essenziali:

1. IS-1 \& Evidenza della perdita di riservatezza, verso l'esterno, di dati digitali di proprietà o sotto controllo del soggetto NIS
2. IS-2 \& Evidenza della perdita di integrità, con impatto verso l'esterno, di dati di proprietà o sotto controllo del soggetto NIS
3. IS-3 \& Evidenza della violazione dei livelli di servizio attesi (SLA) definiti ai sensi della misura DE.CM-01
4. IS-4 \& Evidenza di accesso non autorizzato o abuso di privilegi a dati digitali di proprietà o sotto controllo del soggetto NIS

### Risoluzione del potenziale contrasto tra definizione di legge di “incidente significativo” e categorie di “incidenti significativi”

Secondo i criteri di cui all'Art. 25.4 l'obbligo di notifica sussiste **solo in presenza di impatto significativo** con impatti operativi, finanziari o perdite materiali o immateriali rilevanti.

La determina indica quattro categorie di incidenti significativi da segnalare. Le due fonti non sono in contrasto. La determina infatti non richiede una notifica "indipendentemente dall'impatto" (notifica che sarebbe priva di base legale e contestabile) ma è evidentemente una notifica di un incidente significativo che rispetta i criteri dell’Art. 25.4 e che rientri in una delle categorie sotto individuate.

Le categorie IS-1, IS-2, IS-3, IS-4 sono pertanto **strumenti di classificazione**, **non sostituiscono** il requisito legale di "impatto significativo" ex Art. 25.4.

Per esempio, una password dismessa su leak è un evento classificato IS-1 ma **non è notificabile** se privo di impatto operativo/finanziario/su terzi.

### Integrazione con GDPR

La gestione degli incidenti deve coordinare obblighi NIS 2 e GDPR. Gli incidenti con dati personali richiedono valutazione parallela NIS 2 + GDPR. La notifica a CSIRT Italia non sostituisce la notifica al Garante Privacy e viceversa.

Da questo punto di vista eventi dove si sospetta siano coinvolti dati personali devono essere notificati al DPO o alle strutture preposte alla compliance delle tematiche Privacy per opportuna valutazione dell’incidente.

### Protocollo di Gestione Incidenti Multilivello (NIS 2 / GDPR)

L’entrata in vigore della Direttiva **NIS 2** (D.Lgs. di recepimento) impone un’architettura di risposta agli incidenti che integri, senza sovrapposizioni, i dettami del **Regolamento UE 2016/679 (GDPR)**. La gestione delle crisi cibernetiche non dovrebbe essere un silos stagno, ma deve operare secondo un principio di **valutazione parallela, contestuale e coordinata**.

La NIS2 e il GDPR presidiano, infatti, sfere e interessi diversi che, lungi dal sovrapporsi, devono coordinarsi in quanto un incidente può impattare, potenzialmente, i beni giuridici protetti da entrambe le norme.

E’ necessario che le procedure operative aziendali dialoghino fra di loro e che siano ben definiti ruoli operativi aziendali e compiti.

Le logiche e l’analisi del rischio del breach delle normative segue, però, logiche diverse fra loro, solo all’apparenza incompatibili.

#### I Pilastri del Coordinamento:

1. **Dualità delle Notifiche:** La notifica dell'incidente al **CSIRT Italia** (per profili di resilienza infrastrutturale) **non esonera** l'ente dall'obbligo di notifica al **Garante per la Protezione dei Dati Personali**, qualora l'evento integri una violazione di dati (*Data Breach*) che presenti rischi per gli interessati, e viceversa.

Laddove la violazione non interessi dati personali o sia improbabile che si verifichino rischi per le persone fisiche coinvolte nel trattamento, la violazione, ai sensi del GDPR potrebbe essere archiviata secondo le politiche aziendali (previa consultazione del DPO). Tuttavia, potrebbe essere comunque necessario procedere con la notifica al CSIRT ai sensi della Direttiva NIS2.

1. **Escalation Procedurale nella NIS2:** A differenza del GDPR, che prevede una notifica "secca" entro 72 ore, la NIS 2 introduce un protocollo a tappe forzate per garantire la gestione della crisi in tempo reale.
2. **L’Allarme Precoce (Early Warning) – Entro 24 ore:** È la fase più critica. L’organizzazione deve comunicare al CSIRT Italia (presso l'ACN - Agenzia per la Cybersicurezza Nazionale) se l'incidente è sospettato di avere un impatto significativo.Non servono prove certe, basta il sospetto. Il ritardo qui è la prova della "colpa grave" dell'amministratore.
3. **La Notifica dell’Incidente – Entro 72 ore:** In questo contesto si devono aggiornare le informazioni, fornendo una valutazione iniziale sulla gravità, l'impatto e gli "indicatori di compromissione".

#### La differenza delle notifiche GDPR e NIS2

Un incidente ai sensi della NIS 2 può coincidere con un Data Breach del GDPR, ma i destinatari e i contenuti sono diversi.

Ogni evento di sicurezza che presenti anche solo il sospetto di una compromissione di dati personali deve attivare i processi aziendali per la gestione degli incidenti e attivare un flusso informativo immediato verso il **DPO** o le unità di *Privacy Compliance*.

**Il Risk Assessment Integrato:** La valutazione dell'incidente deve essere binaria e riguardare, **lato NIS 2,** l’impatto sulla continuità del servizio e sulla sicurezza delle reti e lato GDPR, il rischio per i diritti e le libertà delle persone fisiche.

## Framework di Classificazione a Due Livelli

### Metodologia di Valutazione

**Il processo di classificazione si articola in due livelli sequenziali obbligatori:**

#### Livello 1 - Valutazione Impatto Sostanziale (Art. 25.4 D.Lgs. 138/2024)

Verifica se l'incidente soddisfa **almeno uno** dei seguenti criteri:

1\. Grave perturbazione operativa dei servizi a perimetro NIS 2

2\. Perdite finanziarie per il soggetto

3\. Ripercussioni su persone fisiche/giuridiche con perdite materiali o immateriali considerevoli

Se Livello 1 = NEGATIVO → Incidente NON significativo → NESSUNA notifica NIS 2 obbligatoria

#### Livello 2 - Classificazione Tassonomia ACN (IS-1/IS-2/IS-3/IS-4)

Solo se Livello 1 = POSITIVO, classificare secondo tassonomia ACN per determinare modalità di notifica.

### Assi di Impatto per Livello 1

Per determinare oggettivamente la presenza di "impatto significativo", si valutano assi quantitativi/qualitativi.

A seguire si riportano sei assi a titolo illustrativo o come proposta di miglioramento. I pesi e le soglie sono **indicativi** e devono essere calibrati sull'appetito di rischio organizzativo.

È consigliabile l’allineamento degli stessi al Information Security Risk Management e idealmente Enterprise Risk Management affinchè la significatività ai sensi NIS 2 coincida con la significatività del business.

#### Asse 1: Impatto Operativo

1. **Trascurabile:** Il ripristino avviene nei tempi previsti, senza alcuna conseguenza sugli asset o sulle operazioni aziendali. Nessun impatto rilevante sulla continuità operativa.
2. **Basso:** Il superamento dei tempi di ripristino coinvolge asset di importanza intermedia(tier 3) e produce effetti limitati e generalmente risolvibili senza impatti significativi sulle attività.
3. **Medio:** Il ritardo interessa asset di importanza elevata (tier 2) con effetti moderati sull’operatività. Può comportare una temporanea riduzione dell’efficienza, ma senza danni irreparabili. L’incidente non ha impatti diretti nell’erogazione di servizi essenziali o importanti secondo quello che è il perimetro NIS.
4. **Alto:** Riguarda ritardi nei tempi di ripristino che impattano asset di massima importanza (tier 1), con una riduzione consistente della capacità operativa e potenziali perdite rilevanti. L’azione correttiva è prioritaria.
5. **Critico:** Si verifica quando il mancato rispetto dei tempi di ripristino coinvolge asset di massima importanza (tier 1), causando gravi conseguenze per la continuità operativa e possibili ripercussioni economiche e reputazionali significative. Richiede intervento immediato.

La valutazione viene effettuata considerando la violazione degli SLA, il degrado della disponibilità e la durata dell'interruzione, con una ponderazione basata sul livello di criticità degli asset coinvolti. Si riporta un esempio esemplificativo di clusterizzazione di asset sulla base di tier a seguire

|Asset Tier|Descrizione|RTO (esemplificativo)|
|-|-|-|
|Tier 1|Sistemi mission-critical che sostengono servizi essenziali (Mission critical)|<4 ore|
|Tier 2|Sistemi importanti per operatività business (Business Operational)|4-24 ore|
|Tier 3|Sistemi non critici (Business Non-essential)|24-48 ore|
|Tier 4|Sistemi di supporto (Support Services)|>48 ore|

Per il criterio IS-3 risulta inoltre necessario comprendere se l’evento porta ad una violazione degli SLA definiti in coerenza con la misura DE.CM-01 ACN (SLA attesi).

#### Asse 2: Impatto Economico

1. Trascurabile: Impatto stimato < 0,002% del fatturato annuo; riduzione/ incremento trascurabile.
2. Basso: Impatto stimato ≥ 0,002% e < 2%; riduzione attesa dei ricavi/incremento atteso dei costi minore.
3. Medio: Impatto stimato ≥ 2% e < 4%; riduzione attesa dei ricavi/incremento atteso dei costi medio.
4. Alto: Impatto stimato ≥ 4% e ≤ 10%; riduzione attesa dei ricavi/incremento atteso dei costi rilevante.
5. Critico: Impatto stimato > 10%; riduzione attesa dei ricavi/incremento atteso dei costi critico.

Nel caso sopra abbiamo usato una percentuale del valore del fatturato (come fanno le sanzioni del GDPR e della NIS 2) ma possono essere anche indicati valori assoluti o percentuali del EBITDA o altri parametri finanziari oggettivi che permettano di valutare la materialità dell'impatto stesso. Le stesse soglie percentuali possono essere adattate alla dimensione organizzativa e all’appetito al rischio della stessa.

Ai sensi del Regolamento di esecuzione (UE) 2024/2690 della Commissione del 17 ottobre 2024, qualora l’organizzazione rientri tra i soggetti pertinenti (es. fornitori di servizi DNS, registri TLD, cloud computing o data center), ai fini della qualificazione di “incidente significativo” si applica anche il criterio economico per cui l’incidente è considerato significativo se ha causato o è in grado di causare una perdita finanziaria diretta superiore a 500.000 EUR o, se tale importo è inferiore, superiore al 5% del fatturato totale annuo dell’esercizio precedente; in tali casi si raccomanda di considerare la soglia come livello "Alto", indipendentemente da eventuali soglie interne calibrate tramite BIA/ERM.

#### Asse 3: Impatto su Persone

1. Trascurabile: Nessun impatto su persone o salute.
2. Basso: Impatto su singoli individui, nessuna conseguenza sanitaria.
3. Medio: Coinvolgimento di più persone (<% degli utenti o dipendenti), con disagio o lieve danno.
4. Alto: Coinvolgimento ampio (10–50% degli utenti o dipendenti) o rischio moderato alla salute.
5. Critico: Pericolo vita/salute grave o >50% degli utenti o dipendenti impattati.

Anche in questo caso, le soglie percentuali devono essere adattate in base alla dimensione dell'azienda, della clientela impattata o in generale dagli stakeholder potenzialmente impattati (es.% clienti totali ultimi 12m via CRM).

#### Asse 4: Impatto di Riservatezza dei Dati

1. Trascurabile: Nessun impatto; dati pubblici o assenza di dati personali.
2. Basso: Dati a uso interno, pseudonimizzati o aggregati.
3. Medio: Dati personali comuni (<1000 interessati).
4. Alto: Dati riservati/confidenziali o dati personali alto rischio (>1000 interessati).
5. Critico: Dati appartenenti a categorie particolari ex art. 9 GDPR\* o segreti commerciali.

\*Categorie particolari Art. 9 GDPR: origine razziale/etnica, opinioni politiche, convinzioni religiose/filosofiche, appartenenza sindacale, dati genetici/biometrici, dati sanitari, vita sessuale/orientamento.

Nota: non tutti gli incidenti di sicurezza integrano una violazione di dati personali ai sensi del GDPR, mentre tutte le violazioni di dati personali presuppongono tendenzialmente il verificarsi di un incidente di sicurezza (che tuttavia potrebbero non essere informatiche e quindi non a perimetro NIS 2). Pertanto, la violazione Privacy si pone come conseguenza dei più gravi incidenti di sicurezza. Il GDPR definisce come violazione dei dati personali una violazione di sicurezza che comporta accidentalmente o in modo illecito la distruzione, la perdita, la modifica, la divulgazione non autorizzata o l'accesso ai dati personali trasmessi, conservati o comunque trattati.

Ne consegue che quando l’organizzazione rileva oppure viene informata di un incidente di sicurezza deve stabilire se si è verificata o meno una violazione dei dati personali, sorgono specifici obblighi che riguardano sia la documentazione che la gestione della violazione che sono descritti in maniera più dettagliata nel prosieguo del documento.

#### Asse 5: Impatto Reputazionale

1. Trascurabile: Nessun impatto reputazionale.
2. Basso: Perdita d’immagine contenuta, limitata al contesto interno.
3. Medio: Perdita d’immagine percepita da singoli clienti o partner.
4. Alto: Danno d’immagine rilevante a livello nazionale.
5. Critico: Immagine compromessa a livello nazionale/internazionale.

#### Asse 6: Incidente Ricorrente

1. Basso: Primo evento di questo tipo
2. Alto: Incidente stesso tipo/causa root già verificato in 6 mesi

Nota: la ricorrenza indica potenziali carenze processi remediation, elemento potenzialmente aggravante per valutazione dell'evento.

### Punteggio Totale e Trigger Notifica

Il Punteggio Totale non può che considerare quanto riportato nel D.Lgs. 138/2024, Art. 25, commi 1 e 4.

La formula a seguire fa in modo che vengano ritenuti incidenti significativi quelli con: grave perturbazione operativa dei servizi (Asse 1), perdite finanziarie/materiali (Asse 2) ripercussioni su persone (Asse 3) e perdite immateriali (Asse 5).

Inoltre, anche se non richiamato direttamente dal D.Lgs. 138/2024, Art. 25 si ritiene che anche una perdita di riservatezza (Asse 4) possa avere un impatto materiale o immateriale.

A seguire è riportata la formula del **Punteggio Totale Assoluto (PTA)**.

**PTA NIS 2 = MAX (Asse 1, Asse 2, Asse 3, Asse 4, Asse 5)**

La severità complessiva dell’incidente si determina dal valore più alto tra tutte le matrici di impatto. La valutazione della severità è riportata nella tabella seguente:

|PTA|Severità|Descrizione impatto|
|-|-|-|
|5|CRITICO|Compromissione estesa dei servizi essenziali (Asse 1), con grave perturbazione operativa e interruzione prolungata delle attività. Perdite finanziarie o materiali ingenti (Asse 2), come danni economici diretti o indiretti, costi di ripristino e possibili sanzioni. Danni rilevanti a persone (Asse 3), che possono includere rischi per la sicurezza fisica, salute o benessere degli individui coinvolti. Perdita significativa di riservatezza e integrità dei dati (Asse 4), con esposizione di informazioni sensibili o personali e possibile violazione della privacy. Ripercussioni immateriali profonde (Asse 5), quali danni reputazionali, perdita di fiducia da parte di clienti e stakeholder, impatto sull’immagine aziendale e possibili effetti sistemici a livello nazionale o internazionale.|
|4|ALTO|Impatto rilevante sui processi operativi (Asse 1), con possibili interruzioni delle attività principali e della catena di fornitura. Perdite finanziarie o materiali significative (Asse 2), con costi elevati per la gestione dell’incidente e possibili danni patrimoniali. Danni alle persone (Asse 3), come disagio o rischio per la salute e la sicurezza, anche se non critici. Violazione della riservatezza dei dati (Asse 4), con esposizione di dati sensibili o personali a rischio. Ripercussioni immateriali estese (Asse 5), quali danni reputazionali, perdita di credibilità e rischi di sanzioni normative rilevanti.|
|3|MEDIO|Impatto gestibile sui servizi (Asse 1), con possibili interruzioni temporanee o limitate. Perdite finanziarie/materiali moderate (Asse 2), con costi contenuti e facilmente assorbibili. Conseguenze per le persone (Asse 3) di lieve entità, con rischio basso per la sicurezza o il benessere. Possibile perdita di riservatezza dei dati (Asse 4), ma senza esposizione massiva. Ripercussioni immateriali (Asse 5) circoscritte, come impatti limitati su reputazione e compliance, con potenziale escalation se non gestito adeguatamente.|
|2|BASSO|Effetti limitati su servizi (Asse 1), con brevi interruzioni o rallentamenti facilmente gestibili. Perdite finanziarie/materiali contenute (Asse 2), senza impatti significativi sul bilancio. Conseguenze minime per le persone (Asse 3), senza rischi per la sicurezza o la salute. Possibile perdita di riservatezza (Asse 4) senza esposizione di dati critici. Ripercussioni immateriali (Asse 5) quasi nulle, con impatti marginali su reputazione e compliance.|
|1|TRASCURABILE|Impatto trascurabile su servizi (Asse 1), senza interruzioni significative. Perdite finanziarie/materiali assenti o minime (Asse 2). Nessuna conseguenza per le persone (Asse 3), con sicurezza e salute pienamente garantite. Nessuna perdita di riservatezza (Asse 4) o coinvolgimento di dati sensibili. Ripercussioni immateriali (Asse 5) nulle, senza alcun impatto su reputazione o conformità normativa.|

È possibile considerare la ricorrenza degli eventi usando l’Asse 6 come coefficiente booleano. Questo fa in modo che vengano segnalati incidenti ricorrenti di gravità minore che altrimenti non sarebbero notificati

Una formula di esempio del **Punteggio Totale Nettato Ricorsività (PTNR)** è riportata a seguire:

**PTNR NIS 2 = PTA NIS 2 + Asse 6**

Trigger Segnalazione NIS 2: effettuata quando il punteggio >=4 ovvero quando anche solo uno di questi parametri ha un impatto alto.

Nella formula PTNR di fatto un valore booleano forza l’upgrade di eventi con PTA = 3 per segnalazione.

**PT GDPR = Asse 4 \* presenza dati personali (valore booleano 0-1)**

Trigger Notifica al Garante della privacy: deve essere valutata con punteggio >=4 **E sono impattati Dati Personali**

## Workflow Decisionale Operativo

### Processo di Gestione Incidente (Incident Response)

A seguire si riporta un esempio di flusso decisionale per la classificazione degli incidenti ai fini NIS 2.

Step 1: Rilevamento e Triage Iniziale (0-2h)

* Security Operations Center (SOC) / IT rileva un evento anomalo.
* Apertura ticket incidente con timestamp iniziale.
* Classificazione preliminare: security event, incident, crisis.
* Attivazione team di Incident Response se incident confermato.

Step 2: Valutazione Impatto (2-12h)

* Applicazione delle matrici degli assi di impatto 1-6.
* Calcolo del PT e verifica dei trigger.
* Checkpoint Livello >4?

  * NO → Registrazione su log interno, gestione BAU, monitoraggio evoluzione.
  * SÌ → Proseguire con Step 3.

Step 3: Classificazione secondo Tassonomia ACN (12-18h)

* Mappatura sulle categorie IS-1, IS-2, IS-3, IS-4.
* Checkpoint Livello 2: l’evento rientra in una categoria IS-X?

  * NO → Caso borderline, escalation a CISO / Legal / DPO.
  * SÌ → Incidente significativo confermato, proseguire con Step 4.

Step 4: Valutazione Parallela GDPR (contestuale a Step5)

* Verifica se sono coinvolti dati (Asse 4 >= 4).
* Confermare presenza dati personali.
* Se entrambe le condizioni sono soddisfatte → Attivazione parallela del processo di notifica al Garante Privacy : eEscalation a DPO per valutazione del rischio per i diritti e le libertà delle persone (Art. 33 GDPR). Coordinamento con il DPO per la comunicazione agli interessati (Art. 34 GDPR in caso di alto rischio).

Step 5: Notifica a CSIRT Italia (24h / 72h / 30gg)

* T+24h: Early Warning (natura incidente, impatto preliminare, indicatori malevoli o transfrontalieri).
* T+72h: Notifica dettagliata (valutazione gravità, IoC, impatto stimato, misure immediate adottate).
* T+30gg: Report finale (root cause analysis, misure correttive, raccomandazioni).

Il referente CSIRT prepara/invia a CSIRT Italia queste notifiche che sono approvate da CISO.

Step 6: Documentazione e Lessons Learned

* Registrazione completa della timeline decisionale.
* Archiviazione delle evidenze relative alla valutazione dell’impatto.
* Aggiornamento del registro storico degli incidenti.
* Review post-incident per il miglioramento continuo dei processi.

### Escalation e Ruoli

Non sono oggetto di questo documento la definizione della struttura organizzativa; pertanto quanto riportato A SEGUIRE deve essere adattato all’organizzazione aziendale.

SOC/IT

* Responsabilità: rilevamento, triage iniziale, classificazione preliminare.
* Trigger di escalation: incidente confermato.

CISO (o figura analoga responsabile della sicurezza delle informazioni)

* Responsabilità: valutazione impatto, decisione di notifica, coordinamento stakeholder.

Referente CSIRT

* Responsabilità: invio notifiche Portale CSIRT, gestione follow-up/req info ACN, consultazioni con CISO pre-notifica per borderline
* Trigger di notifica: chiara casistica di incidente (PTNR NIS >=4)

DPO

* Responsabilità: valutazione GDPR, notifica al Garante, comunicazione agli interessati.
* Trigger di escalation: presenza di dati personali e rischio per i diritti e le libertà.

Legal

* Responsabilità: supporto in interpretazione normativa, difesa in ispezioni, gestione sanzioni.
* Trigger di escalation: casi borderline.

Business Owners (e.g. CFO, COO)

* Responsabilità: valutazione impatto operativo/finanziario, decisioni su continuità del servizio.
* Trigger di escalation: servizio critico degradato o interrotto.

Board / CEO

* Responsabilità: approvazione comunicazioni esterne, gestione crisi reputazionale.
* Trigger di escalation: impatti critici.

### Gestione Casi Borderline

Per gli incidenti in “zona grigia” si applica il principio di precauzione documentata.

1. Escalation obbligatoria verso CISO, Legal e DPO (se impattati dati personali).
2. Valutazione contestuale con il Business Owner sull’impatto reale sui servizi.
3. Analisi dei trend per capire se si tratta di incidente isolato o pattern ricorrente.
4. Eventuale consultazione informale con CSIRT Italia, se disponibile, per ottenere indicazioni operative.
5. Decisione formalizzata con motivazione scritta:

   1. Notifica, in presenza di dubbio ragionevole sull’evoluzione dell’impatto.
   2. Non notifica, se le evidenze oggettive escludono l’applicabilità dell’Art. 25.4 (documentare la motivazione).
6. Monitoraggio attivo per 48 ore successive all’evento, con riclassificazione se l’impatto evolve.

Regola aurea: “When in doubt, document out”. La difendibilità dipende dalla tracciabilità della decisione, non dalla perfezione della classificazione.

## Documentazione e Audit-Proofing

### Registro Incidenti Obbligatorio

È necessario mantenere un registro completo di tutti gli eventi, significativi e non, per poter dimostrare la corretta valutazione in sede di ispezione.

Campi minimi del registro:

* ID univoco progressivo.
* Data e ora di rilevamento e di chiusura.
* Descrizione sintetica dell’evento.
* Fonte del rilevamento (alert SOC, segnalazione utente, scansione, e così via).
* Asset o servizi impattati.
* Valutazione degli assi di impatto 1-6 (punteggi numerici).
* Trigger NIS o GDPR eventualmente attivi.
* Classificazione Livello 1: presenza di impatto rilevante ai sensi Art. 25.4 (Sì/No).
* Classificazione Livello 2: categoria IS-X (se applicabile).
* Decisione finale: Notifica, Non notifica, Escalation.
* Motivazione della decisione (testo libero con riferimenti normativi – particolarmente rilevante qualora ci si trovi in caistiche borderline).
* Responsabile della decisione (CISO, playbook, team IR, altro).
* Azioni correttive adottate.
* Stato (Aperto, Contenimento, In gestione, Chiuso).
* Flag GDPR: presenza di dati personali (Sì/No), notifica al Garante (Sì/No).

Si raccomanda di integrare i campi NIS2 nei registri di incident management e/o privacy esistenti, evitando duplicazioni, eventualmente aggiungendo un flag “NIS 2”.

Tempo minimo di conservazione suggerito: almeno 5 anni, in linea con la prescrizione delle sanzioni amministrative.

## Annex 1 - Casi d’Uso Pratici

### Caso 1: Password Dismessa su Leak Pubblico

Scenario: il SOC rileva cinque credenziali di accesso aziendali presenti su un dump pubblicato su servizi tipo HaveIBeenPwned.

Analisi:

* Verifica: account relativi a un sistema decommissionato da 8 mesi, già disabilitati.
* Asse 1 (Continuità): 0 (nessun servizio attivo).
* Asse 2 (Economico): 0 (nessun costo).
* Asse 3 (Persone): 0 (nessun utente impattato).
* Asse 4 (Dati): 1 (dati a uso interno, account dismessi).
* Asse 5 (Ricorrenza): 0 (primo evento di questo tipo).
* Asse 6 (Reputazionale): 0 (nessun impatto reputazionale).
* PTNR NIS: 1.
* PT GDPR: 1
* Trigger: nessuno.
* Classificazione ACN: potenziale IS-1 per perdita di riservatezza, ma assenza di impatto ai sensi dell’Art. 25.4.

Decisione: Non notifica. L’evento non è significativo. Registrazione su log interno e monitoraggio.

Azione GDPR: valutazione del DPO che esclude rischi per i diritti e le libertà, quindi nessuna notifica al Garante.

### Caso 2: Ransomware su Sistema di Produzione Critico

Scenario: ransomware che cifra il server ERP aziendale con blocco della produzione.

Analisi:

* Asse 1 (Continuità): 4 (servizio essenziale fermo per più di 72 ore, stimato).
* Asse 2 (Economico): 3 (perdita produzione di circa 600.000 euro al giorno).
* Asse 3 (Persone): 3 (< 10% dipendenti obbligati a lavorare in maniera inefficiente).
* Asse 4 (Dati): 3 (dati riservati ERP, senza dati personali).
* Asse 5 (Ricorrenza): 0 (primo episodio di ransomware).
* Asse 6 (Reputazionale): 2 (potenziale impatto su clienti).
* PTNR NIS: 4
* PT GDPR: 0
* Trigger: impatto forte su continuità, impatto economico e origine malevola.
* Classificazione ACN: IS-2 (integrità) e IS-3 (violazione SLA).

Decisione: Notifica obbligatoria a CSIRT Italia.

* Early Warning a T+24h con descrizione sintetica dell’incidente, impatto sulla produzione, entità economica, indicazioni preliminari sulla minaccia e sull’eventuale natura transfrontaliera.
* Notifica dettagliata a T+72h con IoC, timeline, misure di contenimento e ripristino.
* Report finale a T+30gg con root cause, misure correttive (ad esempio hardening, MFA, EDR, backup offsite) e lessons learned.

Azione GDPR: assenza di dati personali critici, quindi nessuna notifica al Garante Privacy.

### Caso 3: Esfiltrazione Dati Sanitari di Pazienti

Scenario: accesso abusivo a un database di cartelle cliniche con esportazione di 2500 record. Un ulteriore accesso è stato riscontrato 3 mesi prima dell’evento in questione.

Analisi:

* Asse 1 (Continuità): 1 (servizio sanitario operativo, accesso non autorizzato rilevato e bloccato entro circa 4 ore).
* Asse 2 (Economico): 2 (costi stimati per notifica e assistenza ai pazienti pari a 150.000 euro).
* Asse 3 (Persone): 4 (2500 pazienti coinvolti).
* Asse 4 (Dati): 5 (dati sanitari ai sensi dell’Art. 9 GDPR).
* Asse 5 (Ricorrenza): 2.
* Asse 6 (Reputazionale): 4 (alto rischio di esposizione mediatica, settore sanitario).
* PTNR NIS: 6
* PT GDPR: 4
* Trigger: dati sanitari (GDPR) e impatto reputazionale (NIS 2)
* Classificazione ACN: IS-1 (riservatezza) e IS-4 (accesso non autorizzato).

Decisione: Notifica a CSIRT Italia e notifica al Garante Privacy.

NIS 2:

* Early Warning a T+24h.
* Notifica dettagliata a T+72h.
* Report finale a T+30gg con analisi dettagliata e misure correttive.

GDPR:

* Notifica al Garante entro 72 ore ai sensi dell’Art. 33.
* Comunicazione diretta ai pazienti entro 96 ore ai sensi dell’Art. 34, per l’alto rischio legato ai dati sanitari.
* Contenuti: natura della violazione, misure di mitigazione, raccomandazioni, contatti del DPO.

### Caso 4: Violazione SLA per Attacco DDoS (Borderline)

Scenario: Attacco DDoS che degrada il portale e-commerce in orario notturno con disponibilità al 85% per 6 ore (SLA garantito 99,5%).

Analisi:

* Asse 1 (Continuità): 3 (servizio degradato per 6 ore).
* Asse 2 (Economico): 1 (perdita vendite stimata di 30.000 euro).
* Asse 3 (Persone): 2 (circa 300 clienti impattati con disagio temporaneo).
* Asse 4 (Dati): 0 (nessun dato compromesso).
* Asse 5 (Ricorrenza): 2.
* Asse 6 (Reputazionale): 1 (qualche lamentela clienti ma contenute).
* PTNR NIS: 3
* PT GDPR: 0
* Trigger: Nessuno (origine malevola ma impatto limitato).
* Classificazione ACN: IS-3 (violazione SLA).

Decisione: Escalation verso CISO, Legal e Business Owner.

Valutazione contestuale:

* SLA violato ma recupero rapido (meno di 8 ore).
* Nessun danno materiale a terzi.
* Attacco DDoS mitigato con successo (infrastruttura resiliente).
* Conclusione: impatto non “grave” ai sensi dell’Art. 25.4.a (perturbazione contenuta).

Decisione finale: Non notifica. Caso borderline ma sotto la soglia legale.

Documentazione dettagliata della motivazione e monitoraggio di pattern futuri (se ricorrente l’attivazione dell’Asse 5 porterà a segnalazione).

### Caso 5: Phishing Utente Controllata (Servizi Posta O365)

Scenario: Azienda NIS2 Importante (provider O365 tenant multi-dominio per controllate non-NIS2). Utente di azienda controllata clicca URL malevolo → potenziale compromissione tenant condiviso. Analisi IR: nessun exploit confermato, no impatto servizi. Remediation condotta tempestivamente (password reset, MFA check, awareness training effettuata).

Analisi Assi:

* Asse 1 Continuità: 1 (nessun downtime tenant).
* Asse 2 Economico: 1 (costo irrisorio investigazione).
* Asse 3 Persone: 1 (singolo utente esterno, no danno).
* Asse 4 Dati: 2 (potenziale accesso credenziali, dati uso interno).
* Asse 5 Ricorrenza: 1 (primo phishing simile).
* Asse 6 Reputazionale: 1 (locale, no leak).
* PTNR NIS2: 2
* PT GDPR: 0 (no dati personali interessati confermati).
* Classificazione ACN: Potenziale IS-4 (accesso non autorizzato/abuso privilegi), ma zero impatto significativo Art.25.4 (no perturbazione servizi, no perdite terzi).

Decisione: Non notifica. L’evento non è significativo. Registrazione su log interno e monitoraggio.

Azione GDPR: Escalation DPO tenant che esclude rischi per i diritti e le libertà, quindi nessuna notifica al Garante.

## Annex 2 - Glossario

* ACN: Agenzia per la Cybersicurezza Nazionale, autorità competente NIS 2 in Italia.
* CSIRT Italia: Computer Security Incident Response Team nazionale, punto di contatto per le notifiche di incidenti.
* DPO: Data Protection Officer, responsabile della protezione dei dati personali (GDPR).
* Early Warning: Notifica preliminare entro 24 ore dall’awareness dell’incidente (NIS 2).
* GDPR: General Data Protection Regulation, Regolamento (UE) 2016/679.
* Incidente Significativo: Evento con impatto rilevante sui servizi secondo l’Art. 25.4 D.Lgs. 138/2024.
* IS-1/IS-2/IS-3/IS-4: Categorie di base degli incidenti significativi (tassonomia ACN).
* NIS 2: Network and Information Security Directive 2, Direttiva (UE) 2022/2555.
* SOC: Security Operations Center, centro operativo di sicurezza.
* Soggetto Essenziale: Entità dei settori ad alta criticità (energia, trasporti, sanità, ecc.) – Allegati I-II D.Lgs. 138/2024.
* Soggetto Importante: Entità dei settori critici secondari (ICT, food, manufacturing, ecc.) – Allegati III-IV D.Lgs. 138/2024.

