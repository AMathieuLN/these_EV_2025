# Codes et données de réplication pour : "Économie politique des emplois verts : informalité dans les Suds et quête d'une transition juste 
## Description

Ce dépôt regroupe tous les codes et données pour reproduire les chapitres 2 et 3 de ma thèse intitulée "Économie politique des emplois verts : informalité dans les Suds et quête d'une transition juste". 

Les données sont aux formats .RDS, .XLSX ou .CSV. 

Ces jeux de données et codes sont fournis uniquement dans un objectif de reproductibilité de notre travail de thèse. Nous ne sommes pas les concepteurs ni les propriétaires de l'ensemble des données utilisées. Pour un usage approfondi ou autonome, il est fortement recommandé de consulter directement les sources originales, afin de bénéficier des éventuelles mises à jour, d’éviter toute déformation liée à notre traitement, et de garantir une citation adéquate des auteur·e·s des données. Ces derniers sont systématiquement mentionnés dans notre manuscrit de thèse et nos scripts disponibles aux formats .qmd et .pdf.

A noter que les fichiers contenant comportant les mêmes noms que leur source ILO correspondent à des données issues de nos traitements, dans lesquels nous avons notamment introduit une classification des emplois à fort potentiel de verdissement (EFPV), utilisée dans le chapitre 2. Le fichier nommé efpv_sustainability résulte de la fusion entre le jeu de données modifié EMP_TEMP_SEX_EDU_EC2_NB_A et la base sustainability, mobilisée pour les analyses du chapitre 3.

Les données comportant les noms ILO sont le fruit de notre travail avec nos modifications et ajouts d'une catégorie d'emplois à fort potentiel de verdissement (EFPV) servant pour le chapitre 2, et les données de "efpv_sustainability" sont issues de la fusion du jeu de données modifié ici "EMP_TEMP_SEX_EDU_EC2_NB_A" et de "sustainability" servant pour le chapitre 3. 

Pour une présentation complète des enjeux, des intérêts analytiques et des résultats tirés de ces données, nous vous invitons à consulter notre manuscrit de thèse disponible ici : [lien].


## Structure du dépôt

```{r}

├── data/                      # Données brutes originales
│   ├── IV/                    # Fichiers du IV framework
│   │   ├── first_iv.xlsx
│   │   ├── UNCTAD_classification.xlsx
│   │   └── incomegroup_WDI.xlsx
│   ├── freedom/               # Freedom House Excel original
│   │   └── Country_and_Territory_Ratings_and_Statuses_FIW_1973-2024.xlsx
│   ├── pwt/                   # Penn World Table Excel original
│   │   └── pwt1001.xlsx
│   ├── ndgain/                # ND-GAIN CSV original
│   │   └── vulnerability.csv
│   ├── informal/              # Informal Economy Database Excel originaux
│   │   ├── DGE.xlsx
│   │   └── MIMIC.xlsx
│   └── gini/                  # Gini CSV original
│       └── tabulated_adm0_gini_disp.csv
│
├── scripts_chap2/             # Chapitre 2 : verdissement des emplois dans les Suds
│   ├── code_SAGE_github.qmd   
│   ├── code_SAGE_github.pdf
│   ├── chap2_replication.qmd  
│   └── chap2_replication.pdf
│
├── scripts_chap3/             # Chapitre 3 : performances économiques et soutenabilité
│   ├── chap3_model1_replication_annex.qmd
│   ├── chap3_model1_replication_annex.pdf
│   ├── chap3_model2_replication_annex.qmd
│   ├── chap3_model2_replication_annex.pdf
│   ├── chap3_model3_replication_annex.qmd
│   └── chap3_model3_replication_annex.pdf
│
├── outputs/                   # Jeux de données finaux (RDS / CSV)
│   ├── IV.rds                 # IV framework nettoyé
│   ├── <ilostat_indicator>.rds  # 23 fichiers ILOSTAT transformés
│   ├── efpv_sustainability.rds/.csv  # fusion ILOSTAT + sustainability
│   └── sustainability.rds/.csv      # fusion WDI, Freedom, PWT, ND-GAIN, Informal, Gini
├── README.md                                  
└── .gitignore                 # Exclusions Git

```

## Prérequis

Assurez-vous que les dernières versions de R et de RStudio sont installées sur votre système.

## Étapes pour la réplication


