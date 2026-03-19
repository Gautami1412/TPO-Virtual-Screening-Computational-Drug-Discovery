# Computational Virtual Screening and Lead Identification of Natural Thyroid Peroxidase Inhibitors of Hyperthyroidism 

## Overview
End-to-end computational virtual screening and molecular dynamics pipeline to evaluate natural flavonoids as lower-toxicity alternatives to FDA-approved anti-thyroid drugs by comparing binding affinity and protein-ligand stability against Thyroid Peroxidase (TPO).

## Background
Hyperthyroidism affects 0.2–1.3% of the global population and is driven by overproduction of thyroid hormones T3 and T4 via Thyroid Peroxidase (TPO) which is the primary drug target for anti-thyroid therapeutics. While FDA-approved drugs like Methimazole competitively inhibit TPO, they carry significant toxicity liabilities (LD50 = 220 mg/kg), driving the need for safer alternatives. This study computationally evaluates four natural flavonoids — Rutin, Kaempferol, Mearnsitrin and Rosmarinic acid, as potential lower-toxicity alternatives by comparing their binding affinity and interaction stability against TPO with four pharmaceutical agents.

## Pipeline
```mermaid
flowchart TD
    A([**SEQUENCE RETRIEVAL**\nTPO MPO-like domain · UniProt P07202\nResidues 142-738])
    --> B([**HOMOLOGY MODELING**\nSwissModel])
    --> C([**STRUCTURE VALIDATION**\nProSA-web · Z-score = -10.57\nSAVES · Ramachandran >90% favored])
    --> D([**PROTEIN VISUALIZATION & PREPARATION**\nChimeraX])
    --> E([**LIGAND PROCUREMENT**\nPubChem · 4 Pharmaceutical + 4 Natural compounds])
    --> F([**MOLECULAR DOCKING**\nCBDock · AutoDock Vina])
    --> G([**MOLECULAR DYNAMICS SIMULATION**\nSchrödinger Desmond · 10ns · NPT · 300K\nRMSD · RMSF · Protein-Ligand Contacts])
    --> H([**TOXICITY & ADME SCREENING**\nProTox 3.0 · SwissADME])
    --> I([**LEAD CANDIDATE IDENTIFICATION**\nRutin · Binding Energy = -9.6 kcal/mol\nLD50 = 5000 mg/kg])

    style A fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style B fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style C fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style D fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style E fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style F fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style G fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style H fill:#4A90D9,stroke:#2C5F8A,color:#FFFFFF
    style I fill:#2C5F8A,stroke:#1A3A5C,color:#FFFFFF
```


