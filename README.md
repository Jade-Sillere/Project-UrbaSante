# Project Urba Santé

Ce projet est le résultat d'une collaboration entre le MSc&T en Data and Economics for Public Policy à l'École Polytechnique, Telecom et ENSAE et l’ECOLAB, laboratoire d’innovation pour la transition écologique du Commissariat Général au Développement Durable.

Dans ce cadre, un challenge permettant le développement d’outils ancrés dans la communauté de la donnée en santé-environnement afin d’adresser des problématiques partagées a été organisé en 2023.

## Projet Urbasanté

En agissant sur nos comportements et nos modes de vies, l’aménagement du territoire a un rôle majeur dans la santé physique, mentale et sociale de la population. Globalement, en intervenant sur l'environnement, les habitudes de vie et les comportements, il est estimé que l'aménagement du territoir peut affecté jusqu'à 60% de la santé d'un individu.

Cependant, dans le contexte actuel de changement climatique, les services et le cadre de vie fournis par les écosystèmes urbains risquent de se détériorer considérablement, entraînant des conséquences sur la santé publique.

Or, la santé et l'environnement sont souvent gérés de manière indépendante au sein des territoires, avec peu d'interaction entre les deux domaines. Pourtant, les avantages potentiels pour la santé publique sont significatifs. Selon Santé publique France, près d'un tiers des cancers pourraient être évités en modifiant les habitudes de vie de la population.

Face à ce constat, il est nécessaire d'accompagner les décideurs locaux en leur fournissant un outil de sensibilisation, afin de les aider à mieux appréhender la thématique santé-aménagement. 

L'objectif de l'outil est ainsi d'accompagner les collectivités locales dans la réalisation de diagnostics en santé- aménagement de leurs territoires, en proposant une restitution des différents déterminants de santé à travers une plateforme de données cartographiques mettant en lumière des indicateurs en lien avec la santé-aménagement à une maille fine du territoire et pour l'ensemble de la France métropolitaine.


## **Les indicateurs**

Pour être visualisés à l'aide de l'outil de visualisation, à différentes résolutions spatiales, nous avons créé 29 indicateurs répartis entre 11 déterminants socio-sanitaires :

| Domaine                                     | Indicateur                               | Description                                             | Année |
|---------------------------------------------|------------------------------------------|---------------------------------------------------------|-------|
| Qualité de l'air                            | atmo                                     | Pourcentage de jours avec un ATMO score au-delà de 3/6 | 2022  |
| Qualité de l'air                            | somo35                                   | Score SOMO35                                           | 2022  |
| Gestion des eaux                            | Qualite des eaux souterraines           | Score correspondant à la somme des site pondérés        | 2020  |
| Gestion des eaux                            | secheresse                               | Risque pondérée de secheresse                          | 2024  |
| Biodiversité                                | mosquitos_pop                            | Dengue cases per million inhabitants                   |       |
| Biodiversité                                | pest_cmr                                 | Quantités de pesticides CMR achetés (kg)               | 2021  |
| Biodiversité                                | pest_env_a                               | Quantités de pesticides Env A achetés (kg)             | 2021  |
| Biodiversité                                | pest_env_b                               | Quantités de pesticides Env B achetés (kg)             | 2021  |
| Biodiversité                                | pest_sante_a                             | Quantités de pesticides Sante A achetés (kg)           | 2021  |
| Biodiversité                                | pest_sante_autres                        | Quantités de pesticides Autre (hors CMR, Env A, Env B et Sante A achetés) (kg) | 2021 |
| Température                                 | Couvert Forestier                        | Taux de couverture forestière                          | 2018  |
| Température                                 | surface_imperm                           | Taux de surface imperméabilisée                         | 2018  |
| Pollution lumineuse/luminosité              | Radiance                                 | Niveau de radiance                                      | 2015  |
| Sécurité                                    | Coupsetblessuresvolontaires             | Coups et blessures volontaires (taux)                   | 2022  |
| Sécurité                                    | Volssansviolencecontredespe             | Vols sans violence contre des personnes (taux)          | 2022  |
| Sécurité                                    | Cambriolagesdelogementtaux              | Cambriolages de logement (taux)                         | 2022  |
| Sécurité                                    | Usagedestupéfiantstaux2022              | Usage de stupéfiants (taux)                             | 2022  |
| Accès à l'emploi, aux services et aux équipements | equip_interm                        | Part de la population éloignée des équipements intermédiaires | 2021 |
| Accès à l'emploi, aux services et aux équipements | equip_proxim                        | Part de la population éloignée des équipements de proximité | 2021 |
| Accès à l'emploi, aux services et aux équipements | equip_sup                           | Part de la population éloignée des équipements supérieurs | 2021 |
| Accès à l'emploi, aux services et aux équipements | pourcentage_equip                   | Taux d'équipement de proximité accessibles             |       |
| Accès à l'emploi, aux services et aux équipements | Cyclabilitévoirie                   | Taux de la cyclabilité de la voirie                     |       |
| Accès à l'emploi, aux services et aux équipements | Cyclabilitévoirieavecvoirie          | Taux de la cyclabilité de la voirie (voirie 30)         |       |
| Activite physiques et sportives             | n_infra_sportive                        | Nombre d'infrastructure sportives accessibles           |       |
| Alimentation                                | part_surfconvterm                       | Part des surfaces agricoles biologiques                 |       |
| Habitat                                     | Partdesrésidencesprincipales            | Part des résidences principales suroccupées            |       |
| Revenu                                      | age_moins_25                            | Part des pers. âgées de - de 25 ans                     | 2020  |
| Revenu                                      | age_entre_25_64                        | Part des pers. âgées de 25 à 64 ans                     | 2020  |
| Revenu                                      | age_plus_65                             | Part des pers. âgées de 65 ans ou +                     | 2020  |

### **Installation**

Lors de l'exécution de l'outil de visualisation, veuillez vous assurer que vous avez téléchargé le fichier des indicateurs dans votre répertoire et que le chemin d'accès au fichier dans le code est modifié en fonction du chemin d'accès contenant ce fichier.

L'outil de visualisation a été conçu en R, il utilise le package Rshiny. Par conséquent, avant d'exécuter et d'éditer le code, assurez-vous que les paquets suivants sont installés :

install.packages("raster")
install.packages("sp")
install.packages("tmap")
install.packages("sf")
install.packages("dplyr")
install.packages("here")
install.packages("readr")
install.packages("readxl")
install.packages("shiny")
install.packages("leaflet")
install.packages("RColorBrewer")
install.packages("rmapshaper")
install.packages("shinythemes")

En outre, veuillez vous assurer que les fichiers de forme IRIS, communaux, départementaux et régionaux produits par l'INSEE se trouvent dans votre répertoire de travail. Ceux-ci se trouvent dans le dossier INSEE tables (Note : pour plus d'informations sur la structure, veuillez consulter la section sur la structure des fichiers ci-dessous).

### **Utilisation**

Prenons un exemple pour expliciter l'utilisation de l'outil. Un utilisateur souhaite connaître l’indicateur de couvert forestier à l'echelle départementale à travers la France métropolitaine. 

L’utilisateur sélectionne donc :
 
* Choisir un déterminant : Température
* Choisir un indicateur : Couvert Forestier
* Choisir une échelle : Departement

Et si un utilisateur souhaite connaître l’indicateur de couvert forestier à l'echelle communale dans un département (par example L'Essonne) et puis focaliser sur une commune (Palaiseau). 

L’utilisateur sélectionne donc :
 
* Choisir un déterminant : Température
* Choisir un indicateur : Couvert Forestier
* Choisir une échelle : Communes
* Choisir département à visualiser : Essonne
* Choisir localisation : Palaiseau

#### Carte

La cartographie est un graphique en gradient de l'indicateur sélectionné à la résolution spatiale choisie, allant de la valeur la plus basse dans l'intervalle des sept intervalles possibles correspondant au violet, jusqu'à la valeur maximale représentée en jaune. 

### **Limites de l'outil**

#### 1 - Données manquantes à une résolution spatiale
Par example, les iris n’ayant pas de données sont ceux où la population présente est faible et/ou des données Insee sont manquantes.  

#### 2 - Qualité des données 
Pour certains territoires et indicateurs, il peut y avoir des anomalies dans les données et c'est pourquoi il est nécessaire d’avoir une connaissance ou expertise locale permettant de remarquer l’apparition de certaines anomalies. 

### **Structure des fichiers**

├── README.md <- The top-level README for developers using this project.
├── LICENSE <- Licence for the repository (by default, MIT)
├── requirements.txt <- The requirements file for reproducing the analysis environment
├── data
│   ├── raw <- Original data
│   ├── intermediate  <- Intermediate data that has been transformed
│   └── processed  <- The final data set if transformed
│
├── docs <- Documentation of the code
│   └── examples <- Example of how to use it (notebooks) 
│
├── src <- Source code for use in this project.
│   ├── exploratory <- Exploratory scripts
│   ├── features <- Scripts to turn raw data into features for modeling
│   ├── models <- Scripts to train models and then use trained models to make
│   └── analysis <- Scripts to produce results
│
├── reports <- Generated analysis as HTML, PDF, LaTeX, etc.
│
└── app <- If relevant, scripts to run an app

## Contenu du Drive

Le Drive est divisé en 4 grands dossiers.

### "Fichiers Additionnels"

Ce dossier contient les fichiers qui capturent notre progression sur le projet (présentation de diapositives / suivi Excel).

### "Tables INSEE"

Ce dossier contient tous les fichiers shapefile de l'INSEE ou "table de passage" qui nous permettront de lier nos coordonnées brutes à des iris spécifiques, des communes, des départements et des régions en France.

#### 1- Iris INSEE

Les communes avec au moins 10 000 habitants et la plupart des communes avec entre 5 000 et 10 000 habitants sont divisées en unités IRIS. Ce fichier contient le shapefile Iris "CONTOURS-IRIS.shp" qui est le seul importé. Les autres ne contiennent que d'autres informations directement reconnues par le logiciel de programmation.

#### 2- Communes INSEE

Celui-ci contient le shapefile pour les communes en France "communes-20220101.shp" avec les autres fichiers (avec différentes extensions) contenant des informations automatiquement lues par le logiciel comme précédemment.

#### 3- Départements INSEE

Identique aux précédents mais pour les départements en France. Notez que ce shapefile séparait la ville de Lyon et le département "Rhône" (?) donc nous avons dû manipuler ce shapefile afin de fusionner ceux-ci pour inclure Lyon dans "Rhône". Le shapefile final utilisé dans notre flux de travail d'indicateurs est "New Version/departement_shapefile.rds" dans ce fichier.

#### 4- Régions INSEE

Contient le shapefile pour les régions en France avec les autres fichiers (avec différentes extensions) contenant des informations automatiquement lues par le logiciel comme précédemment.

#### Flux de Manipulation INSEE

Contient le script R utilisé pour modifier le shapefile précédent du département.

#### France_shapefile

Ce fichier contient les shapefiles pour la France (à différentes résolutions) qui ont été utilisés lorsque nous avons dû découper la France à partir d'un fichier satellite mondial.

#### Tables de Passage

Ce dossier contient des fichiers Excel de l'INSEE qui nous ont permis de lier nos indicateurs à différentes échelles (des communes aux départements...) en utilisant des codes INSEE universels.

### "Indicateurs"

Le dossier contenant les informations pour chacun de nos indicateurs. Vous trouverez d'abord un fichier pour chacun des déterminants. Ensuite, pour chaque déterminant, un fichier pour chaque indicateur. Chaque fichier d'indicateur comprend les éléments suivants :

#### Code / Flux de travail

Ce fichier contient les scripts utilisés pour créer les indicateurs, avec des annotations expliquant le processus inclus dans ces fichiers. Comme indiqué précédemment, ils peuvent être présents dans différentes extensions lorsque différents langages de programmation sont utilisés.

#### Données

Contient les données recueillies pour la construction de l'indicateur. Comme mentionné précédemment, celles-ci peuvent être présentes dans différents formats spécifiques à un indicateur (géospatial, JSON, Excel...)

#### Indicateur

Contient l'indicateur (au format Excel) ou un objet spécifique (RDS) pour les données satellites.

### "RShiny"

Ce dossier contient tout le code relatif à l'outil de visualisation programmé en R, en utilisant le paquet RShiny.

#### Graphique

Contient le code pour et les images de graphiques individuels des indicateurs.

### **Contributions**

Si vous souhaitez contribuer à ce projet, merci de bien vouloir nous contacter:

Awadalla Carreño Alfonso - alfonso.awadalla-carreno@polytechnique.edu
Jade Sillere - jade.sillere@polytechnique.edu
Julian Rojas - julian.rojas@polytechnique.edu
Maela Guillaume-Le-Gall - maela.guillaume-le-gall@polytechnique.edu
Sofia Vaca - sofia.vaca@polytechnique.edu

### **Remerciements**

Nous tenons à remercier l'équipe d'ECOLAB pour avoir proposé ce défi et pour toute l'aide apportée au cours du développement de cet outil. Nous remercions en particulier Paul Grignon et Theo Sigiscar pour le temps qu'ils nous ont consacré et les conseils qu'ils nous ont prodigués tout au long de ce projet. Par ailleurs, ce projet a été réalisé dans le cadre du MSc&T in Data and Economics for Public Policy et nous tenons à remercier nos directeurs de master Pierre Boyer et Franck Malherbet pour avoir organisé ce challenge avec ECOLAB et pour leur soutien constant.

### **Liens de l'outil du GD4H**

Lors du Challenge Green Data for Health organisé par l'Ecolab du Commissariat général au développement durable en 2023, un premier outil a été développé pour aider les acteurs du territoire à identifier les inégalités sociales de leurs territoires.

Bien que notre outil ait été défini indépendamment de l'outil développé dans le cadre de GD4H, cet outil a fourni un point de référence solide pour la structure du projet et s'est appuyé sur l'objectif général d'aider les acteurs locaux à comprendre les performances de leurs régions sur différents indicateurs. 

[Urbasante Tool from GD4H Challenge - Urbasanté](https://urbasante.shinyapps.io/indic_urbasante/)
[GD4H Challenge - Urbasanté](https://gitlab.com/data-challenge-gd4h)

### **Licence**

Le code est publié sous licence [MIT](/licence.MIT).
