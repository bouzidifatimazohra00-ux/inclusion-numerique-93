
```mermaid
classDiagram
direction TB
    class Institut {
	    +association
	    +centre de formation}
    class Responsable {
      administration
      coordinateurs
      enseignants}

    class Apprenant {
	   jeune diplome
	   sans diplome
       Salarie en activiter
       recovention professionnelle
   }
    Institut --> Apprenant:forme  
    Responsable --> Institut:gère
    Responsable --> Apprenant:supervise
```

