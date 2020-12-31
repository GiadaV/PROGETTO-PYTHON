# PROGETTO-PYTHON

## Costruzione di portafogli diversificati mediante algoritmi di clustering 

Utilizzando diversi algoritmi di *clustering* partizionale e gerarchico, i rendimenti di circa 200 titoli azionari, provenienti dall'indice Nasdaq e selezionati casualmente, vengono suddivisi in *cluster* omogenei sulla base della correlazione. 

La bontà di ogni algoritmo di *clustering* viene valutata in base alla correlazione infra- e intra-*cluster* e alla numerosità di ogni *cluster* prodotto. 

I *cluster* ottenuti vengono utilizzati per formare dei portafogli *equally weighted* (in cui la stessa percentuale di capitale è investita in ogni *asset*) contenenti gli *asset* appartenenti ad ogni *cluster*. Si forma poi un portafoglio contenente tutti gli *asset* disponibili calcolando i pesi ottimali per ogni *cluster*.

Oltre all'ottimizzazione statica, i pesi ottimali di portafoglio sono calcolati su finestre *rolling* giornaliere di ampiezza annuale, che simulano un ribilanciamento giornaliero del portafoglio sulla base dei rendimenti storici osservati nell'ultimo anno. 

Per ogni algoritmo di *clustering*, i risultati delle stime statiche e *rolling* sono confrontati al fine di calcolare l'extrarendimento dovuto al ribilanciamento.

I rendimenti generati da ogni portafoglio di *clustering* sono confrontati *out of sample* con il portafoglio di tangenza, ottenuto applicando la stessa metodologia sopra descritta all'intero universo di *asset*, e con un portafoglio *equally weighted*. Si confrontano sia gli extrarendimenti cumulati rispetto ad un tasso privo di rischio che i rendimenti corretti per il rischio. 
