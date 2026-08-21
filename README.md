# Progetto del corso - Introduzione alla Data Science e al Pensiero Computazionale - a.a. 2025/2026
Progetto di fine corso in Introduzione alla Data Science e al Pensiero Computazionale di GEPID.

## Membri gruppo
Il progetto è stato realizzato dal **Gruppo n° 16**:
* **Filippo Vignoli**: matricola 0001217390, email filippo.vignoli@studio.unibo.it
* **Fabio Sola**: matricola 0001231148, email fabio.sola2@studio.unibo.it

## Analisi del churn dei clienti di una società telco

### Descrizione progetto
Il progetto presente in questa repository consiste nell'analisi dati documentata e riproducibile, comprensiva di report scientifico e repository strutturato, incentrata sull'abbandono dei clienti di una compagnia di telecomunicazioni.

### Obiettivo
L'obiettivo di questo progetto è analizzare i fattori che determinano l'abbandono dei clienti (il cosiddetto "customer churn") e sviluppare modelli di Machine Learning. Tali modelli sono stati ideati per predire preventivamente quali utenti sono a rischio di cancellazione del servizio. In conformità con i goal proposti dal corso, si tratta di un problema di previsione dell'abbandono del servizio.

## Descrizione dataset
Il file utilizzato per l'addestramento e l'analisi è *Customer_Churn.csv*. 
* Il dataset raccoglie i dati dei clienti di un'azienda di telecomunicazioni per analizzare il fenomeno del churn.
* È composto da 7043 righe e 21 colonne.
* Include 3 variabili numeriche e 18 variabili categoriche.
* I dati sono suddivisi in informazioni demografiche (es. genere, presenza di familiari a carico, anzianità), servizi attivati (es. connettività, servizi di sicurezza e supporto, intrattenimento) e dettagli contrattuali e finanziari (es. tipo di contratto, mesi di permanenza, metodo di pagamento, costi).
* La variabile target, denominata "Churn", indica se il cliente ha abbandonato la compagnia (Yes) o è ancora attivo (No).

## Modelli usati
Per la fase di classificazione e modellazione, per mettere a confronto algoritmi lineari e non lineari, sono stati addestrati i seguenti tre modelli di Machine Learning:
* **Regressione Logistica**: modello lineare.
* **Random Forest** (RandomForestClassifier): modello ensemble non lineare.
* **k-Nearest Neighbors** (k-NN): modello non parametrico basato su distanze.
Al fine di ottimizzare la metrica di "Recall" per la rilevazione dei clienti a rischio, i modelli sono stati inseriti in una Pipeline che comprende la tecnica SMOTE per il bilanciamento delle classi e la ricerca degli iperparametri migliori tramite GridSearchCV. Inoltre, la soglia decisionale sulle probabilità è stata abbassata al 35%. Il Random Forest si è rivelato il modello migliore per l'equilibrio di business.

## Istruzioni per l'esecuzione
Per riprodurre il progetto e rieseguire le analisi, seguire i seguenti passaggi:
1. Clonare o scaricare il presente repository GitHub nel proprio ambiente di lavoro (es. Google Colab).
2. Assicurarsi di avere nella directory di lavoro il dataset `Customer_Churn.csv` che viene letto tramite `pd.read_csv("Customer_Churn.csv")`.
3. Assicurarsi di avere installato le librerie Python necessarie richieste nel notebook: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn` e `imblearn`.
4. Eseguire le celle del notebook partendo dalla "Preparazione dell'ambiente" fino alla Parte 4 ("Valutazione e interpretazione dei risultati").

***
Buona lettura e buon lavoro!
