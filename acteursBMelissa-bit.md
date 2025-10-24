classDiagram
    Acteurs <|-- Apprenants 
    Acteurs <|-- Organismes
    Acteurs <|-- Entreprises
    Acteurs: Niveau Bac 
    Acteurs: Maitise des langues
    Acteurs: Compétences numériques()
    Acteurs: 
    class Apprenants{
       +String nom
    +int age
    +String niveau d'étude 
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
