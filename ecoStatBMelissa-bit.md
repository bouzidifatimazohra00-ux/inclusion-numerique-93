# Environnement statistique pour l’insertion professionnelle post-formation numérique en Île-de-France

Modélisation qui s’inspire de l’écosystème des parcours professionnels et des dynamiques d’emploi dans le secteur numérique.

## Sources de données (data brutes)

Pour construire cet environnement statistique, nous utilisons plusieurs types de sources de données :  

- **Open Data publique** :  
  - [INSEE – Emploi et formations](https://www.insee.fr/fr/statistiques) : données sur l’emploi par secteur, âge, niveau d’étude et région.  
  - [Pôle Emploi – statistiques régionales](https://statistiques.pole-emploi.org/) : offres et demandes d’emploi dans le numérique en Île-de-France.  
- **Jeux de données spécifiques au numérique** :  
  - [Kaggle – Tech Jobs Dataset](https://www.kaggle.com/datasets) : offres d’emploi tech et profils recherchés.  
  - [Diigo – #ACEHN #statistiques](https://www.diigo.com/user/luckysemiosis?query=%23ACEHN+%23statistiques) : références de sources complémentaires.  
- **Enquêtes et études professionnelles** : rapports de [Syntec Numérique](https://syntec-numerique.fr/) sur les parcours des jeunes diplômés dans le numérique.  

Ces données brutes permettent d’analyser l’insertion professionnelle des diplômés dans le secteur numérique et d’identifier les tendances de l’emploi en Île-de-France.

## Data tables

La structuration des données se fait sous forme de tables, par exemple :  

| Propriété         | Valeur              | Critère                        |
|------------------|-------------------|-------------------------------|
| Âge               | 25                | Jeune diplômé                 |
| Formation         | Développement Web | Niveau Bac+3                  |
| Statut emploi     | CDI               | 6 mois après formation        |
| Région            | Île-de-France     | Localisation                  |
| Salaire moyen     | 32 000 €          | Annuel brut                   |
| Type de poste     | Développeur Front | Secteur numérique             |

Cette table peut être complétée par d’autres colonnes : expérience précédente, type de contrat, entreprise, satisfaction au travail, etc.

## Structures visuelles

Pour rendre les données compréhensibles et navigables, plusieurs types de visualisations sont envisagés :  

- **Pie chart (diagramme circulaire)** : répartition des types de contrats ou des secteurs d’activité.  
- **Bar chart (diagramme en barres)** : nombre de diplômés par type de formation ou par région.  
- **Heatmap** : zones géographiques avec densité d’insertion professionnelle.  
- **Line chart** : évolution du taux d’emploi sur plusieurs années.  

Exemple : un pie chart permet de visualiser la proportion de CDI, CDD, et stages parmi les diplômés du numérique.

## Représentations de données (D3)

En utilisant D3.js pour le rendu interactif :  

- **Pie chart** :  
  - La taille des segments est proportionnelle au nombre de personnes pour chaque type de poste ou contrat.  
- **Bar chart** :  
  - La hauteur des barres correspond au nombre de diplômés ou aux offres d’emploi disponibles par région.  
- **Heatmap interactive** :  
  - Chaque cellule colorée indique le taux d’emploi par département.  

Ces représentations répondent à des questions comme :  
- Quel est le taux de CDI versus CDD après la formation ?  
- Quelle formation permet la meilleure insertion en Île-de-France ?  
- Quelles zones géographiques offrent le plus d’opportunités dans le numérique ?  

## Interactions avec l’environnement

Pour enrichir l’expérience utilisateur et l’analyse :  

- **Hover (passage de la souris)** : afficher des informations détaillées (nombre exact de personnes, salaire moyen, type de contrat).  
- **Filtrage dynamique** : possibilité de filtrer par âge, formation, région ou type de contrat.  
- **Zoom et sélection** : pour explorer des régions spécifiques ou des types de postes précis.  
- **Export des données** : téléchargement des résultats filtrés pour analyse externe.
