# Space-Invaders
Il progetto Space Invaders intrapreso consiste nella riproduzione del cleberrimo videogioco in java con la classe.
Seguendo le linee guida del professore abbiamo intrapreso i primi step del lavoro, che consistevano sostanzialmente nella creazione e miglioramento grafico di quest'ultima.

  Step 1
In questo step abbiamo creato la classe Intro che serve ad aggiungere una scritta e degli elementi grafici, come per esempio l'pzione di cliccare la x in alto a destra per chiudere la finestra,questo è possibile perchè la classe Intro eredita la classe Space, che estende la classe canvas necessaria per prendere gli imput dell'utente come per empio il click del mouse o in imput di tastiera.

  Step 2
in questo step si vuole dare un' animazione alla scritta che compare facendola venire verso l'interno dello schermo,per far ciò si crea un metodo run all'interno della classe Intro e si richiama il metodo repaint(ereditato dalla classe Canvas) all' interno di un ciclo.Successivamente, dopo che la classe paint ha creato l'immagine, si chiama il metodio repaint che a sua volta richiama il metodo paint per eliminare l'immagine precedente.

  Step 3
In quest'ultimo step della prima parte abbiamo risolto il problema di sfarfallio derivantye dallo step precedente. Per permettere ciò
abbiamo creato due Canvas, facendo così in modo che quando un immagine viene creata e sviluppata, ci sarà subito un immagine successiva pronta asostituire quella precedente. Nel codice abbiamo quindi usato la classe BufferStrategy, derivante dalla classe Canvas. 

A livello hardware per far funzionare questo metodo dobbiamo prendere come esempio un monitor che può avere un refresh rate di 60hz,se non ci fossero 2 classi canvas vedremmo lo sfarfallio questo perchè se la scheda video sviluppasse 1 immagine con una durata di 5hz e poi la prossima sarà disponible solo dopo 2hz in questi 2hz vedremmo questo effetto di sfarfallio.

Con questa tecnica invece avendo a disposizione queste 2 classi canvas dopo lo sviluppo di 1 immagine sarà subito pronta la seconda eliminandoo questo effetto di sfarfallio.
