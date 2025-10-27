
```mermaid
classDiagram
direction TB
    class Institut {
	    +école
	    +centre de formation
	    +université}
    class Responsable {
      administration
      coordinateurs
      enseignants}

    class Apprenant {
	   Jeunes diplômés
	   Jeunes nan diplômés
   }
    Institut <|-- Apprenant
    Institut <|-- Responsable
```
