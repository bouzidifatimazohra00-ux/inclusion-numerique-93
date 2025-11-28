```mermaid
classDiagram

Acteur <|-- Apprenant
Acteur <|-- Professionnels

Professionnels <|-- OrganismeFormation
Professionnels <|-- Entreprise
Professionnels <|-- StructureAccompagnatrice

class Acteur {
  +string nom
  +string region
  +string adresse
  +string email
  +string telephone
}

class Apprenant {
  +string prenom
  +int age
  +string genre
  +string niveauEtudes
  -acteur aCommeActeur
  -Formation programmeSuivi       
  +string typeDispositif       
  +string financeurProgramme
  -Contrat contrat
  +float calculerSalaire()
  +string obtenirProgramme()
  +liste obtenirContrats()
  +int calculerAge()
}

class Professionnels {
  -acteur aCommeActeur
  +string codeAPE
  +string secteurActivite
  +string statutJuridique
  +int anneeCreation
  +int nbEmployes
  +string siteWeb
  +string contactPrincipal
  +string contactReferent
  +string role
  +liste obtenirApprenants()            
}

class OrganismeFormation {
  +Professionnels pcommeProfessionnel
  +string typeOrganisme
  +liste offresDeFormation()   
  +bool ajouterProgramme(string programmeNom)  
  +float calculerTauxReussite()  
  +liste obtenirCertifications()  
}

class Entreprise {
  +Professionnels pcommeProfessionnel
  +string typeOrganisme
  +liste obtenirContrats()
  +bool ajouterPartenaire(string partenaireNom)
}

class StructureAccompagnatrice {
  +Professionnels pcommeProfessionnel
  +string typeOrganisme
}

class Contrat {
  -acteur aCommeActeur
  +string contactRH
  +string idContrat
  +string typeContrat
  +date dateDebut
  +date dateFin
  +string statut
  +string apprenantAssocie
  +string entrepriseAssociee
  +float calculerSalaire()     
  +bool estActif()
  +int dureeContrat()
}

class Indicateur {
  +string nom
  +string definition
  +string unite
  +float valeur
  +int annee
  +float calculerIndicateur()
  +float comparaisonAnneePrecedente()
  +bool estConforme()
}

class Formation {
  -acteur aCommeActeur
  +String intituleFormation
  +String certification
  +Date dateDebut
  +Date dateFin
  +int dureeHeures
  +string format
  +string financement
  +isSurPlace()
}
```
