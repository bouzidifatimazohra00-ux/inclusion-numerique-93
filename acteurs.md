```mermaid
classDiagram
class Apprenant {
  +string nom
  +string prenom
  +string adresse
  +string email
  +string telephone
  +int age
  +string genre
  +string niveauEtudes
  +string intituleFormation
  +string typeDispositif
  +string financeurProgramme
}

class OrganismeFormation {
  +string adresse
  +string email
  +string telephone
  +string typeProfessionnel      %% OrganismeFormation, Entreprise, StructureAccompagnatrice
  +string intituleFormation    
  +string statutJuridique        %% privé, public, association, SCIC
  +string codeAPE
  +string secteurActivite
}

class Entreprise {
  +string nom
  +string adresse
  +string email
  +string telephone
  +string statutJuridique        %% privé, public, association, SCIC
  +string codeAPE
  +string secteurActivite
  +string contactRH
  +string siteWeb
}

class ContratDeTravail {
  -Apprenant aCommeApprenant
  -Entreprise aCommeEntreprise
  -OrganismeFormation aCommeOrganismeFormation
  +string idContrat
  +string typeContrat
  +date dateDebut
  +date dateFin
  +string statut
  +float calculerSalaire()     
  +bool estActif()
  +int dureeContrat()
}

class Formation {
  -Apprenant aCommeApprenant
  -Professionnel aCommeOrganismeFormation
  +string intituleFormation
  +string certification
  +date dateDebut
  +date dateFin
  +int dureeHeures
  +string format
  +string financement
  +bool isSurPlace()
}

%% Relations simplifiées
Apprenant --> Formation : suit
Apprenant --> ContratDeTravail : a
Apprenant --> Entreprise : signeContrat
Apprenant --> OrganismeFormation : inscrit
Entreprise --> ContratDeTravail : propose
ContratDeTravail --> OrganismeFormation : contient
Formation --> OrganismeFormation : dispensée par

```
