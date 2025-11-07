# Environnement statistique pour l’insertion professionnelle post-formation numérique en Île-de-France

Modélisation des dispositifs et dynamiques régionales 


## Sources de données (data brutes)

Le jeu de données utilisé comptabilise le nombres d'entrées en formation des demandeurs d’emploi et ont été enregistrées par France Travail et les Conseils régionaux. 

Ce jeu de données est composé de données quantitaives (la région de formation, le type de dispositif de formation ou de financement ainsi que la période) et provient du portail data.gouv.fr. 

[Jeu de données sur "Entrées en formation des demandeurs d’emploi"](https://www.data.gouv.fr/datasets/entrees-en-formation-des-demandeurs-demploi/) 


## Data tables
Le fichier contient 3 feuilles principales : descriptif, région et types de formation. La table des rôles est organisé sous la forme de tableaux croisés simples des colonnes de priopriété  et des lignes de de valeurs mensuelles (Propriété = régions, valeur = nombre d’entrées en formation).


## Structures visuelles
Une représentation en diagramme circulaire ou en histogramme simple permettra de visualiser la répartition des entrées en fonction des dispositifs de financement par région. 


## Représentations de données (voir les exemples de D3)
- Une visualisation en diagramme circulaire consisterait à représenter, pour un mois donné : un type de formation (AIF, POE, Conseil régional, etc.) par segment du diagramme circulaire et la taille du segment serait proportionnelle au nombre d’entrées.
- Une visualisation en histogramme simple consisterait à représenter, pour un mois donné : les entrées en formation des demandeurs d’emploi selon les régions françaises.


## Interactions avec l'environnement
- Diagramme circulaire ou Histogramme simple : 
En passant sur un segment ou une barre, on affiche une info-bulle avec le nom de la région, le nombre exact d’entrées et la pourcentage en fonction le total national.
