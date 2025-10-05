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