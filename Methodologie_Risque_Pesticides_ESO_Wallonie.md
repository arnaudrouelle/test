# Méthodologie — Évaluation du risque pesticides dans les zones de surveillance des captages d'eau souterraine wallons

**Contexte** : Région wallonne — Troisièmes Plans de Gestion des Districts Hydrographiques (PGDH3, cycle 2022-2027)  
**Cadre réglementaire** : Directive Cadre sur l'Eau 2000/60/CE, Directive 2006/118/CE, Code de l'Eau wallon  
**Sources** : DossierCRAW_2304 (PRIOR'eau), Article INDIC'eau (CRA-W), PGDH3 et ses Annexes (SPW/DEE)

---

## Périmètre et logique générale

**Périmètre** : eaux souterraines (ESO) uniquement.  
**Zones d'analyse** : zones de surveillance des captages d'eau potable = ZAC (Zone à Alimentation de Captage) + zones de protection réglementaires (zones 1, 2a, 2b, 3 — codes `AC_XXX`, Annexe 5 PGDH3).

**Logique en 3 étapes enchaînées :**

```
ÉTAPE 1                    ÉTAPE 2                        ÉTAPE 3
Quelles cultures       →   Ces cultures sont-elles    →   Le sous-sol amplifie-t-il
utilisent les PPP          présentes dans la ZAC ?        le risque ?
les plus lixiviables ?                                    (karst, nappe libre)
```

Le résultat final est une **carte de risque intégré par ZAC**, permettant de prioriser les actions de terrain des conseillers PROTECT'eau.

---

## ÉTAPE 1 — Classer les cultures par risque de lixiviation vers les ESO

### 1.1 Les substances actives de référence

La liste de travail est celle des **21 substances actives préoccupantes INDIC'eau** (CRA-W / PROTECT'eau / SPW), comprenant 20 herbicides et 1 insecticide, établie sur base des détections dans le réseau de surveillance wallon (DCE — 550 ouvrages, base Calypso) et en concertation avec le SPW et le SPF.

**Norme de référence ESO** : 0,1 µg/L par substance active ou métabolite pertinent ; 0,5 µg/L pour la somme (Directive 2006/118/CE).  
**Seuil d'alerte précoce PRIOR'eau** : 30–75 ng/L (30–75 % de la norme), pour agir avant déclassement.

### 1.2 Indices de lixiviation utilisés

Le DossierCRAW_2304 (Tableau 2) recense 6 indices de lixiviation. Deux sont retenus comme complémentaires :

**GUS — Groundwater Ubiquity Score** (Gustafson, 1989) :
```
GUS = log10(DT50) × [4 - log10(Kfoc)]

Seuils :  GUS > 2,8  →  substance lixiviable
          GUS 1,8–2,8 →  zone de transition
          GUS < 1,8  →  substance non lixiviable
```

**Indice de lixiviation CRA-W** (M.LEACH modifié, Durenne et al., 2022) :
```
Indice CRA-W = log10[(Sw × DT50) / Kfoc] + 10

Échelle : 0 à ~20  (plus l'indice est élevé, plus la substance est lixiviable)
```
Avantage du M.LEACH par rapport au GUS : intègre la **solubilité (Sw)**, paramètre déterminant pour la lixiviation.  
Les paramètres DT50 sont issus des dossiers EFSA filtrés sur les conditions pédoclimatiques wallonnes (essais d'Europe du Nord-Ouest exclusivement).

### 1.3 Classement des 21 substances par potentiel de lixiviation ESO

*(Source : Tableau 4, DossierCRAW_2304 — Bergiers et al., 2023)*

| Substance active | Culture principale | GUS | Indice CRA-W | Niveau de risque ESO |
|---|---|:---:|:---:|---|
| MECOPROP-P | Céréales | 2,69 | **15,08** | Très élevé |
| MCPA | Céréales | 2,94 | **13,98** | Très élevé |
| 2,4-D | Céréales | 1,49 | **13,34** | Très élevé |
| BENTAZONE | Pois / haricots | 1,69 | **13,04** | Très élevé |
| METRIBUZINE | Pommes de terre | 2,57 | 12,50 | Élevé |
| METAMITRONE | Betterave | 2,00 | 12,21 | Élevé |
| S-METOLACHLORE | Maïs | 2,24 | 11,70 | Élevé |
| METAZACHLORE | Colza | 1,82 | 11,54 | Élevé |
| GLYPHOSATE | Toutes cultures | -0,31 | 11,49 | Élevé (volumes importants) |
| METOBROMURON | Pommes de terre | 2,01 | 11,43 | Élevé |
| CHLORIDAZON (\*) | Betterave | 1,82 | 11,39 | Élevé |
| DIMETHENAMIDE-P | Betterave | 1,04 | 11,32 | Élevé |
| ETHOFUMESATE | Betterave | 3,07 | 11,22 | Élevé (GUS > 2,8) |
| CHLORTOLURON | Céréales | **2,83** | 11,24 | Élevé (GUS > 2,8) |
| FLUFENACET | Céréales | 2,45 | 10,89 | Modéré-élevé |
| TERBUTHYLAZINE | Maïs | 2,11 | 9,75 | Modéré |
| LENACILE | Betterave | 2,58 | 9,72 | Modéré (GUS > 2,8) |
| PROSULFOCARBE | Pommes de terre | 0,78 | 8,89 | Faible-modéré |
| ACLONIFEN | Pommes de terre | 0,29 | 8,27 | Faible-modéré |
| DIFLUFENICAN | Céréales | 1,07 | 7,45 | Faible |
| PENDIMETHALINE | Céréales | -0,26 | 7,21 | Faible |
| BIFENOX | Céréales | 0,19 | 6,42 | Faible (risque ESU) |
| CYPERMETHRINE | Céréales / Colza | -1,42 | 3,77 | Très faible (risque ESU) |

*(\*) Substance interdite mais encore détectée en raison de sa persistance dans les nappes.*

> **Point d'attention PGDH3** : certaines substances interdites (atrazine/déséthylatrazine, BAM/dichlobénil, bromacile, simazine, diuron) sont toujours détectées dans les ESO wallonnes en raison de leur mobilité et persistance. Elles doivent être intégrées à l'analyse même si elles ne figurent plus dans la liste INDIC'eau active.

### 1.4 Cultures les plus problématiques pour les ESO

| Culture | Substances à risque ESO (indice CRA-W) | Quantité épandue (kg/ha) |
|---|---|---|
| **Céréales** | MCPA (13,98) + 2,4-D (13,34) + CHLORTOLURON (11,24) + FLUFENACET (10,89) | Modérée |
| **Betterave sucrière** | METAMITRONE (12,21) + DIMETHENAMIDE-P (11,32) + ETHOFUMESATE (11,22) + LENACILE (9,72) | Modérée-élevée |
| **Maïs** | S-METOLACHLORE (11,70) + TERBUTHYLAZINE (9,75) | Modérée |
| **Pommes de terre** | METRIBUZINE (12,50) + METOBROMURON (11,43) + PROSULFOCARBE | **15–33 kg/ha** (la plus élevée en Wallonie) |
| **Colza** | METAZACHLORE (11,54) | Modérée |
| **Pois / haricots** | BENTAZONE (13,04) | Faible surface mais indice très élevé |

> Source quantités : PGDH3 §I.3.3b, d'après CORDER (2020) et Habran et al. (2022).

---

## ÉTAPE 2 — Présence des cultures à risque dans les zones de surveillance

### 2.1 Délimitation des zones d'analyse

| Zone | Description | Source |
|---|---|---|
| **Zones de protection** (codes `AC_XXX`) | Zones 1 (ZPI), 2a, 2b (ZPR), 3 (ZPE) — périmètres réglementaires approuvés par arrêté ministériel | Annexe 5 PGDH3 / DGO3 (16/03/2020) |
| **ZAC** | Zone à Alimentation de Captage — bassin d'alimentation hydrogéologique du captage | SPW-DESo / outil QGIS PRIOR'eau |

La **ZAC** est le périmètre prioritaire pour l'analyse : elle représente l'ensemble de la surface dont les eaux de pluie alimentent le captage, et peut être bien plus étendue que les zones de protection réglementaires.

### 2.2 Données d'occupation du sol

| Donnée | Source | Usage |
|---|---|---|
| **RPG / SIGEC-LPIS** | Agence pour l'Agriculture wallonne (ASP) | Identifier les parcelles et cultures dans la ZAC |
| **Carte Smart-Map** (kg/ha/an, moyenne 2015-2017) | CRA-W / Habran et al. (2022) — interpolation SVM | Quantités de s.a. épandues spatialisées |
| **INDIC'eau terrain** (données PROTECT'eau depuis 2021) | CRA-W / PROTECT'eau | Score de risque réel par parcelle et par culture |
| **Indicateur CSI** (séquence culturale) | Vandevoorde & Baret (2023) — DossierCRAW Fig. 14 | Pression cumulée des rotations sur la ZAC |

### 2.3 Traitement SIG dans QGIS

```
1. Charger la couche ZAC + zones de protection AC_XXX (Annexe 5 PGDH3)

2. Intersecter avec le RPG
   → Extraire toutes les parcelles agricoles situées dans la ZAC
   → Calculer la surface par type de culture (ha)

3. Attribuer à chaque parcelle le score de risque de sa culture :
   Score parcelle = Σ [(dose_sa / DMA_culture) × indice_lixiviation_CRA-W_sa]
   (formule INDIC'eau — Article INDIC'eau CRA-W)

4. Superposer avec Smart-Map
   → Vérifier les quantités réelles de s.a. épandues par commune/secteur

5. Calculer l'INDIC'eau agrégé par ZAC :
   INDIC'eau_ZAC = Σ (Score_parcelle × Surface_parcelle) / Surface_ZAC_agricole
```

---

## ÉTAPE 3 — Amplification du risque par les formations karstiques

### 3.1 Pourquoi le karst est un facteur aggravant majeur

En milieu karstique, le transfert des PPP vers les ESO est **direct, rapide et non filtré** :
- absence de filtration par la zone non saturée ;
- circulations souterraines rapides via les conduits karstiques ;
- temps de dégradation insuffisant avant d'atteindre la nappe ;
- les indices de lixiviation standards (GUS, M.LEACH) **sous-estiment** le risque en contexte karstique.

> La méthode **EPIK** est recommandée pour la cartographie de la vulnérabilité intrinsèque en milieu karstique (mentionnée dans DossierCRAW Fig. 9), en remplacement de DRASTIC.

### 3.2 Formations karstiques wallonnes à croiser

*(Source : Fig. 11 DossierCRAW_2304 — Carte des principales formations aquifères de Wallonie, SPW 2024 ; PGDH3 §III.1)*

| Formation karstique | Localisation | Masses ESO potentiellement concernées |
|---|---|---|
| Calcaires du Tournaisis | Hainaut occidental | RWE (district Escaut) |
| Calcaires du Condroz | Entre Sambre et Meuse | RWM (district Meuse) |
| Calcaires du Frasnien | Ardenne septentrionale | RWM |
| Calcaires du Famennien | Entre-Sambre-et-Meuse | RWM |
| Calcaires du Viséen | Bord nord du Bassin de Namur | RWM |

> **Note PGDH3** : l'étude HGE-ULiège (2013-2016) sur les calcaires et grès du Condroz montre qu'une part importante de l'eau quittant le bassin par les eaux de surface a transité par le milieu souterrain, confirmant la forte connectivité ESO-ESU et donc la vulnérabilité accrue de ces formations.

### 3.3 Données à mobiliser

| Donnée | Source |
|---|---|
| Carte des formations aquifères de Wallonie | SPW 2024 (Fig. 11 DossierCRAW) |
| Fiches masses d'eau souterraine | eau.wallonie.be (district Meuse / Escaut / Rhin) |
| Annexe 3 PGDH3 | Caractéristiques des 34 masses ESO (karstification, profondeur nappe, confinement) |
| Carte de vulnérabilité DRASTIC / EPIK | SPW-DESo (si disponible) / "Pesticide fate tool" (DossierCRAW Fig. 10) |

### 3.4 Intégration dans l'analyse spatiale

Dans QGIS, attribuer à chaque ZAC un **coefficient d'amplification karstique** :

| Type de formation sous la ZAC | Coefficient |
|---|---|
| Aquifère karstique (calcaires) — nappe libre | 3 (risque fortement amplifié) |
| Aquifère fissuré — nappe libre | 2 |
| Aquifère sableux / poreux — nappe libre | 1,5 |
| Aquifère captif / confiné | 1 (risque atténué) |

```
Score de risque final ZAC = INDIC'eau_ZAC × Coefficient_karstique
```

---

## Synthèse — Carte de risque intégré et priorisation des ZAC

### Matrice de priorisation

```
                        INDIC'EAU AGRÉGÉ PAR ZAC
                    Faible      Modéré      Élevé
                 ┌──────────┬──────────┬──────────┐
KARST / NAPPE    │          │          │          │
LIBRE            │  MODÉRÉ  │  ÉLEVÉ   │ TRÈS     │
                 │          │          │ ÉLEVÉ    │
                 ├──────────┼──────────┼──────────┤
AQUIFÈRE         │          │          │          │
CAPTIF /         │  FAIBLE  │  MODÉRÉ  │  ÉLEVÉ   │
SEMI-CAPTIF      │          │          │          │
                 └──────────┴──────────┴──────────┘
```

### Validation par les données de surveillance (Calypso)

La carte de risque est **validée et calibrée** par croisement avec les détections existantes dans la base Calypso (SPW-DESo) :

- **Détections > 75 ng/L** dans un ouvrage de la ZAC → zone en déclassement, action urgente
- **Détections 30–75 ng/L** → zone à risque, action préventive prioritaire (approche PRIOR'eau)
- **Détections < 30 ng/L** → surveillance renforcée si score de risque élevé

---

## Récapitulatif des données et outils

| Étape | Donnée | Source | Outil |
|---|---|---|---|
| 1 — Substances | Tableau 4 — indices de lixiviation | DossierCRAW_2304 (CRA-W) | Tableur |
| 1 — Cultures | Liste 21 s.a. INDIC'eau par culture | Article INDIC'eau (CRA-W) | Tableur |
| 2 — Zones | Périmètres ZAC + zones AC_XXX | Annexe 5 PGDH3 / SPW-DESo | QGIS |
| 2 — Cultures | RPG/SIGEC + Smart-Map | ASP + CRA-W (Habran et al., 2022) | QGIS |
| 2 — Score parcelle | INDIC'eau | CRA-W / PROTECT'eau | QGIS / tableur |
| 3 — Karst | Carte formations aquifères | SPW 2024 / Annexe 3 PGDH3 | QGIS |
| 3 — Vulnérabilité | Fiches ESO / DRASTIC / EPIK | SPW-DESo / eau.wallonie.be | QGIS |
| Validation | Détections Calypso (ESO) | SPW-DESo | QGIS / tableur |

---

## Livrables attendus

1. **Carte de vulnérabilité ESO** par ZAC (formations karstiques + type d'aquifère)
2. **Carte de pression PPP** par ZAC (INDIC'eau agrégé + cultures dominantes à risque)
3. **Carte de risque intégré** (croisement des deux axes)
4. **Tableau de bord par ZAC** : cultures à risque présentes, substances prioritaires, détections Calypso existantes, niveau de priorité d'action
5. **Résumé opérationnel par centre PROTECT'eau** (modèle PRIOR'eau — DossierCRAW Fig. 22)

---

*Document élaboré sur base des sources suivantes :*
- *Bergiers G. et al. (2023). PRIOR'eau — Dossier CRA-W 23-04. Centre wallon de Recherches agronomiques, Gembloux.*
- *CRA-W / PROTECT'eau. Article INDIC'eau — Réduire l'impact des herbicides sur la qualité de l'eau grâce à INDIC'eau.*
- *SPW Agriculture, Ressources naturelles et Environnement (2023). Troisièmes Plans de Gestion des Districts Hydrographiques Wallons (PGDH3) — cycle 2022-2027 : document principal, Annexes 3, 5, 7, 13.*
- *SPW ARNE (2023). Méthodologies relatives à la caractérisation des masses d'eau souterraine. Juillet 2023.*
- *SPW ARNE (2023). Méthodologies relatives à la classification de l'état quantitatif des masses d'eau souterraine. Juillet 2023.*
