graph TD
    %% Style Général
    classDef avant fill:#fcf8e3,stroke:#f0ad4e,stroke-width:2px,color:#8a6d3b;
    classDef après fill:#d9edf7,stroke:#31708f,stroke-width:2px,color:#31708f;
    classDef important fill:#dff0d8,stroke:#3c763d,stroke-width:3px,color:#3c763d;
    classDef recruteur fill:#f2dede,stroke:#a94442,stroke-width:2px,color:#a94442;

    subgraph "AVANT HN-TRANSFORM : Un parcours dispersé"
        A1[Formation] --> A2[Projets]
        A2 --> A3[Stages / Alternance]
        A3 --> A4[Compétences]
        A4 --> A5[Recruteur]
    end

    subgraph "APRÈS HN-TRANSFORM : Un parcours structuré"
        B1[Formation] --> B2[Projets / Expériences / Stages / Alternance]
        B2 --> B3[Compétences identifiées et hiérarchisées]
        B3 --> B4[💼 Portfolio HN-TRANSFORM]
        B4 --> B5[Profil lisible pour le recruteur]
    end

    %% Application des styles
    class A1,A2,A3,A4 avant;
    class B1,B2,B3 après;
    class B4 important;
    class A5,B5 recruteur;
