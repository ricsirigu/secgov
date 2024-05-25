## Overview

Ogni utente e azienda online dovrebbe prepararsi all'ondata imminente di potenti applicazioni di intelligenza artificiale generativa (GenAI). La GenAI ha un enorme potenziale di innovazione, efficienza e successo commerciale in diversi settori. Tuttavia, come qualsiasi tecnologia potente nelle sue fasi iniziali, presenta una serie di sfide evidenti e inaspettate.

Negli ultimi 50 anni, l'intelligenza artificiale ha compiuto progressi enormi, supportando discretamente una varietà di processi aziendali finché l'apparizione pubblica di ChatGPT non ha spinto lo sviluppo e l'utilizzo di modelli di linguaggio di grandi dimensioni (LLM) tra utenti e imprese. Inizialmente, queste tecnologie erano limitate agli studi accademici o all'esecuzione di attività specifiche ma vitali all'interno delle aziende, note solo a pochi eletti. Tuttavia, i recenti progressi nella disponibilità di dati, potenza di calcolo, capacità di GenAI e il rilascio di strumenti come Llama 2, ElevenLabs e Midjourney hanno portato l'intelligenza artificiale da una nicchia ad un'accettazione diffusa e generalizzata. Questi miglioramenti non solo hanno reso le tecnologie GenAI più accessibili, ma hanno anche evidenziato la necessità critica per le imprese di sviluppare strategie solide per integrare e sfruttare l'intelligenza artificiale nelle loro operazioni, rappresentando un enorme passo avanti nel modo in cui utilizziamo la tecnologia.

L'intelligenza artificiale è un termine ampio che comprende tutti i campi dell'informatica che consentono alle macchine di svolgere compiti che normalmente richiederebbero intelligenza umana. L'apprendimento automatico e l'intelligenza artificiale generativa sono due sottocategorie dell'IA.
L'apprendimento automatico (Machine Learning) è un sottoinsieme dell'IA che si concentra sulla creazione di algoritmi in grado di imparare dai dati. Questi algoritmi vengono addestrati su un set di dati e successivamente possono utilizzare tali informazioni per effettuare previsioni o decisioni su nuovi dati.
L'intelligenza artificiale generativa è un tipo di apprendimento automatico che si concentra sulla creazione di nuovi dati. Spesso, la GenAI si basa sull'utilizzo di modelli di linguaggio di grandi dimensioni (LLM) per svolgere le attività necessarie per creare nuovi dati.
Un modello di linguaggio di grandi dimensioni (LLM) è un tipo di modello di intelligenza artificiale che elabora e genera testo simile a quello umano. Nel contesto dell'intelligenza artificiale, un "modello" si riferisce a un sistema addestrato a fare previsioni basate su dati di input. Gli LLM sono specificamente addestrati su set di dati di linguaggio naturale di grandi dimensioni, da cui deriva il loro nome.

Le aziende si stanno addentrando in un territorio inesplorato per quanto riguarda la sicurezza e la supervisione delle soluzioni GenAI. Il rapido progresso della GenAI apre le porte anche agli attori malevoli per migliorare le loro strategie di attacco, introducendo una duplice sfida di difesa ed escalation delle minacce.

Le imprese utilizzano l'intelligenza artificiale in molte aree, tra cui le risorse umane per il recruiting, il filtraggio dello spam delle e-mail, i SIEM per l'analisi comportamentale e le applicazioni di rilevamento e risposta gestite (MDR). Tuttavia, questo documento si concentra principalmente sulle applicazioni dei modelli di linguaggio di grandi dimensioni e sulla loro funzione nella creazione di contenuti.

### Intelligenza Artificiale Responsabile e Affidabile

Con l'emergere di sfide e benefici dell'Intelligenza Artificiale (IA) - e con l'approvazione di normative e leggi - i principi e i pilastri di un utilizzo responsabile e affidabile dell'IA stanno passando dall'essere obiettivi e preoccupazioni teoriche a standard consolidati.

L'OWASP AI Exchange Working Group sta monitorando questi cambiamenti e affrontando le considerazioni più ampie e complicate per tutti gli aspetti dell'intelligenza artificiale.

![Fig_1_1](images/GOV1_Fig_1_1.png)

##### Figure 1.1  Pilastri della Intelligenza Artificiale Responsabile e Affidabile
##### creata dal Montreal Ethics Institute 

### A chi è rivolto questo documento?

La OWASP Top 10 for LLM Applications Cybersecurity and Governance Checklist è rivolta a leader in ambito aziendale, tecnologico, di sicurezza informatica, privacy, compliance e legale, nonché a team DevSecOps, MLSecOps e team di difesa informatica. Si rivolge a coloro che si sforzano di rimanere al passo nel mondo dell'IA in rapida evoluzione, con l'obiettivo non solo di sfruttare l'IA per il successo aziendale, ma anche di proteggersi dai rischi derivanti da implementazioni IA frettolose o non sicure. Questi leader e team devono creare tattiche per cogliere le opportunità, affrontare le sfide e mitigare i rischi.

Questa checklist ha lo scopo di aiutare i leader del settore tecnologico e aziendale a comprendere rapidamente i rischi e i vantaggi dell'utilizzo di LLM, consentendo loro di concentrarsi sullo sviluppo di un elenco completo di aree e attività critiche necessarie per difendere e proteggere l'organizzazione durante la definizione di una strategia basata su modelli di linguaggio di grandi dimensioni (Large Language Model).

Il team OWASP Top 10 for LLM Applications si augura che questa lista aiuti le organizzazioni a migliorare le proprie tecniche difensive esistenti e a svilupparne di nuove per affrontare le nuove minacce derivanti dall'utilizzo di questa tecnologia innovativa.

### Perché una checklist?

Le checklist impiegate per sviluppare strategie migliorano la precisione, definiscono gli obiettivi, garantiscono l'uniformità e promuovono un lavoro mirato e deliberato, riducendo dimenticanze e dettagli trascurati. Seguire una checklist non solo aumenta la fiducia in un'adozione sicura, ma incoraggia anche l'innovazione futura dell'azienda, offrendo una strategia semplice ed efficace per il miglioramento continuo.

### Non esaustiva

Sebbene questo documento intenda supportare le organizzazioni nello sviluppo di una strategia LLM iniziale in un ambiente tecnico, legale e normativo in rapida evoluzione, non è esaustivo e non copre tutti i casi d'uso o gli obblighi. Utilizzando questo documento, le organizzazioni dovrebbero estendere le valutazioni e le pratiche oltre l'ambito della checklist fornita, come richiesto dal loro caso d'uso specifico o dalla loro giurisdizione.

### Sfide dei modelli di linguaggio di grandi dimensioni (LLM)

I modelli di linguaggio di grandi dimensioni (LLM) presentano diverse problematiche serie e uniche. Una delle più importanti è che, quando si lavora con gli LLM, il piano di controllo e il piano dati non possono essere completamente isolati o separati. Un'altra sfida significativa è che gli LLM sono non deterministici per progettazione, generando un output diverso a fronte del medesimo prompt o richiesta.
Gli LLM utilizzano la ricerca semantica piuttosto che la ricerca per parole chiave. La differenza fondamentale tra le due sta nel fatto che l'algoritmo del modello dà priorità ai concetti nella sua risposta. Si tratta di un allontanamento significativo dal modo in cui i consumatori hanno utilizzato la tecnologia in precedenza, con un impatto sulla coerenza e l'affidabilità dei risultati. Le "allucinazioni", generate dalle lacune e dagli errori di addestramento nei dati su cui è stato allenato il modello, sono il risultato di questo metodo.

Esistono metodi per migliorare l'affidabilità e ridurre la superficie di attacco per jailbreaking, manipolazione del modello e allucinazioni, ma c'è un compromesso tra restrizioni e utilità, sia in termini di costi che di funzionalità.

L'utilizzo di LLM e le applicazioni basate su LLM aumentano la superficie di attacco di un'organizzazione. Alcuni rischi associati agli LLM sono unici, ma molti sono problemi già noti, come la Bill of Materials (SBoM) del software, la supply chain, la Data Loss Prevention (DLP) e l'accesso autorizzato. Ci sono anche rischi crescenti non direttamente correlati alla GenAI, ma la GenAI aumenta l'efficienza, la capacità e l'efficacia degli aggressori che attaccano e minacciano le organizzazioni.

Gli attori malevoli sfruttano sempre più gli strumenti LLM e di intelligenza artificiale generativa per affinare e accelerare i metodi tradizionali di attacco a organizzazioni, individui e sistemi governativi. Gli LLM facilitano la loro capacità di migliorare le tecniche, consentendo loro di creare facilmente nuovi malware, incorporando potenzialmente vulnerabilità zero-day o progettati per eludere il rilevamento. Possono anche generare schemi di phishing sofisticati, unici o personalizzati. La creazione di deepfake convincenti, video o audio, facilita ulteriormente le loro strategie di social engineering. Inoltre, questi strumenti consentono loro di eseguire intrusioni e sviluppare capacità di hacking innovative. In futuro, un utilizzo più "personalizzato" e combinato della tecnologia IA da parte di criminali richiederà risposte specifiche e soluzioni dedicate per garantire adeguate capacità di difesa e resilienza dell'organizzazione.

Le organizzazioni affrontano anche la minaccia di NON utilizzare le capacità degli LLM, rischiando uno svantaggio competitivo, una percezione di obsolescenza da parte di clienti e partner, l'impossibilità di scalare le comunicazioni personalizzate, la stagnazione dell'innovazione, inefficienze operative, un maggiore rischio di errore umano nei processi e un'allocazione inefficiente delle risorse umane.

Comprendere i diversi tipi di minacce e integrarle con la strategia aziendale aiuterà a valutare sia i pro che i contro dell'utilizzo dei modelli di linguaggio di grandi dimensioni (LLM) rispetto al non utilizzo, assicurandosi che accelerino piuttosto che ostacolino il raggiungimento degli obiettivi aziendali.

### Categorie di minacce verso LLM 

![Fig_1_2](images/GOV1_Fig_1_2.png)

##### Figura 1.2  Tipologie di minacce verso IA
##### crediti: sdunn



### Formazione su Sicurezza e Privacy su Intelligenza Artificiale

La formazione in materia di intelligenza artificiale (IA), intelligenza artificiale generativa (GenAI) e potenziali conseguenze future dello sviluppo, dell'acquisto o dell'utilizzo di modelli di linguaggio di grandi dimensioni (LLM) è utile per tutti i dipendenti di un'organizzazione. La formazione sull'uso consentito e sulla sicurezza informatica dovrebbe essere rivolta a tutti i dipendenti, con un  focus maggiore per alcune figure professionali come risorse umane, legali, sviluppatori, team di dati e team di sicurezza.

L'implementazione dall'inizio di politiche di uso corretto e interazione sana sarà un pilastro fondamentale per il successo delle future campagne di sensibilizzazione sulla sicurezza informatica dell'IA. Ciò fornirà agli utenti la conoscenza delle regole basilari per l'interazione, nonché la capacità di distinguere un comportamento positivo da uno negativo o non etico.

### Integrare la sicurezza e la governance degli LLM
### con pratiche e controlli esistenti e consolidati

Sebbene l'IA e l'intelligenza artificiale generativa aggiungano una nuova dimensione alla sicurezza informatica, alla resilienza, alla privacy e al rispetto dei requisiti legali e normativi, le best practice esistenti da tempo rimangono il modo migliore per identificare problemi, individuare vulnerabilità, risolverle e mitigare potenziali problemi di sicurezza.

● Confermare che la gestione dei sistemi di intelligenza artificiale sia integrata con le pratiche organizzative esistenti.
● Confermare che i sistemi AIML seguano le pratiche esistenti di privacy, governance e sicurezza, e quando necessario, con pratiche di privacy e sicurezza specifiche per sistemi di IA.

### Principi fondamentali di sicurezza

Le capacità degli LLM introducono un tipo diverso di superficio e tipo di attacco. Gli LLM sono vulnerabili a bug complessi della logica di business, come l'iniezione di prompt, la progettazione insicura di plugin e l'esecuzione di codice remoto. Le best practice esistenti sono il modo migliore per risolvere questi problemi. È necessario istituire internamente un team di sicurezza del prodotto che comprenda la revisione sicura del software, l'architettura, la governance dei dati e le valutazioni di terze parti. Il team di cybersecurity dovrebbe inoltre verificare la solidità dei controlli attualmente implementati per individuare problemi che potrebbero essere aggravati dagli LLM, come la clonazione della voce, l'imitazione o il bypass dei captcha.

Sulla base dei recenti progressi nell'apprendimento automatico (Machine Learning), nell'elaborazione del linguaggio naturale (PNL), nella comprensione del linguaggio naturale (NLU), nell'apprendimento profondo e, più recentemente, nei modelli di linguaggio di grandi dimensioni (LLM) e nell'intelligenza artificiale generativa, si raccomanda di integrare professionisti esperti in questi settori accanto ai team di cybersecurity e devops. La loro competenza non solo aiuterà nell'adozione di queste tecnologie, ma anche nello sviluppo di analisi e risposte innovative alle nuove sfide.

### Rischio

Il riferimento al rischio utilizza la definizione ISO 31000: Rischio = "effetto dell'incertezza sugli obiettivi". I rischi associati agli LLM inclusi nella checklist comprendono un elenco mirato di rischi LLM che affrontano rischi avversariali, di sicurezza, legali, normativi, reputazionali, finanziari e competitivi.

### Tassonomia delle Vulnerabilità e della Mitigazione

I sistemi attualmente utilizzati per classificare le vulnerabilità e condividere informazioni sulle minacce, come OVAL, STIX, CVE e CWE, sono ancora in fase di sviluppo per quanto riguarda la capacità di monitorare e allertare i difensori sulle vulnerabilità e le minacce specifiche dei modelli di linguaggio di grandi dimensioni (LLM) e dei modelli predittivi. Ci si aspetta che le organizzazioni si affidino a questi standard consolidati e riconosciuti, come CVE per la classificazione delle vulnerabilità e STIX per lo scambio di informazioni di intelligence sulle minacce informatiche (CTI), quando vengono identificate vulnerabilità o minacce ai sistemi di intelligenza artificiale/apprendimento automatico e alle loro catene di approviggionamento.

## Determinare la Strategia LLM

La rapida espansione delle applicazioni dei modelli di linguaggio di grandi dimensioni (LLM) ha aumentato l'attenzione e l'esame di tutti i sistemi di intelligenza artificiale/apprendimento automatico utilizzati nelle operazioni aziendali, che comprendono sia l'intelligenza artificiale generativa che i sistemi di intelligenza artificiale/apprendimento automatico predittivi consolidati. Questa maggiore attenzione espone potenziali rischi, come gli aggressori che prendono di mira sistemi precedentemente trascurati o sfide di governance o legali che potrebbero essere state ignorate in termini di questioni legali, privacy, responsabilità o garanzia. Per qualsiasi organizzazione che sfrutta i sistemi di intelligenza artificiale/apprendimento automatico nelle sue operazioni, è fondamentale valutare e stabilire politiche complete, governance, protocolli di sicurezza, misure di privacy e standard di responsabilità per garantire che queste tecnologie si allineino ai processi aziendali in modo sicuro ed etico.

Gli attori malevoli o avversari rappresentano la minaccia più immediata e dannosa per le aziende, le persone e gli enti governativi. I loro obiettivi, che vanno dal guadagno finanziario allo spionaggio, li spingono a rubare informazioni critiche, interrompere le operazioni e danneggiare la fiducia. Inoltre, la loro capacità di sfruttare le nuove tecnologie come l'intelligenza artificiale e l'apprendimento automatico aumenta la velocità e la sofisticazione degli attacchi, rendendo difficile per le difese rimanere al passo.

La minaccia LLM non avversaria più urgente per molte organizzazioni deriva dall'"IA Shadow": dipendenti che utilizzano strumenti di intelligenza artificiale online non approvati, plug-in per browser non sicuri e applicazioni di terze parti che introducono funzionalità LLM tramite aggiornamenti o upgrade, aggirando i processi standard di approvazione del software.

![Fig_2_1](images/GOV1_Fig_2_1.png)

##### Figura 2.1  Opzioni per una strategia di distribuzione 
##### crediti: sdunn


### Strategia di distribuzione

Gli ambiti spaziano dall'utilizzo di applicazioni pubbliche per i consumatori all'addestramento di modelli proprietari su dati privati. Fattori come la sensibilità del caso d'uso, le capacità necessarie e le risorse disponibili aiutano a determinare il giusto equilibrio tra comodità e controllo. Tuttavia, la comprensione di questi cinque tipi di modello fornisce un quadro per valutare le opzioni.

![Fig_2_2](images/GOV1_Fig_2_2.png)

##### Figura 2.2 Opzioni per tipologie di distribuzione
##### crediti: sdunn
## Checklist

### Adversarial Risk

Il rischio avversario comprende la concorrenza e attori malevoli.

Analizza come i competitor stanno investendo nell'intelligenza artificiale. Sebbene l'adozione dell'IA comporti dei rischi, ci sono anche vantaggi commerciali che possono influire sul posizionamento futuro nel mercato.
Indaga sull'impatto dei controlli di sicurezza attuali, come il reset della password tramite riconoscimento vocale, che potrebbero non offrire più una difesa adeguata contro i nuovi attacchi potenziati dalla Generative AI (GenAI).
Aggiorna il piano di risposta agli incidenti e le procedure operative standard per gestire attacchi avanzati con GenAI e specifici incidenti legati all' intelligenza artificiale machine learning (AIML).

### Threat Modeling

Si raccomanda vivamente di effettuare il threat modeling per identificare le minacce e analizzare i processi e le difese di sicurezza. Il threat modeling è un insieme di processi sistematici e ripetibili che consentono di prendere decisioni di sicurezza ragionevoli per applicazioni, software e sistemi. Eseguire il threat modeling prima di implementare modelli di linguaggio grande (LLM) e per gli attacchi accelerati da GenAI rappresenta il modo più conveniente per identificare e mitigare i rischi, proteggere i dati, tutelare la privacy e garantire un'integrazione sicura e conforme all'interno dell'azienda.

In che modo gli aggressori sfrutteranno la Generative AI per lanciare attacchi sempre più mirati contro l'organizzazione, i dipendenti, i dirigenti o gli utenti? Le aziende dovrebbero prepararsi ad attacchi "iper-personalizzati" su larga scala con l'ausilio della GenAI. Gli attacchi di spear phishing basati su LLM sono ora esponenzialmente più efficaci, mirati e strumentalizzati per gli attacchi.
Come potrebbe essere utilizzata la GenAI per attaccare i clienti o i partner commerciali dell'azienda attraverso lo spoofing o contenuti generati dalla GenAI?
L'azienda è in grado di rilevare e neutralizzare input o query dannosi o malevoli indirizzati alle soluzioni LLM?
L'azienda può salvaguardare le connessioni con i sistemi e i database esistenti con integrazioni sicure in tutti i trust boundaries degli LLM?
L'azienda dispone di misure per mitigare le minacce interne e prevenire l'abuso da parte di utenti autorizzati?
L'azienda può impedire l'accesso non autorizzato a modelli o dati proprietari per proteggere la proprietà intellettuale?
L'azienda può prevenire la generazione di contenuti dannosi o inappropriati utilizzando un filtro automatico dei contenuti?

### AI Asset Inventory

An AI asset inventory should apply to both internally developed and external or third-party solutions.

Catalog existing AI services, tools, and owners. Designate a tag in asset management for specific inventory.
Include AI components in the Software Bill of Material (SBOM), a comprehensive list of all the software components, dependencies, and metadata associated with applications.
Catalog AI data sources and the sensitivity of the data (protected, confidential, public)
Establish if pen testing or red teaming of deployed AI solutions is required to determine the current attack surface risk.
Create an AI solution onboarding process.
Ensure skilled IT admin staff is available either internally or externally, following SBoM requirements.

### AI Security and Privacy Training

Actively engage with employees to understand and address concerns with planned LLM initiatives.
 Establish a culture of open, and transparent communication on the organization's use of predictive or generative AI within the organization process, systems, employee management and support, and customer engagements and how its use is governed, managed, and risks addressed. 
Train all users on ethics, responsibility, and legal issues such as warranty, license, and copyright.
Update security awareness training to include GenAI related threats. Voice cloning and image cloning, as well as in anticipation of increased spear phishing attacks
Any adopted GenAI solutions should include training for both DevOps and cybersecurity for the deployment pipeline to ensure AI safety and security assurances.

### Establish Business Cases

Solid business cases are essential to determining the business value of any proposed AI solution, balancing risk and benefits, and evaluating and testing return on investment. There are an enormous number of potential use cases; a few examples are provided.

Enhance customer experience
Better operational efficiency
Better knowledge management
Enhanced innovation
Market Research and Competitor Analysis
Document creation, translation, summarization, and analysis 

### Governance

Corporate governance in LLM is needed to provide organizations with transparency and accountability. Identifying AI platform or process owners who are potentially familiar with the technology or the selected use cases for the business is not only advised but also necessary to ensure adequate reaction speed that prevents collateral damages to well established enterprise digital processes.

Establish the organization’s AI RACI chart (who is responsible, who is accountable, who should be consulted, and who should be informed)
Document and assign AI risk, risk assessments, and governance responsibility within the organization.
Establish data management policies, including technical enforcement, regarding data classification and usage limitations. Models should only leverage data classified for the minimum access level of any user of the system. For example, update the data protection policy to emphasize not to input protected or confidential data into nonbusiness-managed tools.
Create an AI Policy supported by established policy (e.g., standard of good conduct, data protection, software use)
Publish an acceptable use matrix for various generative AI tools for employees to use.
Document the sources and management of any data that the organization uses from the generative LLM models. 

### Legal

Many of the legal implications of AI are undefined and potentially very costly. An IT, security, and legal partnership is critical to identifying gaps and addressing obscure decisions.

Confirm product warranties are clear in the product development stream to assign who is responsible for product warranties with AI.
Review and update existing terms and conditions for any GenAI considerations.
Review AI EULA agreements. End-user license agreements for GenAI platforms are very different in how they handle user prompts, output rights and ownership, data privacy, compliance, liability, privacy, and limits on how output can be used.
Organizations EULA for customers, Modify end-user agreements to prevent the organization from incurring liabilities related to plagiarism, bias propagation, or intellectual property infringement through AI-generated content.
Review existing AI-assisted tools used for code development. A chatbot's ability to write code can threaten a company's ownership rights to its product if a chatbot is used to generate code for the product. For example, it could call into question the status and protection of the generated content and who holds the right to use the generated content.
Review any risks to intellectual property. Intellectual property generated by a chatbot could be in jeopardy if improperly obtained data was used during the generative process, which is subject to copyright, trademark, or patent protection. If AI products use infringing material, it creates a risk for the outputs of the AI, which may result in intellectual property infringement.
Review any contracts with indemnification provisions. Indemnification clauses try to put the responsibility for an event that leads to liability on the person who was more at fault for it or who had the best chance of stopping it. Establish guardrails to determine whether the provider of the AI or its user caused the event, giving rise to liability.
Review liability for potential injury and property damage caused by AI systems.
Review insurance coverage. Traditional (D&O) liability and commercial general liability insurance policies are likely insufficient to fully protect AI use.
Identify any copyright issues. Human authorship is required for copyright. An organization may also be liable for plagiarism, propagation of bias, or intellectual property infringement if LLM tools are misused.
Ensure agreements are in place for contractors and appropriate use of AI for any development or provided services.
Restrict or prohibit the use of generative AI tools for employees or contractors where enforceable rights may be an issue or where there are IP infringement concerns.
Assess and AI solutions used for employee management or hiring could result in disparate treatment claims or disparate impact claims.
Make sure the AI solutions do not collect or share sensitive information without proper consent or authorization.

### Regulatory

The EU AI Act is anticipated to be the first comprehensive AI law but will apply in 2025 at the earliest. The EU's General Data Protection Regulation (GDPR) does not specifically address AI but includes rules for data collection, data security, fairness and transparency, accuracy and reliability, and accountability, which can impact GenAI use. In the United States, AI regulation is included within broader consumer privacy laws. Ten US states have passed laws or have laws that will go into effect by the end of 2023.

Canada has so far only published a Voluntary Code of Conduct on the Responsible Development and Management of Advanced Generative AI Systems, however, the Artificial Intelligence and Data Act (AIDA) will have stronger requirements.

Federal organizations such as the US Equal Employment Opportunity Commission (EEOC), the Consumer Financial Protection Bureau (CFPB), the Federal Trade Commission (FTC), and the US Department of Justice's Civil Rights Division (DOJ) are closely monitoring hiring fairness.

Determine Country, State, or other Government specific AI compliance requirements.
Determine compliance requirements for restricting electronic monitoring of employees and employment-related automated decision systems (Vermont, California, Maryland, New York, New Jersey)
Determine compliance requirements for consent for facial recognition and the AI video analysis required (Illinois, Maryland, Washington, Vermont)
Review any AI tools in use or being considered for employee hiring or management.
Confirm the vendor’s compliance with applicable AI laws and best practices.
Ask and document any products using AI during the hiring process. Ask how the model was trained, and how it is monitored, and track any corrections made to avoid discrimination and bias.
Ask and document what accommodation options are included.
Ask and document whether the vendor collects confidential data.
Ask how the vendor or tool stores and deletes data and regulates the use of facial recognition and video analysis tools during pre-employment.
Review other organization-specific regulatory requirements with AI that may raise compliance issues. The Employee Retirement Income Security Act of 1974, for instance, has fiduciary duty requirements for retirement plans that a chatbot might not be able to meet. 

### Using or Implementing Large Language Model Solutions

Threat Model LLM components and architecture trust boundaries.
Data Security, verify how data is classified and protected based on sensitivity, including personal and proprietary business data. (How are user permissions managed, and what safeguards are in place?)
Access Control, implement least privilege access controls and implement defense-in-depth measures
Training Pipeline Security, require rigorous control around training data governance, pipelines, models, and algorithms.
Input and Output Security, evaluate input validation methods, as well as how outputs are filtered, sanitized, and approved.
Monitoring and Response, map workflows, monitoring, and responses to understand automation, logging, and auditing. Confirm audit records are secure.
Include application testing, source code review, vulnerability assessments, and red teaming in the production release process.
Check for existing vulnerabilities in the LLM model or supply chain.
Look into the effects of threats and attacks on LLM solutions, such as prompt injection, the release of sensitive information, and process manipulation.
Investigate the impact of attacks and threats to LLM models, including model poisoning, improper data handling, supply chain attacks, and model theft.
Supply Chain Security, request third-party audits, penetration testing, and code reviews for third-party providers. (both initially and on an ongoing basis)
Infrastructure Security, ask how often a vendor performs resilience testing? What are their SLAs in terms of availability, scalability, and performance?
Update incident response playbooks and include an LLM incident in tabletop exercises. 
Identify or expand metrics to benchmark generative cybersecurity AI against other approaches to measure expected productivity improvements.

### Testing, Evaluation, Verification, and Validation (TEVV)

NIST AI Framework recommends a continuous TEVV process throughout the AI lifecycle which includes the AI system operators, domain experts, AI designers, users, product developers, evaluators, and auditors. TEVV includes a range of tasks such as system validation, integration, testing, recalibration, and ongoing monitoring for periodic updates to navigate the risks and changes of the AI system.

Establish continuous testing, evaluation, verification, and validation throughout the AI model lifecycle.
Provide regular executive metrics and updates on AI Model functionality, security, reliability, and robustness.

### Model Cards and Risk Cards

Model cards and risk cards are foundational elements for increasing the transparency, accountability, and ethical deployment of Large Language Models (LLMs). Model cards help users understand and trust AI systems by providing standardized documentation on their design, capabilities, and constraints, leading them to make educated and safe applications. Risk cards supplement this by openly addressing potential negative consequences, such as biases, privacy problems, and security vulnerabilities, which encourages a proactive approach to harm prevention. These documents are critical for developers, users, regulators, and ethicists equally since they establish a collaborative atmosphere in which AI's social implications are carefully addressed and handled. These cards, developed and maintained by the organizations that created the models, play an important role in ensuring that AI technologies fulfill ethical standards and legal requirements, allowing for responsible research and deployment in the AI ecosystem.

Model cards include key attributes associated with the ML model:

Model details: Basic information about the model, i.e., name, version, and type (neural network, decision tree, etc.), and the intended use case.
Model architecture: Includes a description of the structure of the model, such as the number and type of layers, activation functions, and other key architectural choices.
Training data and methodology: Information about the data used to train the model, such as the size of the dataset, the data sources, and any preprocessing or data augmentation techniques used. It also includes details about the training methodology, such as the optimizer used, the loss function, and any hyperparameters that were tuned.
Performance metrics: Information about the model's performance on various metrics, such as accuracy, precision, recall, and F1 score. It may also include information about how the model performs on different subsets of the data.
Potential biases and limitations: Lists potential biases or limitations of the model, such as imbalanced training data, overfitting, or biases in the model's predictions. It may also include information about the model's limitations, such as its ability to generalize to new data or its suitability for certain use cases.
Responsible AI considerations: Any ethical or responsible AI considerations related to the model, such as privacy concerns, fairness, and transparency, or potential societal impacts of the model's use. It may also include recommendations for further testing, validation, or monitoring of the model.

The precise features contained in a model card may differ based on the model's context and intended usage, but the purpose is to give openness and accountability in the creation and deployment of machine learning models.

Review a models model card 
Review risk card if available
Establish a process to track and maintain model cards for any deployed model including models used through a third party.

### RAG: Large Language Model Optimization

Fine tuning, the traditional method for optimizing a pre-trained model, involved retraining an existing model on new, and domain-specific data, modifying it for performance on a task or application. Fine-tuning is expensive but essential to improve performance. 

Retrieval-Augmented Generation (RAG) has evolved as a more effective way of optimizing and augmenting the capabilities of large language models by retrieving pertinent data from up to date available knowledge sources. RAG can be customized for specific domains, optimizing the retrieval of domain-specific information and tailoring the generation process to the nuances of specialized fields. RAG is seen as a more efficient and transparent method for LLM optimization, particularly for problems where labeled data is limited or expensive to collect. One of the primary advantages of RAG is its support for continuous learning since new information can be continually updated at the retrieval stage.

The RAG implementation involves several key steps starting from embedding model deployment, indexing the knowledge library, to retrieving the most relevant documents for query processing. Efficient retrieval of the relevant context is made based on vector databases which are used for storage and querying of document embeddings.

#### RAG Reference
Retrieval Augmented Generation (RAG) & LLM: Examples
12 RAG Pain Points and Proposed Solutions

### AI Red Teaming

AI Red Teaming is an adversarial attack test simulation of the AI System to validate there aren’t any existing vulnerabilities which can be exploited by an attacker. It is a recommended practice by many regulatory and AI governing bodies including the Biden administration. Red-teaming alone is not a comprehensive solution to validate all real-world harms associated with AI systems and should be included with other forms of testing, evaluation, verification, and validation such as algorithmic impact assessments and external audits.

Incorporate Red Team testing as a standard practice for AI Models and applications.
## Resources

OWASP Top 10 for Large Language Models

![OWASP Top10 for LLM](images/GOV1_Fig_4_1.jpg)
##### Figure 4.1  OWASP Top 10 for Large Language Model Applications

![OWASP Top10 for LLM Visual](images/GOV1_Fig_4_2_en.png)
##### Figure 4.2  OWASP Top 10 for Large Language Model Applications Visualized


### OWASP Resources

Using LLM solutions expands an organization's attack surface and presents new challenges, requiring special tactics and defenses. It also poses problems that are similar to known issues, and where there are already established cybersecurity procedures and mitigations. Integrating LLM cybersecurity with an organization's established cybersecurity controls, processes, and procedures allows an organization to reduce its vulnerability to threats.
How they integrate is available at the OWASP Integration Standards.

#### OWASP Resource
OWASP SAMM
#### Description
Software Assurance Maturity Model
#### Why it is Recommended & Where To Use It
Provides an effective and measurable way to analyze and improve an organization's secure development lifecycle. SAMM supports the complete software lifecycle. It is iterative and risk-driven, enabling organizations to identify and prioritize gaps in secure software development so resources for improving the process can be dedicated where efforts have the greatest improvement impact.

#### OWASP Resource
OWASP AI Exchange
OWASP Machine Learning Security Top 10
#### Description
OWASP Project to connect worldwide for an exchange on AI security, fostering standards alignment, and driving collaboration.
OWASP AI Exchange is the intake method for the OWASP AI Security and Privacy Guide
OWASP Machine Learning Security Top 10 security issues of machine learning systems
#### Why it is Recommended & Where To Use It
This project includes the ML Top 10 and is a live working document that provides clear and actionable insights on designing, creating, testing, and procuring secure and privacy-preserving AI systems. It is the best OWASP resource for AI global regulatory and privacy information.

#### OWASP Resource
Open Common Requirement Enumeration : OpenCRE
#### Description
OpenCRE is the interactive content-linking platform for uniting security standards and guidelines into one overview.
#### Why it is Recommended & Where To Use It
Use this site to search for standards. You can search by standard name or by control type.

#### OWASP Resource
OWASP Threat Modeling
#### Description
A structured, formal process for threat modeling of an application
#### Why it is Recommended & Where To Use It
Learn everything about Threat Modeling which is a structured representation of all the information that affects the security of an application.

#### OWASP Resource
OWASP CycloneDX
#### Description
OWASP CycloneDX is a full-stack Bill of Materials (BOM) standard that provides advanced supply chain capabilities for cyber risk reduction.
#### Why it is Recommended & Where To Use It
Modern software is assembled using third-party and open source components. They are glued together in complex and unique ways and integrated with original code to achieve the desired functionality. An SBOM provides an accurate inventory of all components which enables organizations to identify risk, allows for greater transparency, and enables rapid impact analysis.
EO 14028 provided minimum requirements for SBOM for federal systems.

#### OWASP Resource
OWASP Software Component Verification Standard (SCVS)
#### Description
A community-driven effort to establish a framework for identifying activities, controls, and best practices to identify and reduce risk in a software supply chain.
#### Why it is Recommended & Where To Use It
Use SCVS to develop a common set of activities, controls, and best practices that can reduce risk in a software supply chain and identify a baseline and path to mature software supply chain vigilance.

#### OWASP Resource
OWASP API Security Project
#### Description
API Security focuses on strategies and solutions to understand and mitigate the unique vulnerabilities and security risks of Application Programming Interfaces (APIs).
#### Why it is Recommended & Where To Use It
APIs are a foundational element of connecting applications and mitigating misconfigurations or vulnerabilities is mandatory to protect users and organizations. Use for security testing and red teaming the build and production environments.

#### OWASP Resource
OWASP Top 10 CI/CD Security Risks
#### Description
Helps defenders identify focus areas for securing their CI/CD ecosystem.
#### Why it is Recommended & Where To Use It
CI/CD environments, processes, and systems are the ecosystem of modern software organizations. They deliver code from an engineer's workstation to production. They have their unique attack surface and a frequent attack target. Use for security testing and red teaming the build and production environments. 

#### OWASP Resource
OWASP Application Security Verification Standard ASVS
#### Description
Application Security Verification Standard (ASVS) Project provides a basis for testing web application technical security controls and also provides developers with a list of requirements for secure development.
#### Why it is Recommended & Where To Use It
Cookbook for web application security requirements, security testing, and metrics. Use to establish security user stories and security use case release testing.

#### OWASP Resource
OWASP Threat and Safeguard Matrix (TaSM)
#### Description
An action oriented view to safeguard and enable the business
#### Why it is Recommended & Where To Use It
This matrix allows a company to overlay its major threats with the NIST Cyber Security Framework Functions (Identify, Protect, Detect, Respond, & Recover) to build a robust security plan. Use it as a dashboard to track and report on security across the organization.

#### OWASP Resource
Defect Dojo
#### Description
An open-source vulnerability management tool that streamlines the testing process by offering templating, report generation, metrics, and baseline self-service tools.
#### Why it is Recommended & Where To Use It
Use Defect Dojo to reduce the time for logging vulnerabilities with templates for vulnerabilities, imports for common vulnerability scanners, report generation, and metrics.


### MITRE Resources

The increased frequency of LLM threats emphasizes the value of a resilience-first approach to defending an organization's attack surface. Existing TTPS is combined with new attack surfaces and capabilities in LLM Adversary threats and mitigations. MITRE maintains a well-established and widely accepted mechanism for coordinating opponent tactics and procedures based on real-world observations.

Coordination and mapping of an organization's LLM Security Strategy to MITRE ATT&CK and MITRE ATLAS allows an organization to determine where LLM Security is covered by current processes such as API Security Standards or where security holes exist.

MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) is a framework, collection of data matrices, and assessment tool that was made by the MITRE Corporation to help organizations figure out how well their cybersecurity works across their entire digital attack surface and find holes that had not been found before. It is a knowledge repository that is used all over the world. The MITRE ATT&CK matrix contains a collection of strategies used by adversaries to achieve a certain goal. In the ATT&CK Matrix, these objectives are classified as tactics. The objectives are outlined in attack order, beginning with reconnaissance and progressing to the eventual goal of exfiltration or impact.

MITRE ATLAS, which stands for "Adversarial Threat Landscape for Artificial Intelligence Systems," is a knowledge base that is based on real-life examples of attacks on machine learning (ML) systems by bad actors. ATLAS is based on the MITRE ATT&CK architecture, and its tactics and procedures complement those found in ATT&CK.

#### MITRE Resource
MITRE ATT&CK
#### Description
Knowledge base of adversary tactics and techniques based on real-world observations
#### Why it is Recommended & Where To Use It
The ATT&CK knowledge base is used as a foundation for the development of specific threat models and methodologies. Map existing controls within the organization to adversary tactics and techniques to identify gaps or areas to test.

#### MITRE Resource
MITRE AT&CK Workbench
#### Description
Create or extend ATT&CK data in a local knowledge base
#### Why it is Recommended & Where To Use It
Host and manage a customized copy of the ATT&CK knowledge base. This local copy of the ATT&CK knowledge base can be extended with new or updated techniques, tactics, mitigation groups, and software that is specific to your organization.

#### MITRE Resource
MITRE ATLAS
#### Description
MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) is a knowledge base of adversary tactics, techniques, and case studies for machine learning (ML) systems based on real-world observations, demonstrations from ML red teams and security groups, and the state of the possible from academic research
#### Why it is Recommended & Where To Use It
Use it to map known ML vulnerabilities and map checks and controls for proposed projects or existing systems.

#### MITRE Resource
MITRE ATT&CK Powered Suit
#### Description
ATT&CK Powered Suit is a browser extension that puts the MITRE ATT&CK knowledge base at your fingertips.
#### Why it is Recommended & Where To Use It
Add to your browser to quickly search for tactics, techniques, and more without disrupting your workflow.

#### MITRE Resource
The Threat Report ATT&CK Mapper (TRAM)
#### Description
Automates TTP Identification in CTI Reports
#### Why it is Recommended & Where To Use It
Mapping TTPs found in CTI reports to MITRE ATT&CK is difficult, error prone, and time-consuming. TRAM uses LLMs to automate this process for the 50 most common techniques. Supports Juypter notebooks.

#### MITRE Resource
Attack Flow v2.1.0
#### Description
Attack Flow is a language for describing how cyber adversaries combine and sequence various offensive techniques to achieve their goals.
#### Why it is Recommended & Where To Use It
Attack Flow helps visualize how an attacker uses a technique, so defenders and leaders understand how adversaries operate and improve their defensive posture.

#### MITRE Resource
MITRE Caldera
#### Description
A cyber security platform (framework) designed to easily automate adversary emulation, assist manual red teams, and automate incident response.
#### Why it is Recommended & Where To Use It
Plugins are available for Caldera that help to expand the core capabilities of the framework and provide additional functionality, including agents, reporting, collections of TTPs, and others.
Here is the plugin library.

#### MITRE Resource
CALDERA plugin: Arsenal
#### Description
A plugin developed for adversary emulation of AI-enabled systems.
#### Why it is Recommended & Where To Use It
This plugin provides TTPs defined in MITRE ATLAS to interface with CALDERA.

#### MITRE Resource
Atomic Red Team
#### Description
Library of tests mapped to the MITRE ATT&CK framework.
#### Why it is Recommended & Where To Use It
Use to validate and test controls in an environment. Security teams can use Atomic Red Team to test controls.
You can execute atomic tests directly from the command line; no installation is required.

#### MITRE Resource
MITRE CTI Blueprints
#### Description
Automates Cyber Threat Intelligence reporting.
#### Why it is Recommended & Where To Use It
CTI Blueprints helps Cyber Threat Intelligence (CTI) analysts create high-quality, actionable reports more consistently and efficiently



### AI Vulnerability Repositories

AI Incident Database
A repository of articles about different times AI has failed in real-world applications and is maintained by a college research group and crowds sourced.
OECD AI Incidents Monitor (AIM)
Offers an accessible starting point for comprehending the landscape of AI-related challenges.


### Leading Companies Tracking AI Model Vulnerabilities

Huntr Bug Bounty : ProtectAI
Bug bounty platform for AI/ML
AI Vulnerability Database (AVID) : Garak
Database of model vulnerabilities
AI Risk Database: Robust Intelligence
Database of model vulnerabilities
LVE Repository
Open LLM Vulnerability and Exposures Repository


### AI Procurement Guidance

World Economic Forum: Adopting AI Responsibly: Guidelines for Procurement of AI Solutions by the Private Sector: Insight Report June 2023
The standard benchmarks and assessment criteria for procuring Artificial systems are in early development. This procurement guidelines provide organizations with a baseline of considerations for the end-to-end procurement process.

Use this guidance to augment an organization's existing Third Party Risk Supplier and Vendor procurement process. 

## Team

Thank you to the OWASP Top 10 for LLM Applications Cybersecurity and Governance Checklist Contributors.

### Checklist Contributors

Sandy Dunn
Heather Linn
John Sotiropoulos
Steve Wilson
Fabrizio Cilli
Aubrey King
Bob Simonoff
David Rowe
Ken Huang
Guilherme Junior
Andrea Succi
Jason Ross
Talesh Seeparsan
Anthony Glynn
Julie Tao
Cédric Lallier
Tetsuo Seto
Ads Dawson

## Riguardo alla traduzione

- **Riccardo Sirigu**  
[https://www.linkedin.com/in/riccardosirigu/](https://www.linkedin.com/in/riccardosirigu/) 
