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