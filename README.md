# Esercizio del 23 maggio 2017

A partire dalla scena del combattimento tra cowboy, si aggiunga una interfaccia grafica che disponga dei controller di seguito elencati. Tra parentesi è indicata l'/le immagine/i da usare per la personalizzazione dell'UI element.
Tutti gli UI elements si trovano su un panel che ha come sfondo l'immagine menuBackground.jpg



1. Un selettore che permette di accendere e spegnere la luce nella scena (lighton e lightoff)
2. Uno slider che permette di controllare l'intensità luminosa della luce presente
3. Ancorati in basso alla destra e sinistra della UI, si trovano tre bottoni che servono rispettivamente a:
	3.1 muovere il personaggio in avanti (arrow)
	3.2 attaccare l'avversario (punch)
	3.3 muovere il personaggio indietro (arrow)

Per ciascun cowboy nell'angolo in alto a sx/dx si troverà un indicatore della energia residua che in assenza di colpi aumenta in maniera costante di 5% al secondo.
L'accesso via script al componente Image script associato agli UI element si ottiene per mezzo di:
	
	- using UnityEngine.UI;
	- Image i = getComponent<Image>();
	- i.fillAmount //per accedere o modificare il valore corrente di filling dell'immagine.
	
La progress bar va implementata attraverso l'uso di ImageType Filled con riempimento radiale a 360 gradi (un semicerchio). La progress bar deve essere di colore diverso per i due cowboy. La sprite di default da usare è Knob (generalmente importata di default da unity in caso contrario una immagine circolare colorabile). Il valore di fillAmount dello script Image deve essere impiegato per visualizzare la percentuale di energia (dal momento che esso varia tra 0 e 1 è facilmente impiegabile allo scopo).
Il cowboy colpito potrà pertanto morire solo nel momento in cui il colpo ricevuto porta la sua energia residua al di sotto dello 0%.

Qualsiasi button nella scena deve essere animato attraverso il transition mode Animation che espande leggermente il pulsante quando il mouse è sopra il pulsante e ne cambia il colore quando viene premuto.


