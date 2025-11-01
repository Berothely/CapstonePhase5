<center>

# **Prédiction du risque d’insécurité alimentaire en Haïti**



###  Projet Capstone réalisé dans le cadre du Bootcamp de Data Science & Intelligence Artificielle 
    
    
### Akademi (powered by Flatiron School)
<br/>
<hr>  
    
    
 
**Rédigé par :**  
                **Richecard Blade DAMEUS** & **Berothely THELUS**

**Sous la supervision de :**  
    M. Wedter JEROME & M. Geovany LAGUERRE

<br/>

**Date de présentation :** Octobre 2025  
 
**Localisation :** Port-au-Prince, Haïti

</center>



## 🎯 Objectif du projet

Ce projet vise à concevoir un **modèle prédictif** capable d’anticiper le **niveau d’insécurité alimentaire** à l’échelle des départements haïtiens, tout en analysant l’influence des indicateurs économiques, climatiques et environnementaux sur ces niveaux.
À partir des données combinées, le modèle doit permettre de :
- Prévoir les phases IPC (1 à 5) associées à chaque département ou commune,
- Identifier les indicateurs clés (prix, pluviométrie, NDVI, taux de change, etc.) qui expliquent la dégradation ou l’amélioration des conditions alimentaires,
- Fournir un outil d’aide à la décision pour anticiper les crises et orienter les interventions préventives.



## 🧾 Résumé du travail

En Haïti, l’insécurité alimentaire persiste dans un contexte marqué par des crises climatiques, économiques et sécuritaires (les groupes armés en Haïti ont ravagé des champs agricoles et entravent l’accès à l’aide alimentaire dans le pays).
Pour y répondre, ce projet utilise la data science pour anticiper les risques à l’échelle communale. Il s’appuie sur des données du système Joint Monitoring Report (JMR) et du Integrated Food Security Phase Classification (IPC) pour construire un modèle supervisé capable d’identifier les zones à haut risque, contribuant ainsi à une meilleure planification humanitaire et agricole. 

Le projet vise à offrir un outil concret d’aide à la décision pour renforcer la résilience alimentaire et mieux orienter les interventions humanitaires en Haïti.


## 🧠 Méthodologie utilisée

Le projet repose sur la méthodologie **CRISP-DM**, reconnue pour sa rigueur et sa clarté dans la conduite des projets de *Data Science*.  
Cette approche couvre tout le processus analytique, depuis la compréhension du problème jusqu’à la restitution des résultats.



<center>
    <img src="CRISP-DM.png" alt="CRISP-DM Process" width="700"/>
    <br>
 
</center>



La carte suivante présente la structure administrative du territoire haïtien ainsi que le périmètre d’analyse retenu pour ce projet


<center>
    <img src="carte_Haiti.jpeg.jpg"
        " alt="Carte d'Haïti - Zones d'étude" width="700"/>
    <br>
    <em>Figure 1 — Carte d’Haïti : zones d’étude pour la prédiction du risque d’insécurité alimentaire.</em>
</center>

### **Mots-clés :**  
`Data Science` · `Machine Learning` · `Sécurité alimentaire` · `Haïti` · `CRISP-DM` · `Classification` · `Analyse prédictive`

# Partie 1 – Compréhension du domaine *(Business Understanding)*

## 🎯 Contexte et justification

Depuis plusieurs années, Haïti fait face à une **crise alimentaire profonde**.  
Les épisodes de sécheresse, les inondations répétées, la dégradation des sols, la hausse des prix des denrées et la baisse de la production locale se conjuguent à une **insécurité grandissante** dans plusieurs régions rurales.  

Les récents événements survenus dans la Plaine de l’Artibonite, le Bas-Sud et certaines zones du Nord-Est en sont une illustration :  
des **groupes armés ont incendié ou pillé des champs de riz, de maïs et de haricots**, détruisant plusieurs récoltes et forçant des familles à abandonner leurs terres.  
Ces attaques, relevées par le **Programme Alimentaire Mondial (PAM)**, aggravent une situation déjà fragile : près de **six millions de personnes** sont aujourd’hui exposées à un risque aigu d’insécurité alimentaire.  

Les conséquences ne sont pas uniquement économiques.  
La perte de moyens de subsistance, l’exode rural, la dépendance accrue à l’aide humanitaire et la hausse du coût de la vie créent un cercle vicieux qui érode les bases mêmes de la sécurité alimentaire nationale.  
Dans ce contexte, disposer d’un outil capable d’**anticiper les zones à haut risque** devient essentiel pour permettre aux décideurs de **planifier et cibler leurs interventions** avant que la crise ne s’installe.



Selon la capsule matinale de ProFin diffusée le 23 octobre 2025, la Communauté des Caraïbes (CARICOM) et l’Argentine ont entamé des discussions autour de nouveaux partenariats stratégiques en matière de sécurité alimentaire et d’opportunités de coopération agroalimentaire pour la région caribéenne. Ces échanges visent à renforcer les chaînes régionales de production et de distribution, avec des retombées économiques et agricoles potentielles pour Haïti, notamment à travers le développement de filières locales intégrées et la promotion d’une autosuffisance alimentaire durable.
Cette orientation régionale, axée sur l’autosuffisance alimentaire, s’accorde directement avec les ambitions de ce projet.  

Sur le plan national, plusieurs initiatives soutiennent déjà cette dynamique :  
- Le **Programme National de Cantines Scolaires (PNCS)**, appuyé par le **Programme Alimentaire Mondial**, achète chaque mois pour environ **1,7 million USD** de produits issus de la production locale.  
  Ce modèle, inspiré du *Home-Grown School Feeding*, relie écoles et agriculteurs tout en stimulant les économies rurales.  
- À l’occasion de la Journée internationale des femmes rurales, célébrée le 15 octobre 2025, le Ministère de l’Agriculture, des Ressources Naturelles et du Développement Rural (MARNDR), en collaboration avec la FAO rappelle que plus de 70% des agriculteurs en Haïti sont des femmes pourtant freinées par l’accès à la terre, au crédit et aux circuits formels.
  Renforcer leur participation est une condition incontournable pour restaurer la productivité et la résilience alimentaire du pays.  

Sur le plan international, ce projet s'inscrit dans les Objectifs de Développement Durable (ODD) des Nations Unies, en particulier les ODD 2 (Faim zéro) et ODD 13 (Lutte contre les changements climatiques), qui sont essentiels pour la durabilité et la résilience des systèmes alimentaires mondiaux. Le ODD 2, qui vise à éradiquer la faim et garantir la sécurité alimentaire pour tous, trouve une application directe dans notre projet, qui utilise la data science pour anticiper les risques alimentaires à travers la prédiction des crises alimentaires et l’identification des zones vulnérables en Haïti. En offrant un outil prédictif aux acteurs humanitaires et institutionnels, notre projet contribue à renforcer la planification préventive et à améliorer l'accès à la nourriture dans les zones les plus exposées.

De plus, l’ODD 13, qui appelle à la lutte contre les changements climatiques, est également au cœur de notre démarche. En utilisant des données climatiques telles que les précipitations, les températures, et les périodes de sécheresse, nous visons à renforcer la résilience climatique des communautés haïtiennes. Les effets du changement climatique, notamment les cyclones et les sécheresses prolongées, affectent gravement la production agricole et exacerbent l’insécurité alimentaire. En permettant une meilleure anticipation de ces événements grâce à des modèles prédictifs fiables, ce projet cherche à adopter des solutions d’adaptation pour atténuer les effets du changement climatique sur la sécurité alimentaire.

Ces initiatives montrent qu’il existe déjà un élan de transformation du système agricole haïtien.  
Le projet vient s’y inscrire en apportant une **dimension scientifique et prédictive**, permettant d’appuyer ces efforts par la donnée et l’analyse.

---

## 💡 Problématique 

> Comment anticiper les zones à haut risque d’insécurité alimentaire en Haïti à partir de données climatiques, géographiques et socio-économiques, afin d’aider les autorités et les partenaires à agir avant la crise ?

Cette question résume l’essence du projet : passer d’une **réaction tardive** à une **prévention éclairée par la donnée**.

---

## Hypothèse 
Les indicateurs climatiques (pluie, NDVI, sécheresse) et d’accessibilité influencent significativement le risque d’insécurité alimentaire.

---
## ⚙️ Objectifs spécifiques

1. **Identifier les facteurs déterminants** (pluviométrie, production agricole, variables climatiques, accès aux marchés, structure des ménages, etc.) liés à l’insécurité alimentaire.  
2. **Concevoir un modèle d’apprentissage supervisé** capable d’estimer la phase IPC de chaque commune à partir de données observées.  
3. **Évaluer les performances du modèle** à l’aide de métriques rigoureuses.
4. **Proposer un cadre analytique reproductible**, pouvant être utilisé par les institutions publiques et les ONG pour le suivi à long terme.

---

## 🧭 Vision du projet

Le projet vise à révolutionner la gestion de la sécurité alimentaire en Haïti en développant un modèle prédictif capable d’anticiper les crises alimentaires avant qu’elles n'atteignent des seuils critiques. En intégrant des données climatiques, économiques, sociales et sécuritaires, ce modèle permettra aux acteurs humanitaires et institutionnels de prendre des décisions proactives, optimisant ainsi les interventions et les ressources disponibles. Contrairement aux outils traditionnels comme l’IPC, qui se contentent d'une analyse descriptive de la situation actuelle, ce modèle se distingue par sa capacité à prédire l’évolution des phases de l'IPC en fonction de multiples facteurs locaux. Nous voulons renforcer la résilience des communautés haïtiennes en permettant une anticipation des crises alimentaires, ce qui permettra une gestion plus réactive et ciblée des ressources. Ainsi, le projet s’inscrit dans une vision à long terme, en offrant un outil flexible et dynamique qui soutient non seulement la gestion de la crise actuelle, mais aussi la préparation aux crises futures, tout en intégrant les spécificités de la réalité haïtienne.

---

<div style="text-align:center; font-weight:600; font-size:16px; margin-bottom:8px;">
  Acteurs clés du système alimentaire haïtien
</div>

| Catégorie                   | Acteurs principaux                                     | Rôle dans la sécurité alimentaire                                      |
|:--------------------------- |:------------------------------------------------------ |:------------------------------------------------------------------------|
| **Institutions nationales** | MARNDR, PNCS, CNSA                                     | Planification, coordination, achats locaux                              |
| **Organisations internationales** | FAO, PAM, CARICOM, WFP                          | Financement, assistance technique, distribution                         |
| **Producteurs ruraux**      | Coopératives agricoles, femmes agricultrices           | Production, transformation, résilience locale                           |
| **Collectivités locales**   | Mairies, CASEC, délégations départementales            | Gestion territoriale, identification des zones vulnérables              |
| **Communautés**             | Écoles, ménages, associations locales                  | Bénéficiaires directs, sensibilisation et participation communautaire   |

# Partie 2 – Compréhension des données *(Data Understanding)*

Cette phase vise à comprendre la nature, la structure et la signification des données disponibles avant toute modélisation.
Elle consiste à examiner leur origine, leur fiabilité, leur cohérence et leur potentiel d’analyse.
Dans le cadre de ce projet, 2 sources principales pour 3 datasets ont été exploitées :

1. Les données du Joint Food Security Monitor - Haiti de la part de la Banque Mondiale
    1. Les données du Joint Monitoring Report (JMR)
    2. Le référentiel géographique administratif (PCodes)   
2. Le jeu de données du système IPC (Integrated Food Security Phase Classification).

Ces trois jeux de données forment un socle d’analyse combinant la dimension temporelle, la dimension spatiale et la dimension structurelle de l’insécurité alimentaire en Haïti.


## 2.1 – Description des jeux de données

Trois sources principales ont été retenues :

### a) **HTI_JMR_data.csv**  
Ce jeu de données provient du **Joint Monitoring Report (JMR)**.  
Ce fichier contient des observations mensuelles de l’évolution des phases IPC par commune depuis 2010. Il contient près de 451 920 observations décrivant les valeurs de référence liées à la classification IPC au niveau communal (adm2_pcode). Il inclut des variables telles que :


| Variable | Description | Type |
|-----------|-------------|------|
| `iso3` | Code ISO du pays | Catégorielle |
| `ipc phase cutoff` | Niveau seuil IPC considéré | Numérique |
| `adm2_pcode` | Code administratif de la commune | Catégorielle |
| `year`, `month`, `date` | Variables temporelles | Temporelles |
| `indicator`, `grouping` | Type d’indicateur ou regroupement | Catégorielles |
| `value` | Valeur observée | Numérique |

Ce jeu de données offre une vue chronologique continue de la situation alimentaire à travers les communes haïtiennes.
Il permettra de suivre les évolutions dans le temps et d’extraire des tendances saisonnières ou structurelles.

### **HTI_JMR_pcodes.csv**  
Ce fichier fournit le référentiel géographique permettant d’associer chaque code à sa zone administrative.


| Variable | Description |
|-----------|--------------|
| `adm1_name` | Département |
| `adm2_name` | Commune |
| `adm2_pcode` | Code administratif |
| `country` | Nom du pays (Haïti) |

Ce fichier est essentiel pour lier les données JMR et IPC à leurs localisations géographiques.

### c) **ipc_hti_area_long_latest.csv** 
Ce dernier jeu de données regroupe les **résultats récents de l’analyse IPC (septembre 2025)**. Il décrit la population touchée par phase IPC.


| Variable | Description |
|-----------|-------------|
| `Date of analysis` | Mois et année de l’analyse |
| `Level 1` | Département |
| `Phase` | Niveau d’insécurité alimentaire (1 à 5) |
| `Number` | Population touchée |
| `Percentage` | Proportion dans la population totale |
| `From` / `To` | Période de validité de l’évaluation |


Nous avons regroupé les types d’informations suivies dans le système de surveillance alimentaire.  
Ces indicateurs traduisent la **réalité économique, climatique et environnementale** des communes haïtiennes.  
Ils constituent la base des observations utilisées par le système IPC pour évaluer le risque d’insécurité alimentaire.


# Phase 3 – Préparation des données (Data Preparation)


Cette phase marque le passage entre la compréhension des données et la construction du modèle. De ce fait, au cours de cette étape, on va essayer de rendre les données exploitables pour la modélisation.  
C’est ici que l’on va :
- Nettoyer et harmoniser les données issues des différentes sources,  
- Les fusionner pour former un jeu de données complet,  
- Explorer en profondeur les relations entre variables,   
- Identifier les **variables explicatives (features)** et la **variable cible (target)** avant la modélisation..

# Phase 4 — Modélisation (Modeling)

Cette phase vise à construire et à évaluer un **modèle prédictif supervisé**
permettant d’estimer la **phase d’insécurité alimentaire (IPC)** à partir des
indicateurs issus du *Joint Monitoring Report (JMR)*.

La démarche suit une approche scientifique en quatre étapes :
1. Séparation des données en features et target ;  
2. Division du jeu de données en ensembles d’entraînement et de test ;  
3. Construction, apprentissage et évaluation de plusieurs modèles ;
4. Sélection du modèle final et analyse de ses performances.


## 🧹 4.1 – Harmonisation et agrégation des doublons

Avant toute modélisation, il a été observé que certaines communes apparaissaient plusieurs fois
pour la même **date**, **phase**, **département** et **indicateurs**, ne différant que par la variable
**Population touchée**.

Pour garantir une cohérence territoriale et statistique :

- Les **indicateurs numériques** (GLM, NDVI, pluie, taux de change, prix) ont été agrégés par **moyenne** ;
- La **population touchée** a été agrégée par **somme**, représentant l’ensemble des personnes affectées dans la commune ;
- La **phase IPC** (1 à 5) a été conservée telle quelle.

Ainsi, chaque **commune-date-phase** devient une observation unique, propre à la modélisation.


# Phase 5 — Évaluation et validation du modèle

Dans cette phase, on a vérifier si le modèle qu'on a construit est réellement fiable pour anticiper le niveau d’insécurité alimentaire (Phase IPC) dans les départements et communes d’Haïti.

L’objectif n’est pas seulement d’avoir un bon score mathématique. L’objectif est de pouvoir répondre à une question opérationnelle très simple :

> Est-ce que nous pouvons utiliser ce modèle pour dire à une autorité (Agriculture, CNSA, PAM) :
> « Attention, telle commune risque de passer en phase critique » ?

Pour répondre sérieusement à cette question, on va :
1. mesurer la précision des prédictions,
2. vérifier que le modèle ne triche pas (surapprentissage),
3. étudier les erreurs de prédiction,
4. relier les résultats à la réalité du terrain (prix alimentaires, sécheresse, pluie).

La phase 5 n’est donc pas seulement technique. C’est la phase où on juge si le modèle peut vivre dans le monde réel.


## 5.1 Performance prédictive du modèle sur des données jamais vues

Dans cette section, on teste le modèle sur des données qu’il n’a pas vues pendant l’entraînement.  

On mesure trois choses :
- **MAE (Mean Absolute Error)** : l’erreur moyenne absolue entre la phase réelle et la phase prédite.
- **RMSE (Root Mean Squared Error)** : pénalise plus fort les grosses erreurs.
- **R²** : quelle part de la variation de la phase IPC est expliquée par nos indicateurs.

Plus MAE et RMSE sont bas, mieux c’est.  
Plus R² est haut, mieux c’est.

=== Évaluation du modèle sur le jeu de test ===
MAE :  0.0140
RMSE : 0.0249
R²   : 0.8201
Ce faible MAE veut dire que, en moyenne, le modèle ne se trompe pas beaucoup sur la phase IPC réelle de la commune.
Le R² de 0.82 signifie que nos indicateurs (prix alimentaires, taux de change, pluie, sécheresse NDVI...) expliquent déjà plus de 3/4 de la gravité alimentaire observée sur le terrain.
C’est un bon résultat solide pour un pays en crise multidimensionnelle.
En clair : le modèle est capable de donner un signal crédible d’alerte.

5.2 Visualisation directe : réalité vs prédiction
Un bon modèle ne doit pas être évalué uniquement par des chiffres.
Ici, on veux voir visuellement si les prédictions suivent bien la réalité.

On a fait deux vérifications :

Réalité vs Prédiction

Chaque point du graphe représente une commune sur une année donnée.
Vu que les points sont proches de la diagonale rouge (ligne parfaite), ça veut dire que le modèle colle à la réalité.
Analyse de l’erreur (résidus)

On regarde l’erreur IPC_réel - IPC_prédit.
On veut savoir : est-ce que le modèle sous-estime systématiquement certaines zones (par exemple zones rurales isolées) ?
Ou est-ce qu’il est équilibré ?

<center>
    <img src="CRISP-DM.png" alt="CRISP-DM Process" width="700"/>
    <br>
 
</center>

Il n'y a pas pas de biais global car la moyenne est proche de 0.
On peut remarquer que les valeurs min/max ne sont pas extrêmes car le modèle ne se trompe pas beaucoup.


5.3 Vérification du surapprentissage (overfitting)
On doit vérifier si le modèle est honnête.

Un modèle peut “tricher” : il peut apprendre par cœur les données historiques (train), avoir l’air parfait, mais devenir inutile dès qu’on lui donne une nouvelle période ou une nouvelle commune.

Pour vérifier ça :

on mesure l’erreur sur l’échantillon d’entraînement (données connues),
on mesure l’erreur sur l’échantillon de test (données jamais vues),
on compare.
Si l’erreur explose sur le test, c’est du surapprentissage.

Apres notre analyse, nous avons trouvé :

RMSE (train) : 0.023
RMSE (test)  : 0.0249
Ce qui signifie qu'il n'y a pas de signe majeur de surapprentissage : le modèle reste fiable sur de nouvelles communes/périodes.

5.4 Validation croisée
Maintenant on veut répondre à une question de confiance :
Est-ce que le modèle reste bon si on change légèrement les données d’entraînement ?
Ou bien est-ce qu’il est fragile, c’est-à-dire performant uniquement dans certains départements mais pas dans d’autres ?

Pour ça, on utilise la validation croisée (5-fold cross-validation) : on ré-entraine et réévalue le modèle plusieurs fois sur des sous-échantillons différents, puis on regarde la stabilité des scores R².
On a trouvé :
Scores R² par fold : [0.44168194 0.43545675 0.33603654 0.49627384 0.50207096]
R² moyen     : 0.4423
Écart-type   : 0.0597


### Validation croisée : stabilité du modèle

Le modèle a été soumis à une validation croisée à 5 plis afin de vérifier sa robustesse statistique.  
Les scores R² obtenus pour chaque pli sont les suivants :

| Fold | R² obtenu |
|------|------------|
| 1 | 0.4417 |
| 2 | 0.4355 |
| 3 | 0.3360 |
| 4 | 0.4963 |
| 5 | 0.5021 |

**R² moyen = 0.44 ± 0.06**

Ces résultats montrent que le modèle **explique environ 44 % de la variabilité de l’insécurité alimentaire (Phase IPC)** à partir des indicateurs climatiques et économiques retenus.  
L’écart-type faible (≈ 0.06) confirme la **stabilité du modèle** : les performances sont homogènes d’un échantillon à l’autre.

Alors, Le modèle présente une bonne performance moyenne et une bonne stabilité à travers les 5 plis de validation croisée.
Ces résultats traduisent une capacité du modèle à généraliser ses apprentissages sans dépendre d’un seul échantillon.
Dans le cadre du suivi IPC en Haïti, cela signifie qu’on peut utiliser ce modèle comme un outil de pré-alerte, tout en prévoyant d’y intégrer des variables additionnelles (marchés, sécurité, accessibilité) pour renforcer la précision future.


## 5.5 On peut se demander : Qu’est-ce qui explique vraiment l’insécurité alimentaire ?

On veut répondre honnêtement à la question suivante :

> “Pourquoi ce département est-il dans cette phase IPC ?”
> Est-ce à cause des prix des denrées ? du taux de change ? du manque de pluie ? de la dégradation des cultures ?

On extrait donc l’importance de chaque indicateur dans le modèle (basé ici sur la Random Forest).

<center>
    <img src="CRISP-DM.png" alt="CRISP-DM Process" width="700"/>
    <br>
 
</center>


Les résultats de l’analyse des importances des variables confirment les dynamiques connues de l’insécurité alimentaire en Haïti.  
Les **prix alimentaires** et les **conditions climatiques** (pluie, végétation) apparaissent comme les principaux moteurs de la dégradation des phases IPC.  
Les indicateurs socio-économiques (taux de change, modèle de subsistance) viennent renforcer cette lecture.

Ce qui nous permet de dire que :
- Une **hausse soudaine des prix alimentaires** ou une **sécheresse prolongée** conduit mécaniquement à une hausse des phases IPC dans les zones rurales.
- À l’inverse, une **stabilité monétaire** et une **bonne saison agricole** contribuent à la réduction du nombre de ménages en crise alimentaire.

En d'autres termes,
- Quand **les prix alimentaires (Food prices)** montent, l’IPC augmente. C’est cohérent : les ménages ne peuvent plus se nourrir correctement.  
- Quand **la pluviométrie en période de sécheresse (Drought rainfall)** est faible et que le **NDVI** baisse, l’agriculture locale souffre. Les ménages basculent plus vite dans l’insécurité alimentaire.  
- Quand **le taux de change (Exchange rates)** se dégrade, la nourriture importée devient trop chère : cela se reflète dans l’IPC.

Ces éléments confirment que le modèle peut servir à **anticiper les chocs** sur la sécurité alimentaire et orienter les **mesures préventives** (aides ciblées, planification logistique, appui aux agriculteurs).

## 5.6 Vue agrégée par département :
### Qui souffre le plus, et pourquoi ?

Ici on résume, par département, trois informations clés :
- la sévérité alimentaire (phase IPC moyenne),
- le prix des denrées,
- et la quantité de pluie disponible même en contexte de sécheresse.

L’objectif est de comprendre l'essence de cette question : “Quels départements combinent prix élevés et sécheresse ?”

<center>
    <img src="CRISP-DM.png" alt="CRISP-DM Process" width="700"/>
    <br>
 
</center>


<center>
    
### **Resultat de l'analyse** 
    
</center>

Ce graphique illustre la corrélation entre les prix alimentaires moyens, la quantité de pluie reçue en période de sécheresse et la sévérité moyenne de l’insécurité alimentaire (Phase IPC) dans les différents départements d’Haïti.
Chaque point (ou bulle) représente un département :

La taille de la bulle correspond à la pluviométrie moyenne (Drought rainfall),
la couleur indique le département,
et les axes traduisent la relation entre prix alimentaires (X) et phase IPC moyenne prédite (Y).
L’objectif est de comprendre comment les facteurs climatiques et économiques se combinent pour influencer l’insécurité alimentaire selon la réalité géographique et socio-économique du pays.

L’analyse du graphique corrélant le prix des aliments, le déficit pluviométrique et la sévérité de l’IPC révèle une dynamique complexe et différenciée selon les départements du pays. Dans les lignes suivantes, nous allons les présenter : 



#### **Sud-Est**

Le département du Sud-Est se trouve dans une situation particulièrement préoccupante sur le plan de la sécurité alimentaire. Les prévisions indiquent un indice IPC moyen de 3,14, le plus élevé du pays, traduisant un niveau de crise alimentaire aiguë dans de nombreux ménages. Les prix des produits y sont aussi parmi les plus chers du pays, en grande partie à cause de l'instabilité politique, de l'insécurité (qui perturbe les circuits d’approvisionnement), de l'inflation et de et la forte dépendance du pays vis-à-vis des importations alimentaires, comme le souligne la Banque mondiale. 
Même si la région enregistre un déficit pluviométrique modéré, l’économie locale, majoritairement agricole, demeure extrêmement vulnérable aux cyclones, sécheresses et glissements de terrain, ce qui limite la stabilité de la production. 

Les projections issues du modèle montrent que le Sud-Est risque de subir dans les prochains mois une pression croissante sur les prix alimentaires, amplifiée par une inflation généralisée et par la rareté des produits locaux. Ce département, en grande partie montagneux, souffre d’un manque d’eau, notamment à cause du risque de sécheresse et des effets du changement climatique.
Bien que le risque de pénurie soit encore classé comme modéré selon les estimations de Think Hazard, les tendances indiquent une aggravation progressive de la situation si aucune mesure d’adaptation n’est mise en œuvre.

Le relief accidenté du département complique davantage la situation. Les terres pentues et sujettes à l’érosion rendent difficile la pratique agricole durable, tandis que les petits exploitants manquent de moyens pour irriguer leurs cultures. Dans des communes comme Bainet, Belle-Anse ou Anse-à-Pitres, une seule saison sèche suffit à bouleverser la production, entraînant des hausses soudaines des prix sur les marchés. 

Face à cette situation, ce département a besoin d’un appui fort en matière de gestion de l’eau : la construction de bassins de rétention, le déploiement de systèmes de micro-irrigation, le reboisement des zones dégradées et la valorisation des marchés locaux afin que les produits agricoles ne se perdent pas avant d’arriver aux consommateurs.

---

#### **Centre**

Le département du Centre présente lui aussi un niveau préoccupant d’insécurité alimentaire, avec un indice IPC moyen de 3,00, indiquant que de nombreux ménages vivent une situation de crise alimentaire persistante. Les projections montrent un déficit pluviométrique modéré, ce qui constitue un facteur majeur de vulnérabilité pour une région dont l’économie repose essentiellement sur l’agriculture pluviale. C’est une région agricole importante mais très dépendante des précipitations. Les habitants de Hinche, Cerca-la-Source ou Thomonde le savent bien : quand la pluie tarde, les récoltes disparaissent, les rivières s’assèchent et les marchés deviennent presque vides.

Entre 2010 et 2025, la succession de périodes sèches a contribué à l’épuisement des terres et à la baisse de la productivité agricole, aggravant la dépendance du département aux produits importés. De plus, l’enclavement de certaines zones rurales, où les routes sont peu praticables ou inexistantes, rend la situation encore plus difficile, car le transport des denrées coûte cher, ce qui accentue la vulnérabilité des populations. 

Pour renforcer la sécurité alimentaire du Centre, il faudrait miser sur l’irrigation légère, la création de petites réserves d’eau communautaires et la formation des agriculteurs à des pratiques capables de conserver l’humidité du sol.

---

#### **Grand’Anse**

La Grand’Anse est un cas particulier. Les résultats du modèle prévisionnel révèlent un fort déficit pluviométrique, le plus élevé du pays, associé à un indice IPC moyen en phase de crise. Cela peut paraître surprenant, car c’est une région connue pour sa pluie abondante et ses terres fertiles. Toutefois, les dernières années ont profondément bouleversé cet équilibre : les saisons de pluie sont devenues irrégulières, alternant entre périodes de sécheresse prolongée et catastrophes naturelles dévastatrices.
Les ouragans Matthew (2016), Grace (2021) et même le cyclone le plus récent (Melissa en 2025) ont successivement frappé la région, provoquant des dégâts majeurs sur les plantations, les routes rurales et les infrastructures agricoles. Ces événements climatiques extrêmes ont non seulement détruit des milliers d’hectares de cultures, mais ont également rendu de nombreuses zones inaccessibles, isolant les producteurs et aggravant les pertes post-récolte. Les routes coupées empêchent l’acheminement des produits vers les marchés, et et les agriculteurs n’ont souvent aucun moyen de stockage, ce qui détériore rapidement les denrées périssables. 

Pourtant, la Grand’Anse demeure une région à fort potentiel agricole, connue pour la qualité de ses productions : café, cacao, igname, banane, fruits tropicaux qui pourraient jouer un rôle clé dans la relance économique et alimentaire du pays. Cependant, sans un réseau routier résilient, sans entrepôts modernes et sans système d’alerte efficace face aux chocs climatiques, cette production reste vulnérable et difficilement valorisable.

Les projections du modèle soulignent ainsi un profond dérèglement climatique qui menace la stabilité agricole du département. Pour inverser la tendance, il est essentiel de renforcer les infrastructures agricoles, de réhabiliter les routes d’accès, de développer des capacités locales de stockage et de transformation, et d’instaurer un système d’alerte rapide pour prévenir les pertes liées aux catastrophes naturelles.

---

#### **Nippes**

Le département des Nippes connaît une crise alimentaire silencieuse mais persistante, marquée par un indice IPC moyen en phase de crise et un déficit pluviométrique modéré. Bien que de petite taille, ce département joue un rôle important dans l’économie agricole du pays, mais il reste souvent négligé dans les grands programmes nationaux de développement. L’économie y repose principalement sur des petites exploitations familiales, très vulnérables aux aléas climatiques et aux crises successives. Les chocs climatiques des dernières années, notamment la sécheresse de 2019 et les perturbations consécutives au séisme de 2021, ont affaibli les capacités de production et d’autonomie alimentaire. Les ménages nippesois vendent souvent leur bétail ou leurs outils pour se procurer de la nourriture. Dans un contexte où le bétail représente à la fois un capital économique et une assurance de survie, cette pratique illustre la profondeur de la crise.
La dépendance aux importations dans certaines communes accentue la sensibilité aux fluctuations des prix mondiaux.

Pour enrayer cette spirale de précarité, les Nippes doivent bénéficier d’un plan intégré de sécurité alimentaire, combinant des actions à la fois écologiques, techniques et communautaires. Il s’agit notamment de promouvoir le reboisement productif pour restaurer les terres dégradées, de déployer des systèmes de micro-irrigation pour stabiliser la production en saison sèche, et de renforcer les coopératives locales afin d’améliorer la résilience collective. Ces interventions permettraient non seulement d’accroître la productivité agricole, mais aussi de favoriser une gestion durable des ressources naturelles et de redonner aux populations nippesoises la capacité de vivre dignement de leur travail.

---

#### **Nord-Est**

Le Nord-Est présente une situation alarmante sur le plan de la sécurité alimentaire. Les prévisions indiquent un indice IPC moyen en phase de crise, accompagné d’une hausse significative des prix alimentaires, parmi les plus élevés du pays. Ce département, historiquement agricole, subit aujourd’hui une pression croissante sur ses terres en raison d’un déficit pluviométrique persistant et de la réduction des surfaces cultivables, notamment après l’installation du Parc industriel de Caracol. Construit sur près de 246 hectares, ce complexe devait initialement offrir plus de 20 000 emplois lors de son inauguration en 2012, mais les résultats n’ont pas été à la hauteur des attentes. En réalité, la conversion des terres agricoles en zones industrielles a affaibli la production locale sans créer les débouchés économiques espérés, accentuant ainsi la dépendance aux importations alimentaires. 

Les données prévisionnelles montrent que cette combinaison de déficit de pluviométrie moyen, de manque d’irrigation et de faible diversification économique exerce une pression directe sur les ménages, en particulier dans les communes rurales de Vallières, Mont-Organisé et Carice, où le coût de la vie ne cesse d’augmenter. Les familles agricoles, déjà fragilisées par l’érosion et la rareté de l’eau, voient leurs revenus diminuer tandis que les produits de base deviennent inabordables. Dans ces conditions, l’insécurité alimentaire ne découle plus uniquement des aléas climatiques, mais également de choix structurels d’aménagement du territoire et d’une planification économique inachevée.

Pour inverser cette tendance, les projections recommandent un rééquilibrage entre développement industriel et sécurité alimentaire, en veillant à préserver les terres agricoles restantes et à moderniser les systèmes d’irrigation. L’installation de réseaux d’eau agricoles, le soutien à la petite production vivrière et la promotion des achats institutionnels (notamment pour les cantines scolaires et les programmes de nutrition communautaire) constitueraient des leviers essentiels pour revitaliser la production locale.

---


#### **Nord-Ouest**

Le Nord-Ouest demeure une région naturellement sèche, marquée par ses paysages arides, ses sols appauvris et la rareté de ses ressources en eau. Pourtant, selon les résultats du modèle, il apparaît comme la région présentant le plus faible déficit pluviométrique du pays. Ce résultat peut prêter à confusion : il ne signifie pas que le Nord-Ouest reçoit davantage de pluie que les autres départements, mais plutôt que les niveaux actuels de précipitation restent conformes à la moyenne historique d’une région déjà sèche. Autrement dit, le modèle met en lumière une stabilité dans la sécheresse : il pleut peu, certes, mais il ne pleut pas moins qu’avant.

Cette nuance est essentielle pour comprendre la dynamique climatique du Nord-Ouest. Elle illustre la distinction entre un climat structurellement sec et un déficit pluviométrique conjoncturel. Malgré cette apparente stabilité statistique, la situation humanitaire et économique du département demeure critique. L’IPC y atteint un niveau critique et, même si les prix moyens des produits alimentaires paraissent légèrement inférieurs à ceux d’autres régions, cette apparente stabilité masque une forte dépendance aux importations en provenance de Port-de-Paix, de Jean-Rabel et des départements voisins. 
La population vit souvent de petits commerces, d’activités artisanales ou de l’élevage, mais les sécheresses prolongées entraînent des pertes de bétail, une baisse du pouvoir d’achat et une insécurité alimentaire chronique.

Pour renforcer la résilience du Nord-Ouest, les recommandations issues des projections du modèle préconisent des solutions locales et accessibles. Il s’agit notamment de diversifier l’élevage, en misant sur des espèces plus résistantes comme les chèvres et moutons, de relancer la pêche artisanale le long des côtes, et surtout d’investir dans la gestion communautaire de l’eau à travers la construction de citernes, la récupération d’eau de pluie et la mise en place de bassins de rétention. Ces stratégies simples et accessibles peuvent améliorer durablement la sécurité alimentaire sans nécessiter de lourdes infrastructures.

---

#### **Artibonite**

L’Artibonite présente un tableau plus équilibré en termes de sécurité alimentaire, malgré une situation stressante marquée par un déficit de pluie faible, ce qui lui permet d’échapper aux effets dévastateurs des sécheresses prolongées. Elle est l’une des régions les plus résilientes du pays sur le plan agricole, grâce à sa plaine irriguée qui soutient la production de riz. 

Toutefois, malgré ces atouts, plusieurs facteurs externes viennent perturber sa stabilité. L’instabilité politique, qui affecte directement la route nationale #1, engendre des retards dans l’écoulement des produits et perturbe l’approvisionnement en intrants agricoles, notamment les engrais. De plus, l’impact des groupes armés, qui envahissent parfois les champs, met en péril la production locale en causant des incendies volontaires et en empêchant les paysans de travailler dans des conditions normales. 

Les sécheresses modérées des dernières années ont été relativement maîtrisées grâce à l’irrigation, mais la dépendance presque exclusive au riz rend la région vulnérable aux chocs extérieurs.

Pour assurer la durabilité de son système de production, plusieurs mesures doivent être prises. Tout d’abord, il est essentiel de moderniser les infrastructures d’irrigation pour garantir une production stable, surtout dans un contexte de variabilité climatique. 
Ensuite, la diversification des cultures doivent être encouragée pour éviter la dépendance excessive au riz et offrir aux agriculteurs des alternatives économiques. 

Une autre priorité est la création de petites unités de transformation, permettant de réduire les pertes après récolte, tout en générant des emplois et en favorisant la valorisation des produits agricoles.
Cependant, les autorités locales doivent mettent en place des politiques qui facilitent la sécurisation des routes, la libre circulation des producteurs, et la protection des zones agricoles contre les menaces sécuritaires, afin d’assurer un environnement propice à la production et à l’approvisionnement.

---

#### **Sud** 

La situation du département du Sud se révèle être préoccupante malgré un déficit pluviométrique moyen, ce qui peut surprendre étant donné que la région est fréquemment frappée par des inondations dévastatrices. En effet, le Sud est l’une des régions les moins exposées à un IPC élevé, mais cela ne signifie pas qu’il est exempt de risques. Ce département présente un potentiel agricole important, avec des terres fertiles et un climat généralement favorable, mais il est régulièrement victime de catastrophes naturelles, telles que des séismes, des ouragans et des inondations qui ont, au fil des années, détruit des milliers d’hectares cultivables.

Malgré la présence de zones productives comme Torbeck et Camp-Perrin, de nombreux paysans peinent à réhabiliter leurs terres après chaque catastrophe, faute de moyens financiers et techniques. Cette situation contribue à une insécurité alimentaire persistante et à une dépendance accrue à l’aide extérieure. Pour pallier cette vulnérabilité, il est essentiel de concentrer les efforts sur la réhabilitation des canaux d’irrigation, sur la relance des coopératives agricoles et sur l’intégration de technologies de stockage modernes afin de préserver les récoltes et d’éviter les pertes post-récolte.

Le Sud constitue une zone stratégique pour la relance agricole durable. Cependant, pour que cette relance soit pérenne, l’État doit absolument sécuriser les infrastructures rurales et mettre en place des mesures de résilience face aux crises récurrentes. Si ces actions sont menées efficacement, le Sud pourrait jouer un rôle majeur dans la sécurisation alimentaire à l’échelle nationale.

---

#### **Nord**

Le Nord est le deuxième département du pays à afficher une situation de sécurité alimentaire relativement moins préoccupante, bien qu’il présente des prix alimentaires élevés et un déficit pluviométrique moyen. La région reste vulnérable, mais bénéficie d’un certain équilibre alimentaire, en grande partie grâce à Cap-Haïtien, qui sert de hub commercial facilitant les échanges et l’approvisionnement. Cependant, les zones rurales, notamment Borgne et Bahon, rencontrent des difficultés agricoles importantes dues à la sécheresse récurrente et au manque d’irrigation, ce qui limite le potentiel de production locale. Bien que la région possède un fort potentiel agricole, l’absence de modernisation des pratiques entrave son plein développement.

Ce relatif équilibre alimentaire n’est pas uniquement dû à l’agriculture, mais découle également des dynamismes économiques locaux. En effet, les mouvements migratoires, notamment l’afflux de personnes fuyant l’insécurité à Port-au-Prince, ont eu un impact direct sur l’économie de la région. En se dirigeant vers Cap-Haïtien, ces déplacements massifs ont permis d’augmenter les flux financiers, ce qui a réduit l’IPC et amélioré l’accessibilité alimentaire pour la population locale.

Cependant, cette dynamique pourrait être remise en question. L’insécurité à Port-au-Prince continue de forcer des milliers de personnes à migrer vers le Nord, principalement vers Cap-Haïtien. Cette croissance rapide de la population pourrait engendrer plusieurs problèmes économiques pour la région : augmentation de la demande pour les biens de consommation, hausse des prix, et déséquilibre de la répartition des produits alimentaires sur le marché. En effet, un trop grand nombre de nouveaux arrivants pourrait créer une pénurie de produits alimentaires, augmentant les tensions sociales et économiques dans la région.

Pour maintenir cette dynamique économique positive, il est impératif que des politiques adaptées soient mises en place. Ces politiques devraient viser à soutenir les activités économiques locales tout en favorisant une gestion durable des ressources agricoles. L’amélioration des infrastructures de stockage et de transport est également essentielle pour éviter les pertes après récolte et garantir une distribution efficace des produits. Sans ces mesures, la vulnérabilité alimentaire de la région pourrait être exacerbée par l’inflation et les déplacements massifs, mettant en péril l’équilibre alimentaire et la stabilité économique du Nord.

---

#### **Ouest**

Le département de l’Ouest est aujourd’hui le mieux placé du pays en matière de sécurité alimentaire. Selon les résultats du modèle, il présente la plus faible valeur de l’IPC, ce qui en fait le département le moins exposé à une crise d’insécurité alimentaire. Cette situation s’explique en partie par le fait que Port-au-Prince, capitale du pays et centre économique national, concentre la majorité des échanges commerciaux et reçoit l’essentiel des produits agricoles en provenance des autres départements. Cette concentration d’approvisionnements fait que les prix moyens des denrées y sont plus bas que dans les régions rurales éloignées, ce qui limite temporairement l’exposition de la population urbaine à une crise alimentaire aiguë.

Cependant, derrière cette apparente stabilité se cachent des fragilités structurelles profondes. L’Ouest est aujourd’hui le département le plus affecté par l’insécurité, notamment à cause de la présence de gangs armés qui contrôlent de vastes portions du territoire, y compris les principales voies d’accès vers la capitale. Ces groupes imposent des taxes illégales aux transporteurs et aux producteurs, perturbant ainsi la libre circulation des marchandises. De nombreux paysans et commerçants hésitent désormais à se rendre à Port-au-Prince, ce qui ralentit les flux d’approvisionnement et fait peser un risque croissant de pénurie sur les marchés urbains.

De plus, plusieurs zones autrefois productives, comme Kenscoff, Fermathe ou Pétion-Ville, sont aujourd’hui menacées par l’urbanisation anarchique, les conflits armés et la dégradation des terres. Certaines portions agricoles ont été abandonnées, d’autres sont devenues improductives à cause de la pollution chimique liée à des affrontements armés ou à des incendies volontaires. 
L’Ouest, autrefois considéré comme le grenier urbain du pays, connaît désormais une réduction drastique de ses surfaces cultivables et un affaiblissement des filières locales.

Par ailleurs, même si le déficit pluviométrique du département demeure faible, certaines zones rurales de montagne connaissent des périodes de sécheresse prolongée et un manque d’eau potable, aggravant la vulnérabilité des familles les plus pauvres.
Dans les quartiers populaires de Port-au-Prince, l’inflation et le chômage massif accentuent la dépendance aux produits importés.

Pour préserver sa position privilégiée, l’Ouest doit repenser sa gouvernance alimentaire. Il faut encourager la production de proximité, promouvoir des marchés de quartier sécurisés, développer des jardins urbains communautaires, et renforcer la logistique de transport local. L’État devrait également réhabiliter les zones agricoles endommagées, sécuriser les routes d’accès, et soutenir les producteurs locaux à travers des programmes d’incitation et de microfinancement. En renforçant la sécurité logistique et alimentaire, tout en encourageant la résilience urbaine, l’Ouest pourrait non seulement consolider sa position de département le plus stable, mais aussi redevenir le cœur productif et nourricier d’Haïti, capable de soutenir les autres régions en période de crise.


---

En résumé, le graphique met en évidence la **complexité systémique de l’insécurité alimentaire haïtienne** :  
elle résulte d’un enchevêtrement entre climat, économie et gouvernance.  
Les modèles prédictifs montrent que **les politiques d’adaptation ne peuvent pas être seulement agricoles** : elles doivent aussi inclure la **sécurisation des routes**, la **régulation des prix**, la **dépendance aux importations** et l’**investissement dans l’irrigation rurale**.


*Le modèle raconte la géographie de la faim : là où la route, la pluie ou le prix vacillent, la sécurité alimentaire s’effondre.*

# Phase 6 — Déploiement 

Cette phase vise à **transformer les résultats analytiques et prédictifs** obtenus dans les étapes précédentes en **instruments concrets d’aide à la décision**.    
Dans le contexte haïtien, cela signifie utiliser le modèle pour **anticiper les crises alimentaires**, orienter les **interventions humanitaires**, et soutenir la **planification gouvernementale** en matière de sécurité alimentaire.

Le modèle développé fournit un cadre d’analyse basé sur les indicateurs climatiques, économiques et géographiques, permettant d’identifier les **zones à haut risque** avant qu’une crise ne s’installe.

---

## 6.1 Interprétation  du modèle

Les résultats du modèle ont mis en évidence les relations suivantes :

- Les **prix alimentaires** sont le **facteur le plus influent** dans la dégradation des phases IPC.  
- Les **indicateurs climatiques** (pluviométrie, NDVI) influencent directement la disponibilité agricole.  
- Le **taux de change** amplifie les vulnérabilités économiques et affecte le coût de la vie.  
- Le modèle a atteint une **performance moyenne (R² ≈ 0.44)** avec une **stabilité inter-fold solide (± 0.06)**, traduisant une capacité de généralisation satisfaisante.

Ces résultats confirment que l’insécurité alimentaire en Haïti n’est pas liée à un seul facteur :  
elle est **le produit de la convergence** entre **chocs économiques, instabilité climatique et contraintes logistiques**.

---

## 6.2 Déploiement technique du modèle

### Objectif technique

Le modèle peut être intégré dans un système de suivi dynamique :
- Actualisation mensuelle des données (prix, précipitations, NDVI) ;  
- Prédiction automatique de la **phase IPC probable** par commune ou par département.


## 6.3 Application terrain et système d’alerte précoce

Le modèle final peut être intégré dans un système national de suivi et d’alerte précoce (Early Warning System).
L’objectif est de détecter rapidement les signaux d’aggravation de l’insécurité alimentaire et de déclencher une réponse rapide avant la crise.
Les résultats de la modélisation peuvent alimenter un système d’alerte précoce (EWS) destiné à :
- Identifier les communes les plus vulnérables ;
- Détecter rapidement les variations anormales des prix et de la pluviométrie ;
- Mobiliser les stocks alimentaires régionaux et planifier les convois humanitaires avant la détérioration de la situation par les institutions;
- Informer la priorisation des ressources pour les programmes du PAM et du MARNDR.

Par exemple :

Si le modèle prédit une hausse de l’IPC en Grand’Anse ou dans le Sud à la suite d’événements climatiques comme le cyclone Melissa, les acteurs peuvent activer immédiatement les stocks régionaux ou rediriger les convois humanitaires avant l’aggravation de la crise.

---

##  6.4 Plan de déploiement institutionnel

Le modèle prédictif développé dans ce projet n’a de véritable valeur que s’il peut être **mis au service des acteurs publics, humanitaires et territoriaux** qui œuvrent à la réduction de l’insécurité alimentaire en Haïti.  
L’objectif de cette section est donc de proposer un **plan de déploiement institutionnel réaliste et durable**, permettant de transformer les résultats du modèle en **outil opérationnel d’aide à la décision**.

---

### Objectif du déploiement

Mettre à la disposition du **Gouvernement haïtien**, du **CNSA (Coordination Nationale de la Sécurité Alimentaire)**, du **PAM**, de la **FAO**, et du **MARNDR** un système d’analyse et de prévision permettant :
- d’**identifier les communes à risque élevé** d’insécurité alimentaire avant la crise,  
- de **déclencher des alertes précoces**,  
- et de **planifier les interventions logistiques et humanitaires** de manière plus efficace.

---

### Structure institutionnelle proposée

Le déploiement du modèle repose sur une **collaboration interinstitutionnelle** organisée autour de trois niveaux de gouvernance :

| Niveau | Institution clé | Responsabilités principales |
|--------|------------------|-----------------------------|
| **1. Politique et stratégique** | **Primature & MARNDR** | Pilotage général, intégration dans la stratégie nationale de résilience alimentaire. |
| **2. Technique et analytique** | **CNSA, FAO, PAM, OCHA** | Gestion des données, mise à jour du modèle, suivi mensuel des prévisions IPC. |
| **3. Opérationnel et territorial** | **DAE, Bureaux départementaux de l’agriculture** | Collecte de données locales, validation terrain, communication des alertes. |

Cette architecture garantit un **partage clair des rôles** entre les acteurs décisionnels, techniques et locaux, assurant la durabilité du système.

---

### Approche technologique et déploiement

Le modèle peut être déployé sous forme d’un **tableau de bord interactif** ou d’une **application légère** accessible via un portail web institutionnel.  
L’idée est de créer un outil intuitif et accessible même dans des environnements à faible connectivité.

#### 🔹 Étapes de déploiement :
1. **Automatisation des mises à jour de données** à partir des sources existantes (CNSA, FAO, Météo Haïti).  
2. **Hébergement du modèle** sur un serveur institutionnel (ou cloud sécurisé — par exemple Google Cloud ou AWS, en partenariat FAO-PAM).  
3. **Création d’un tableau de bord (Dashboard)** avec des indicateurs interactifs :  
   - Cartes de risques (phases IPC par commune).  
   - Courbes de tendance par indicateur (prix, pluviométrie, NDVI).  
   - Alertes dynamiques lorsque les seuils critiques sont atteints.  
4. **Formation des cadres techniques** (CNSA, MARNDR, FAO) à l’interprétation et à la maintenance du modèle.  
5. **Validation annuelle** des performances du modèle à partir des nouvelles données de terrain.


---

### Intégration dans les cadres internationaux

Le modèle pourrait être intégré dans le **Cadre Harmonisé d’Analyse de la Sécurité Alimentaire (CH)** utilisé par la FAO et le PAM pour la classification IPC.  
Cela permettrait à Haïti :
- de **renforcer la crédibilité internationale** de ses données,  
- d’**accéder plus rapidement aux financements humanitaires**,  
- et de **synchroniser ses rapports** avec les pays voisins de la région caraïbe.


---


Le plan de déploiement institutionnel s’inscrit dans une vision à long terme :  
faire de la **data science un pilier de la politique alimentaire et climatique d’Haïti**.  
En reliant la technologie aux institutions, le modèle devient un outil de gouvernance moderne, capable de **transformer la prévision en action, et la donnée en décision.**

> *Ce projet marque un pas décisif vers une gestion intelligente des risques alimentaires en Haïti : une approche où chaque donnée devient un signal d’alerte, et chaque prévision, une opportunité d’agir avant la crise.*

---


# Recommandations stratégiques


### 1️⃣ Pour les institutions publiques (CNSA, MARNDR)

- Créer un Observatoire national de la sécurité alimentaire prédictive basé sur ce modèle ;
- Intégrer la prévision IPC dans les politiques agricoles et de résilience ;
- Renforcer la collecte de données locales (prix, production, accès routier, pluviométrie) ;
- Utiliser les prédictions pour cibler les subventions agricoles ou les programmes de soutien aux ménages.

### 2️⃣ Pour les acteurs humanitaires (PAM, FAO, ONG)
 
- Utiliser le modèle comme outil d’aide à la planification géographique des interventions ;
- Déployer les aides en fonction du niveau de risque prédictif ;
- Développer des protocoles d’action rapide déclenchés automatiquement par les signaux du modèle;
- Croiser les prévisions avec les rapports de terrain pour affiner la réponse humanitaire.

### 3️⃣ Pour la communauté scientifique

- Étendre le modèle avec de nouvelles variables : accès à l’eau, mobilité, sécurité, état des infrastructures ;
- Promouvoir la collaboration entre chercheurs, ingénieurs et acteurs du terrain pour affiner les modèles prédictifs ;
- Promouvoir des programmes de formation en Data Science appliquée au développement durable.


# Perspectives d’amélioration

- Intégration de données satellitaires haute résolution (MODIS, Sentinel) pour affiner les prévisions climatiques ;

- Utilisation de modèles plus avancés (XGBoost, LSTM, Random Forest Optimized) pour améliorer la précision ;

- Couplage avec des modèles socio-économiques pour simuler l’impact des politiques publiques (subventions, importations, aides).

---

# Conclusion

Le projet "Prédiction de risque d'insécurité alimentaire en Haïti" a permis d'explorer la complexité des défis alimentaires auxquels le pays est confronté. Cette étude avait pour but d’apporter une compréhension claire et prédictive du phénomène de l’insécurité alimentaire en Haïti, à travers une approche rigoureuse de modélisation fondée sur les données climatiques, économiques et géographiques. Dès le départ, la démarche s’est appuyée sur une problématique essentielle : Comment anticiper les zones à haut risque d’insécurité alimentaire en Haïti à partir de données climatiques, géographiques et socio-économiques, afin d’aider les autorités et les partenaires à agir avant la crise ? C’est autour de cette question centrale que le projet a pris forme, en s’inscrivant dans une logique d’analyse scientifique mais aussi d’utilité publique.

Le travail a consisté à mobiliser, harmoniser et traiter plusieurs jeux de données issus du *Joint Monitoring Report (JMR)* et de diverses sources complémentaires. Après un long processus de nettoyage, de transformation et d’agrégation, un modèle prédictif supervisé a été construit afin d’estimer la **phase IPC**, indicateur clé de l’insécurité alimentaire, à partir d’un ensemble de variables indépendantes telles que la pluviométrie (Drought Rainfall), l’indice de végétation (NDVI), le taux de change, les prix alimentaires, GLM. Ce modèle, entraîné sur plus de deux mille observations réparties par commune et par année, a permis d’identifier les relations profondes entre le climat, les prix et la vulnérabilité sociale des territoires.

Les résultats ont révélé que **les prix alimentaires constitue le déterminant majeur de la variation de l’IPC. Autrement dit, plus les prix augmentent, plus la probabilité d’entrer dans une phase d’insécurité sévère est élevée. 

Les résultats montrent que, bien que certaines régions comme l’Artibonite, le Nord et l’Ouest bénéficient d’une plus grande résilience grâce à des infrastructures d’irrigation et un meilleur accès aux marchés, la majorité des départements reste profondément vulnérable aux effets du changement climatique, des variations de prix et des catastrophes naturelles. En particulier, des départements tels que le Sud-Est, le Centre, le Sud et les Nippes présentent des indices de vulnérabilité élevés, avec un déficit pluviométrique marqué et une forte dépendance à l’agriculture pluviale, ce qui accroît la précarité des habitants.

Au-delà des chiffres, ce travail met en évidence une vérité fondamentale : **l’insécurité alimentaire haïtienne n’est pas qu’un phénomène naturel, mais un phénomène systémique et multidimensionnel.** Elle résulte d’une interaction entre la pluviométrie, la gouvernance, les prix, la mobilité et la stabilité sociale. Dans certains cas, les aléas climatiques ne font qu’exacerber des fragilités déjà existantes ; dans d’autres, ce sont les tensions économiques et les violences humaines qui amplifient les effets de la nature. Le modèle développé dans ce projet a donc servi non seulement à prévoir, mais aussi à comprendre : comprendre comment le manque d’eau ou l’excès de pluie se traduit en souffrance humaine, comment un prix du maïs qui double dans un marché isolé peut devenir un facteur de famine, ou comment la fermeture d’une route par un groupe armé peut interrompre toute la chaîne alimentaire d’un département entier.

Sur le plan méthodologique, l’approche a démontré la pertinence de la **modélisation supervisée** (Random Forest et régression multiple) pour des problématiques sociales complexes. Le modèle le plus performant, avec un coefficient R² moyen avoisinant **0,44**, explique près de la moitié des variations observées de la phase IPC, tout en conservant une bonne stabilité sur les tests croisés. Ces résultats, bien qu’imparfaits, traduisent une performance réaliste pour un domaine aussi fluctuant et hétérogène que la sécurité alimentaire, où la donnée reste souvent lacunaire et irrégulière.

D’un point de vue stratégique, ce projet ouvre la voie à une utilisation concrète de la data science au service des politiques publiques. En intégrant les prédictions du modèle dans les systèmes d’alerte précoce, il devient possible d’anticiper, département par département, les risques de détérioration de la situation alimentaire. Il ouvre la voie à des politiques publiques plus ciblées et à des initiatives communautaires qui doivent être soutenues par des acteurs nationaux et internationaux. Les résultats de ce projet, s’ils sont pris en compte dans l’élaboration des stratégies de sécurité alimentaire, peuvent offrir un outil précieux pour aider le pays à renforcer sa résilience et à lutter contre l’insécurité alimentaire de manière durable.

Il a mis en lumière l'importance de ne pas se limiter à des analyses statistiques de surface. L’interprétation des données doit toujours prendre en compte les réalités locales, telles que l’infrastructure insuffisante, l’accès limité à l’eau et la fragilité du système de production agricole. Ainsi, une approche locale et intégrée de la gestion de la sécurité alimentaire est indispensable. Des actions telles que la gestion durable de l’eau, le renforcement des systèmes d’irrigation, la diversification des productions agricoles, et l'amélioration de l’accès aux marchés sont cruciales pour augmenter la résilience des communautés face aux crises alimentaires.

Le modèle prédictif développé dans ce projet, bien qu’il fournisse des indications précieuses sur les risques d’insécurité alimentaire, met aussi en évidence le besoin de solutions pragmatiques et adaptatives en fonction des spécificités de chaque région. En intégrant des solutions basées sur les ressources locales, comme l’agropastoralisme dans le Nord-Ouest ou la gestion des ressources hydriques dans le Sud-Est, Haïti pourrait réduire sa vulnérabilité face aux aléas climatiques et économiques.

En conclusion, ce projet a permis de répondre à la problématique initiale en prouvant qu’il est possible de **prédire la phase d’insécurité alimentaire** à partir d’indicateurs combinant économie, climat et territoire. Il a montré que la faim n’est pas un mystère mais un signal mesurable, que la donnée peut capter et interpréter. L’objectif de construction d’un outil d’aide à la décision a été atteint : le modèle développé constitue une base solide pour des projections futures, tout en offrant une grille d’analyse pour la compréhension des déséquilibres régionaux. Il s’agit là d’une étape vers une gouvernance plus anticipative, où la donnée devient un levier d’équité et de prévention.

Cette recherche a voulu démontrer que la science des données, lorsqu’elle est utilisée avec rigueur et conscience, peut devenir un instrument de résilience nationale. Dans le contexte haïtien, chaque ligne de code, chaque variable nettoyée, chaque corrélation identifiée représente une tentative de rendre le pays un peu plus prévisible, un peu plus stable, et un peu plus capable de se défendre contre l’invisible : la faim.


# Remerciements 



Nous tenons à exprimer nos profondes gratitudes envers toutes les personnes et institutions qui ont contribué, directement ou indirectement, à la réalisation de ce projet.

- À **l’équipe pédagogique d’Akademi (powered by Flatiron School)**, pour l’encadrement rigoureux et la vision pratique qu’elle apporte à la science des données.  
- À Mme Castelline, pour cette formation enrichissante.
- À nos **superviseurs, M. Wedter et M. Geovany**, pour leur accompagnement méthodologique, leurs conseils techniques et leur exigence de qualité.   
- Enfin, à toutes les **institutions haïtiennes** (CNSA, FAO, MARNDR, PAM) dont les données et les rapports de terrain ont nourri la réflexion scientifique et opérationnelle.

---



Ce projet nous a permis de dépasser la simple approche académique pour comprendre la **valeur stratégique de la donnée dans les décisions publiques**.  
Il nous a appris qu’un modèle prédictif n’a de sens que s’il **améliore concrètement la vie des gens**.

En travaillant sur la prédiction du risque d’insécurité alimentaire en Haïti, nous avons compris que la Data Science n’est pas seulement une discipline mathématique :  
c’est un **langage de compréhension du monde**, un outil d’action face à des défis réels – la faim, la pauvreté, les catastrophes naturelles.

---


Au terme de cette soutenance, ce projet n’est pas une fin, mais un point de départ.  
Il ouvre la voie vers une **nouvelle manière de penser la planification et la prévention en Haïti** — fondée sur la donnée, la science et la responsabilité collective.

> *“Les chiffres ne mentent pas, mais c’est à nous de leur donner un sens.”*  


<center>

### **Fin du projet Capstone : Prédiction du risque d’insécurité alimentaire en Haïti**


</center>    

<center>

### **Merci pour votre attention**

</center>



