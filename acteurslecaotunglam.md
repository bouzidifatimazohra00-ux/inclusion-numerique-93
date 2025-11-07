
```mermaid
classDiagram
     
    Oragnisme <|-- Pro_org
    Oragnisme <|-- Edu_org
    Pro_org <|-- Association
    Edu_org <|-- Association
    Pro_org <|-- Entreprise
    Edu_org <|- Centre-de-formation
    
    
    class Oragnisme{
        +String name
        +isPublic()
        +isActive()
        +String domaine
        +int Capacité
    }
    
    class Org_prestataire{
        
    }
    class Association {
    }
    
    class Centre-de-formation{
      
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
