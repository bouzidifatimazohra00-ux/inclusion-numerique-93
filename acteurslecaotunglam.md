
```mermaid
classDiagram
     
    Oragnisme <|-- Centre-de-formation
    Oragnisme <|-- Entreprise
    Centre-de-formation <|-- Etudiant
    Entreprise <|-- Etudiant
    class Oragnisme{
        +String name
        +isPublic()
        +isActive()
        +String domaine
    }
    class Centre-de-formation{
      +int Capacité
    }
    class Entreprise{
    
    }
    class Etudiant{
        + String name
        + String DOB
        + 
      +bool enFormation
      +run()
    }
```
