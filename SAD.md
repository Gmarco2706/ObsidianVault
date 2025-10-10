#R
**PROGRAMMAZIONE FUNZIONALE**
	La programmazione funzionale è un paradigma di programmazione basato sull'uso delle funzioni come entità di prima classe, ovvero le funzioni possono essere trattate come dati e quindi passate come argomenti, restituite da altre funzioni e memorizzate in variabili, la programmazione funzionale ha queste caratteristiche:
	 - Immutabilità: le variabili non vengono modificate ma se ne creano di nuove
	 - Funzioni Pure: che non hanno effetti collaterali ma dipendono solo dall'otuput 
	 - Composizione di Funzioni: Funzioni combinate insieme per formare operazioni più complesse
	 
**FUNZIONI IN R**
	R dispone di un linguaggio di interazione multi-paradigma comprendendo caratteristiche funzionali, OOP e di programmazione funzionale. 
	Le funzioni di R sono **anonime** e alcune di esse permettono di applicare altre funzioni su intere strutture dati.
	Per definire una funzione in R si usa il comando **function**:
	   `function(lista parametri)`
	 se vogliamo assegnare una funzione ad un oggetto "funz" scriveremo: 
	   `funz <- function()`
	 **FUNZIONI APPLY**
		  La famiglia di funzioni apply è progettata per facilitare l'applicazione di operazioni su insiemi di dati come matrici, array, liste e data frame:
		  - riducono l'uso esplicito dei for
		  - migliorano la leggibilità e la compattezza del codice
		![[Pasted image 20251005113716.png]]
		 **APPLY**
			 la funzione apply è definita come `apply(X,MARGIN,FUN, ...)` in cui:
			 - X è una matrice di array 
			 - MARGIN specifica se applicare la funzione per righe (MARGIN = 1) o per colonne (MARGIN = 2) 
			 - FUN è la funzione da applicare
			 apply viene utilizzata per applicare una funzione a una matrice o a un array multidimensionale
		 **SUPPLY**
			 è una funzione semplificata di apply che restituisce un vettore o una matrice se possibile, è utilizzata principalmente per applicare una funzione a ciascun elemento di una lista o di un vettore
		 **LAPPLY**
			  è usata per applicare una funzione a ciascun elemento di una lista o di un vettore, è utili per iterare su liste di qualsiasi tipo, non limitandosi a liste numeriche, ma anche su liste che contengono vettori, matrici o altri oggetti, l'output è sempre una lista
**VETTORI**
	In R i vettori sono oggetti che mantengono al loro interno un insieme indicizzato di elementi dello  **dello stesso tipo**. 
		**OPERAZIONI CON I VETTORI**
				**INSERIRE ELEMENTI**
					i valori possono essere inseriti in un vettore in deversi modi:
					- operatore di sequenza
					- operatore di concatenazione
					- funzione `seq()`
					- funzione `rep()`
					- funzione `scan()`
				**ORDINAMENTO**
					l'ordinamento viene fatto tramite la funzione `sort()`
				**RICERCA**
					è possibile ricercare elementi di un vettore che soddisfano una determinata condizione tramite `wich()` la quale richiede come argomento un vettore di tipo logico
					 **SLICING**
					 Se si desidera accedere all'i-esimo elemento del vettore x occorre utilizzare `x[i]` mentre con `x[-i]` si crea un nuovo vettore contenente tutti gli elementi di x escluso l'elemento i-esimo.
					 Se si utilizza `x[i:j]` si visualizzano gli elementi del vettore x dalla posizione i alla j, mentre con `x[-i:j]` si crea un nuovo vettore contenente tutti gli elementi di x esclusi gli elementi dalla posizione i alla posizione j
**ARRAY E MATRICI**
	**LISTE**
		Una lista è una struttura dati in R che può contenere **elementi eterogenei** a differenza degli array. Nella pratica array e vettori possono risultare molti simili, molto spesso gli array vengono indicati come **vector structure** semplicemente un array apre alla possibilità di specificare un ulteriore parametro che ne definisce la dimensione.
		 In particolare in un array tridimensionale "a"  `a[i,j,k]` è l'elemento nella posizione (i,j,k) dell'array, un array tridimensionale di dimensione n × m × r è visto come una sovrapposizione di r array bidimensionali di dimensione n×m
<<<<<<< HEAD
	**MATRICI**
		 **cbind() e bind()**
			 permettono di creare opportune matrici componendo vettori di uguale lunghezza e matrici delle stesse dimensioni, `cbind()`  usa i vettori per creare le colonne mentre `rbind()` per creare le colonne
		 **daig()**
		 La funzione `diag()` cambia funzionalità in base al parametro di input:
		 - `diag(v)` con "v" vettore è usata per creare una matrice diagonale con gli elementi del vettore sulla diagonale e i restanti elementi nulli
		 - `diag(a)` con "a" matrice fornisce un vettore costituito dagli elementi della diagonale principale della matrice
		 - `diag(n)` con "n" intero fornisce la matrice di identità n × n
		**rowsname e colnames**
			`rownames(a)` restituisce o imposta i nomi delle righe di una matrice o di un dataframe
			 `colnames(a)` restituisce o imposta i nomi delle colonne di una matrice o di un dataframe
		**OPERAZIONI TRA MATRICI**
			 
=======
	 **ARRAY**
		 La sostanziale differenza tra array e vettori è il fatto che gli array possono avere più dimensioni, un array viene creato tramite `array()` specificando le dimensioni.
		 Gli array sono utili quando è necessario fornire differenti informazioni per identificare un elemento, una matrice non è che un array bidimensionale di elementi univocamente determinati da una coppia di numeri interi ovvero gli indici di riga e colonna.
		 **MATRICI**
			 se si vuole costruire una matrice n × m con tutti gli elementi nulli si può utilizzare il comando `matrix()` se si vuole accedere all'elemento (i,j) si usa `a[i,j]` mentre con `a[,j]` si selezionano gli elementi della j-esima colonna e viceversa con gli elementi della i-esima riga.
			 Per riempire una matrice si usano le funzioni `cbind()` e `rbind()` che permettono di creare opportune matrici componendo vettori di uguale lunghezza e matrici delle stesse dimensioni, la prima funzione crea le colonne con i vettori e la seconda funzione crea le righe con i vettori.
			 La funzione `diag()` cambia l'output a seconda del suo input:
			 - `diag(v)` con v vettore è usata per creare una matrice diagonale con gli elementi del vettore sulla diagonale e i restanti elementi nulli
			 - `diag(a)` con a matrice fornisce un vettore costruito dagli elementi della diagonale principale della matrice
			 - `diag(n)` con n intero fornisce la matrice di identità n×m
			 Le funzioni `rownames(a)` `colnames(a)` restituiscono o impostano i nomi delle righe e delle colonne di una matrice o di un dataframe 
			 **OPERAZIONI**
				 R interpreta i suoi vettori come vettori colonna, per effettuare una trasposizione di un vettore o di una matrice si usa la funzione `t()` di trasposizione, sui vettori e sulle matrici delle stesse dimensioni si applicano le usuali operazioni aritmetiche come somma prodotto differenza ecc.
				 **PRODOTTO MATRICIALE**
					 R fornisce la possibilità di effettuare il prodotto matriciale tra due matrici a di dimensioni n × m e b di dimensione m × r utilizzando l'operatore  `%*%`
				 DETERMINANTE
						E' un valore scalare associato a una matrice quadrata che fornisce informazioni sulla matrice come l'invertibilità che è tale solo se il determinante è zero, il determinante viene calcolato tramite la funzione `det(a)`  
				 **INVERSA**
					 è una matrice che moltiplicata per la matrice originale fornisce la matrice di identità, è possibile calcolare in R l'inversa di una matrice quadrata `solve(a)`
					 
**AUTOVETTORI E AUTOVALORI**
	R consente di determinare gli autovettori di una matrice quadrata A di ordine n
	Sia A una matrice quadrata n×m, v è chiamato **autovettore** se esiste un numero $\lambda$ tale che valga la relazione $A * v = \lambda * v$ ciò equivale a richiedere che $(A-\lambda I)v = 0$ dove $I$ è la matrice di identità ammette soluzioni non nulle se e solo se $det(A-\lambda I) = 0$ , questo vuol dire che quando la matrice A agisce sull'autovettore v il risultato è un vettore parallelo a v scalato di un fattore $\lambda$
	Gli autovettori rappresentano le direzioni le quali una trasformazione lineare agisce semplicemente come una dilatazione o una compressione, l'autovalore associa a quanto viene dilatato o compresso l'autovalore nella sua direzione:
	- Se $\lambda>1$ la trasformazione allunga il vettore
	- Se $0<\lambda>1$ la trasformazione accorcia il vettore
	- Se $\lambda = 1$ il vettore è invariato 
	- Se $\lambda = 0$ il vettore viene trasformato nel vettore nullo
	- Se $\lambda<0$ il vettore viene invertito nella sua direzione 
	L'autovettore viene prevalentemente utilizzato nell'analisi statistica per ridurre la dimensionalità e trovare le direzioni principali di varianza
	In R funzione `eigen(A)` calcola gli autovalori e gli autovettori di una matrice A, il risultato è una lista di due componenti:
	- Un vettore di nome **values** contenente gli autovalori 
	- Una matrice di nome **vectors** che contiene i corrispondenti autovettori sulle colonne
	Questi due componenti possono essere usati in istruzioni di assegnazione utilizzando `eigen(A)$values` e `eigen(A)$vectors` rispettivamente.
#STATISTICA_DESCRITTIVA
**STATISTICA DESCRITTIVA**
	La statistica nella ricerca è formata da quattro parti fondamentali 
	- Raccolta dati
	- Elaborazione dei dati 
	- Descrizione dei dati
	La statistica si differenzia in due branche:
	-**Descrittiva** che si occupa della presentazione e sintesi dei dati 
	 -**Inferenziale** che permette di trasferire le informazioni ottenute su un campione all'intera popolazione
	La statistica descrittiva è l'analisi dei fenomeni osservabili, queste analisi vengono fatte attraverso **l'osservazione del comportamento** delle caratteristiche **visibili** di un generico fenomeno. Dall'osservazione possiamo **misurare, contare e osservare** i valori assunti da X e possiamo analizzare le caratteristiche di un fenomeno ovvero **associare una variabile di ogni caratteristica osservabile di un fenomeno**.
	 La statistica descrittiva è una branca della statistica che si concentra sulla **raccolta**, sull'**organizzazione**, sull'**analisi** e sulla **presentazione dei dati** in modo da riassumere e descrivere le principali caratteristiche di un insieme di dati, le principali tematiche di cui si occupa sono:
	 - Misure di centralità (media campionaria, mediana, moda)
	 - Misure di dispersione (varianza, derivazione standard)
	 - Grafici e tabelle
	 - Misura della forma della distribuzione 
	 - Percentili e quantili 
	 - Frequenze e percentuali
	**GRAFICI IN R**
		R è dotato di un ambiente grafico per la creazione dei grafici.
		**GRAFICI PER VETTORI**
			Consideriamo un vettore x contenente un tipo di dato quantitativo, ossia numeri allora possiamo usare la funzione `plot(x)` che illustra l'andamento dei valori assoluti del vettore rispetto ai relativi indici
			![[Pasted image 20251008141221.png]]connettendo i punti mediante linee possiamo creare una **serie storica** dei dati visualizzati utilizzando la funzione `plot()` con `type = 1` che permette di creare le linee
			![[Pasted image 20251008141327.png]]
			Possiamo anche procedere tramite la funzione `lines()` che viene utilizzato per aggiungere linee a un grafico esistente, molto utili quando si vogliono sovrapporre ad un grafico precedentemente creato con `plot()`
	 **SERIE TEMPORALI**
		 Una serie temporale è una sequenza di osservazioni di una variabile raccolte e registrate ad intervalli di tempo regolari, l'obiettivo è quello di analizzare i dati per identificare pattern o tendenze che possano aiutare a fare previsioni sul futuro **(forecasting)**.
		 Una **serie temporale univariata** analizza **una sola variabile** misurata nel tempo, ponendo l'attenzione sulla dinamica temporale di una singola quantità![[Pasted image 20251008142217.png]]
		 Una serie temporale può essere memorizzata in un vettore **se i dati sono univariati** o  in una matrice se sono **multivariati**, R dispone di una specifica funzione `ts()` per rappresentare i valori di una serie temporale insieme ad alcune altre caratteristiche
		 `y <- ts(x, start =, frequency =, deltat=, end=)` dove:
		 - x: valori della serie 
		 - start: istante iniziale temporale
		 - frequency: numero di osservazioni nell'unità di tempo 
		 - deltat: la distanza temporale tra le osservazioni
		 - end: istante finale
		 La funzione `window()` è utile per lavorare con serie temporali quando si vuole isolare o analizzare un sottoinsieme di dati temporali, il comando è `window(x,start,end)`
		 dove:
		 - x: oggetto di tipo ts da cui estrarre una sottoserie 
		 - start: il punto di inizio della sottoserie
		 - end: il punto di fine della sottoserie
	**TS STUDIO**
		è una libreria avanzata per R specializzata nell'analisi e nella visualizzazione di serie temporali, è progettata per fornire un insieme completo di strumenti per lavorare con dati temporali in modo efficiente e intuitivo TS studio è:
		- un toolkit integrato 
		- interfaccia user-friendly
		- ponte tra analisi e visualizzazione
	**BARPLOT**
		Un barplot è una rappresentazione grafica che utilizza barre di lunghezza variabile per mostrare le frequenze o altre misure quantitative, i barplot servono per:
		- Comparazione
		- visualizzazione di dati aggregati
		- rappresentazione di distribuzione
		è utilizzato per dati categoriali per rappresentare aggregazioni di dati, ci sono vari tipi di barplot:
		- tradizionali
		![[Pasted image 20251008143650.png]]
		- Grouped BarPlot
		![[Pasted image 20251008143733.png]]
		-Stacked barPlot
		![[Pasted image 20251008143914.png]]
		Supponiamo ora di avere una matrice di dati numerici, a partire da essa è possibile creare dei vettori contenenti gli elementi delle singole colonne, le unità di misura in questo caso sono importanti dato che spesso dobbiamo procedere ad una standardizzazione dei dati per avere dei numeri puri, ossia privi di una unità di misura, un semplice modo di standardizzazione è quello di dividere gli elementi di ogni colonna per la somma dei valori della colonna presa in questione.
	**SCATTERPLOT**
		Consideriamo un campione costituito da n coppie di osservazioni di **tipo quantitativo** Le relazioni tra coppie di dati quantitativi possono essere rappresentate mediante **diagrammi di dispersione (scatterplot)** in cui ogni coppia di osservazioni viene rappresentata sotto forma di **un punto in un piano euclideo**, dopo aver scelto la variabile da porre sulle ascisse **variabile dipendente** e la variabile da porre sulle ordinate (variabile indipendente), si disegnano dei punti in corrispondenza delle coppie, il risultato finale è una nuvola di punti che può essere ottenuto con `plot(x,y)`, il grafico ottenuto mira ad evidenziare se le coppie di punti presentano una regolarità e tende ad evidenziare eventuali **relazioni tra le variabili** 
		![[Pasted image 20251008151053.png]]
		 La funzione `pairs()` è in grado di visualizzare in un'unica finestra grafica una pluralità di grafici per punti ottenuti in relazione a tutte le coppie di variabili quantitative definite all'interno di un dataframe
	**GRAFICI DI FREQUENZA E CONTIGENZA**
		**DISTRIBUZIONE DI FREQUENZA**
			consideriamo una variabile X e indichiamo con $z_1, z_2, z_3 .. z_k$ le modalità distinte da essa assunte, se la variabile X:
			- è **qualitativa** le modalità indicano delle qualità distinte degli individui
			- è **quantitativa** le modalità sono dei numeri reali distinti
			Prendiamo un campione $x_1, x_2 ... x_n$ costituito da n osservazioni di X, se indichiamo con $n_i$ il numero di volte in cui ciascuna osservazione di $z_i$ è presente nel campione (frequenza assoluta) allora l'insieme ${(z_i,n_i),i = 1, 2 ...,k}$ si chiama **distribuzione di frequenza** ovvero l'insieme formato dalle coppie di valore assunto dalla variabile e frequenza assoluta
			![[Pasted image 20251009114435.png]]
			![[Pasted image 20251009114513.png]]
			Se non esistono dati mancanti, la somma delle frequenze assolute è sempre uguale alla numerosità del campione $n = n_1 + n_2 + ... + n_k$ 
			La **frequenza relativa** di un evento è il rapporto tra la frequenza assoluta di quell'evento e il numero totale di osservazioni, viene espressa come frazione o percentuale e indica la proporzione con cui un determinato evento si verifica
			$Frequenza relativa = \frac {Numero totale di osservazioni}{Frequenza assoluta dell'evento}$
			 In R la costruzione di una distribuzione di frequenza si fa tramite `table()` che crea una **tabella di contingenza** che mostra la frequenza assoluta degli elementi unici di un vettore, la **tabella di contingenza** è una tabella che riassume la distribuzione congiunta di due o più variabili categoriali, mostrando frequenze assolute o relative con cui si verificano le combinazioni dei livelli delle variabili.
			 **La frequenza assoluta cumulata** rappresenta il numero totale di osservazioni che hanno un valore inferiore o uguale a un determinato valore in un insieme di dati, ovvero la somma delle frequenze assolute fino a quel punto nella  distribuzione
			 $N_i = n_1 + n_2 + ... + n_i$, fornisce un'idea di quante osservazioni si sono accumulate fino a un certo valore, R per calcolare la frequenza assoluta cumulata si usa **cumsum()**.
			 **La frequenza relativa cumulata** è la proporzione di osservazioni che hanno un valore inferiore o uguale a un determinato valore, ovvero la somma delle frequenze relative fino a quel punto nella distribuzione.
			 Le frequenze assolute e relative possono essere calcolate anche per variabili quantitative sempre che il numero di modalità distinte sia ben definito, spesso le informazioni vengono **raccolte in classi**.
		**FREQUENZE NEI DATI**
			**Gestione dei dati mancanti**: quando ci sono valori mancanti, si può usare la frequenza assoluta delle categorie per decidere come imputare i valori mancanti, es. sostituire i valori mancanti con categoria più frequente nei dati categoriali
			**Ribilanciamento dei dataset sbilanciati**: Nei problemi di classificazione binaria o multiclass sbilanciati, le frequenze relative delle classi vengono usate per bilanciare i dati applicando tecniche come **downsampling** (ridurre il numero di campioni della classe maggioritaria) o **upsampling** (replicare campioni della classe minoritaria)
			**Encoding di variabili categoriali**: Le frequenze relative delle categorie possono essere utilizzate per trasformare variabili categoriali in valori numerici, il processo è detto **target-encoding**, questo processo è utili per variabili con molte categorie dove una semplice **one-hot encoding** potrebbe essere insufficiente.
