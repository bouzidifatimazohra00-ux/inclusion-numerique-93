```mermaid
lassDiagram
    Acteurs <|-- Apprenants 
    Acteurs <|-- Organismes
    Acteurs <|-- Entreprises
    Acteurs: Niveau d'etude 
    Acteurs: Maitise des langues
    Acteurs: Competences numeriques()
    Acteurs: 
    class Apprenants{
       +String nom
    +int age
    +String niveau d'etude 
    +String objectif professionnel ()
    +String competences numeriques ()
    }
    class Organismes{
      +String nom
    +String type d'organisme
    +String programmes numeriques
    +formerApprenant()
    +accompagner insertion()
    }
    class Entreprises{
      +String nom
    +String secteur
    +bool propose alternance
    +String besoins competences
    +recruter apprenant()
    +proposer stage()
    }
```
