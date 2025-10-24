classDiagram
    Acteur <|-- Apprenants
    Acteur <|-- Organismes
    Acteur <|-- Entreprises
    Acteur : Lieu geographique
    Acteur : Type d'acteur
    Acteur : Satisfaction
    Acteur: +isMammal()
    Acteur: +mate()
    class Apprenants{
      +texte Niveau de formation
      +texte Genre
      +texte Age
      +texte Duree de la formation

      +swim()
      +quack()
    }
    class Organismes{
      +texte Taux de reussite
      +texte Capacite d'accueil
      +texte Type de formation
      +texte Specialite

      -canEat()
    }
    class Entreprises{
      +texte Salaires post-formations
      +texte Secteur d activite
      +texte Type de contrat
      +texte Competences recherchees
      +run()
    }
