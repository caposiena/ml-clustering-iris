# ML Clustering Iris

Progetto di clustering con KMeans e DBSCAN.

Nel lavoro ho applicato tecniche di clustering sul dataset Iris, utilizzando solo le feature senza le etichette originali. Prima di tutto ho standardizzato i dati con StandardScaler, così tutte le variabili hanno la stessa scala.

Ho iniziato con DBSCAN provando diversi valori di eps. Con eps = 0.35 ho ottenuto 4 cluster ma con molto rumore, con eps = 0.45 ho ottenuto 3 cluster con meno punti rumorosi, mentre con eps = 0.55 i cluster diventano 2. Il valore più equilibrato sembra essere 0.45, perché identifica 3 gruppi abbastanza chiari.

Successivamente ho applicato il metodo dell’Elbow usando KMeans, calcolando l’inertia per valori di K da 1 a 10. Dal grafico si nota un “gomito” intorno a K = 3, quindi anche questo metodo suggerisce che il numero ottimale di cluster è 3.

A questo punto ho eseguito KMeans con K = 3 e ho valutato il risultato usando il Silhouette Score, che risulta circa 0.48. Questo valore indica che i cluster sono abbastanza ben separati, anche se non perfetti.

Infine ho visualizzato i cluster in un grafico 2D utilizzando due feature, colorando i punti in base al cluster assegnato e mostrando anche i centroidi.

In conclusione, sia DBSCAN che il metodo dell’Elbow indicano che il numero migliore di cluster è 3, risultato coerente con la struttura reale del dataset Iris.