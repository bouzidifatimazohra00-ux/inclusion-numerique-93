
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
	   Recherche d’emploi
	   chômeur
       travailleur
   }
    Institut --> Apprenant:forme  
    Responsable --> Institut:gère
    Responsable --> Apprenant:supervise
```

