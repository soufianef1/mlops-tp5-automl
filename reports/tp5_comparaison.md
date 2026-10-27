Modele manuel ou modele AutoML ? (TP05)
Critere	Manuel (rf 500/16)	AutoML (FLAML 90 s)
Famille de modele	RandomForest	XGBoost
F1 sur le jeu de test	0.8669	0.8561
Temps de recherche machine	1.6 s	90.1 s
Temps humain (estimation)	30 min à 1 h	quelques minutes
Latence mediane (ms)	48.6	8.1
Latence p95 (ms)	80.0	32.4
Taille du fichier (Mo)	13.37	0.28
Explicabilite	Nombre d'arbres, profondeur, importance des variables	Importance des variables mais réglages plus complexes
Decision
Je mettrais le modèle AutoML en production. Bien que son F1 (0.8561) soit légèrement inférieur à celui du modèle manuel (0.8669), il présente une latence beaucoup plus faible. Son fichier est également beaucoup plus petit (0.28 Mo contre 13.37 Mo), ce qui facilite le déploiement et réduit les coûts d'infrastructure. Le temps nécessaire pour obtenir le modèle est automatisé et ne dépend pas fortement de l'expertise humaine. Pour un service de prédiction en temps réel, les gains de performance et de portabilité compensent la légère baisse du F1.