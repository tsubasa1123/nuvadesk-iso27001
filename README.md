# Mission de conformité ISO/IEC 27001:2022 — NuvaDesk SAS

> **Cas d'étude** réalisé dans le cadre de mon portfolio GRC. NuvaDesk SAS, ses salariés, ses clients et ses chiffres sont inventés ; la méthode, les référentiels et l'outillage sont réels.

Accompagnement d'une PME SaaS vers la certification ISO 27001, de l'analyse d'écarts à la revue de direction, avec une analyse de risques EBIOS RM et un SMSI piloté dans **CISO Assistant** (auto-hébergé sous Docker).

---

## Le client

| | |
|---|---|
| **Organisation** | NuvaDesk SAS, éditeur d'une plateforme SaaS de support client |
| **Taille** | 85 salariés, siège à Lyon |
| **Hébergement** | AWS (région UE) |
| **Enjeu** | Clients bancaires et grands comptes exigeant un certificat ISO 27001 |
| **Périmètre du SMSI** | Conception, développement, hébergement, exploitation et support de la plateforme SaaS |
| **Objectif** | Audit de certification visé le 22/10/2027 |

## Compétences démontrées

| Compétence | Où la trouver dans la mission |
|---|---|
| **ISO 27001** | Analyse d'écarts (123 exigences), DdA, 9 politiques, audit interne, revue de direction |
| **ISO 27005 / EBIOS RM** | Méthode de risques, 5 ateliers EBIOS RM, matrice 4×4, traitement et acceptation des risques |
| **GRC** | Gouvernance du SMSI, RACI, objectifs et indicateurs, tableau de bord, cycle PDCA complet |
| **IAM** | Politique de contrôle d'accès (POL-02), indicateur et constat sur les accès à privilèges |
| **TPRM** | Cartographie de l'écosystème (atelier 3), politique fournisseurs (POL-03), mesures M-ECO |
| **Security by design** | Politique de développement sécurisé (POL-05), mesures SDLC, pistes SAST |

## Déroulé de la mission

| Phase | Clauses ISO 27001 | Réalisations | Livrables |
|---|---|---|---|
| **1. Analyse d'écarts** | 4 à 10, annexe A | Audit initial NVD-AUD-01 dans CISO Assistant : 30 clauses et 93 mesures évaluées | Rapport d'écarts : 10 chantiers, 6 mesures conservatoires |
| **2. Cadre et risques** | 4, 5, 6.1 | Contexte du SMSI, politique de sécurité, méthode de risques, analyse EBIOS RM complète | DOC-01, POL-01, MET-01, RISK-01 |
| **3. Mesures et politiques** | 6.1.3, 7.5, annexe A | Déclaration d'applicabilité, 8 politiques thématiques, preuves dans l'outil | DdA (classeur Excel), POL-02 à POL-09 |
| **4. Évaluation et amélioration** | 6.2, 9.1, 9.2, 9.3, 10.2 | Objectifs, indicateurs, tableau de bord, audit interne, non-conformités, revue de direction | NVD-AUD-02, NVD-FA-01, REV-01 |

### Phase 1 — Analyse d'écarts
- Domaine et périmètre dédiés dans CISO Assistant, séparés d'un autre cas d'étude (DORA).
- Audit NVD-AUD-01 : chaque exigence qualifiée (conforme, partiellement conforme, non conforme) avec observation.
- Restitution au registre consultant : 10 chantiers priorisés et 6 mesures conservatoires.

### Phase 2 — Cadre du SMSI et analyse de risques
- **Contexte** (4.1 à 4.4) : enjeux internes et externes, parties prenantes et attentes, périmètre.
- **Politique de sécurité** (5.2) : objectifs 2027 et RACI.
- **Méthode de risques** (6.1.2, ISO 27005) : matrice NuvaDesk sur mesure (gravité G1 à G4 × vraisemblance V1 à V4), tolérance fixée au niveau « Modéré ».
- **EBIOS RM, ateliers 1 à 5** :
  - atelier 1 : valeurs métier, biens supports et événements redoutés ;
  - atelier 2 : couples source de risque / objectif visé ;
  - atelier 3 : cartographie de l'écosystème (criticité = dépendance × pénétration / (maturité × confiance)) et scénarios stratégiques ;
  - atelier 4 : chemins d'attaque et modes opératoires cotés ;
  - atelier 5 : plan de traitement (mesures M-TRT et M-ECO) et risques résiduels.
- **Acceptation des risques** : 6 risques modérés acceptés par des comptes approbateurs distincts (séparation des rôles), avec expiration au 23/02/2028.

### Phase 3 — Mesures, DdA et politiques
- **Déclaration d'applicabilité** : 93 mesures applicables ; à son émission, 10 conformes, 59 partiellement conformes, 24 non conformes.
- **8 politiques thématiques** : contrôle d'accès, fournisseurs, incidents, développement sécurisé, classification, sauvegarde et continuité, cryptographie, utilisation des actifs.
- Politiques saisies comme mesures de catégorie « Politique », avec preuves versionnées, statut d'approbation et date d'expiration.

### Phase 4 — Évaluation et amélioration
- **6 objectifs** (6.2) reliés à **6 indicateurs** (9.1), chacun avec un responsable, une cible et un diagnostic (Conforme, À risque, Non maîtrisé).
- **Tableau de bord** « Pilotage du SMSI » : 6 cartes avec cible et seuils tricolores.
- **Audit interne NVD-AUD-02** (9.2), conduit par un auditeur indépendant : 1 non-conformité majeure, 3 mineures, 2 observations, 2 pistes d'amélioration, 2 bonnes pratiques.
- **Traitement des non-conformités** (10.2) : classeur de constats, analyse des causes (5 pourquoi), actions correctives reliées aux constats, aux exigences et aux objectifs.
- **Revue de direction** (9.3) : éléments d'entrée, 9 décisions (budget, ressources, maintien de la certification), plan d'actions.

## La boucle d'amélioration continue

```
Objectif (OBJ-06) ──▶ Indicateur (MET-06) ──▶ Audit interne (A.8.13)
       ▲                                              │
       │                                              ▼
Revue de direction ◀── Action corrective (M-COR-01) ◀── Constat (NC-01)
```

Chaque élément est relié aux autres dans CISO Assistant : depuis un objectif, on retrouve son indicateur, le constat d'audit qui le concerne et l'action corrective qui le traite.

## Livrables

### Documents du SMSI (`docs/`)

| Référence | Document | Clause / mesure |
|---|---|---|
| NVD-SMSI-RPT-01 | [Rapport d'écarts](docs/NVD-SMSI-RPT-01_Rapport_ecarts.pdf) | Phase 1 : 10 chantiers, 6 mesures conservatoires |
| NVD-SMSI-DOC-01 | [Contexte du SMSI](docs/NVD-SMSI-DOC-01_Contexte_du_SMSI.pdf) | 4.1 à 4.4 |
| NVD-SMSI-MET-01 | [Méthode de gestion des risques](docs/NVD-SMSI-MET-01_Methode_gestion_risques.pdf) | 6.1.2, 8.2 (ISO 27005) |
| NVD-SMSI-RISK-01 | [Analyse de risques EBIOS RM](docs/NVD-SMSI-RISK-01_Analyse_EBIOS_RM.pdf) | 6.1.2, 6.1.3, 8.2, 8.3 |
| NVD-SMSI-POL-01 | [Politique de sécurité de l'information](docs/NVD-SMSI-POL-01_Politique_securite_information.pdf) | 5.2, 6.2 |
| NVD-SMSI-POL-02 | [Politique de contrôle d'accès et de gestion des identités](docs/NVD-SMSI-POL-02_Politique_controle_acces.pdf) | A.5.15 à A.5.18, A.8.2 à A.8.5, A.8.18 |
| NVD-SMSI-POL-03 | [Politique de relations avec les fournisseurs](docs/NVD-SMSI-POL-03_Politique_fournisseurs.pdf) | A.5.19 à A.5.23, A.8.21, A.8.30 |
| NVD-SMSI-POL-04 | [Politique de gestion des incidents de sécurité](docs/NVD-SMSI-POL-04_Politique_gestion_incidents.pdf) | A.5.5, A.5.6, A.5.24 à A.5.28, A.6.8 |
| NVD-SMSI-POL-05 | [Politique de développement sécurisé](docs/NVD-SMSI-POL-05_Politique_developpement_securise.pdf) | A.8.8, A.8.25 à A.8.33 |
| NVD-SMSI-POL-06 | [Politique de classification et de protection des informations](docs/NVD-SMSI-POL-06_Politique_classification.pdf) | A.5.9, A.5.12 à A.5.14, A.5.33, A.5.34, A.8.10, A.8.12 |
| NVD-SMSI-POL-07 | [Politique de sauvegarde et de continuité d'activité](docs/NVD-SMSI-POL-07_Politique_sauvegarde_continuite.pdf) | A.5.29, A.5.30, A.7.11, A.8.13, A.8.14 |
| NVD-SMSI-POL-08 | [Politique de cryptographie](docs/NVD-SMSI-POL-08_Politique_cryptographie.pdf) | A.8.24 (avec A.5.14, A.5.17, A.8.5) |
| NVD-SMSI-POL-09 | [Politique d'utilisation des actifs et du télétravail](docs/NVD-SMSI-POL-09_Politique_utilisation_actifs.pdf) | A.5.10, A.5.11, A.6.7, A.7.7, A.7.9, A.7.10, A.7.14, A.8.1 |
| NVD-SMSI-REV-01 | [Compte rendu de revue de direction 2027](docs/NVD-SMSI-REV-01_Revue_de_direction_2027.pdf) | 9.3 |

### Exports de CISO Assistant (`exports/`) et DdA (`dda/`)

| Export | Contenu |
|---|---|
| [Audit initial NVD-AUD-01](exports/NVD-AUD-01_Audit_initial.pdf) | Analyse d'écarts : 123 exigences évaluées |
| [Rapport de déclaration d'applicabilité](exports/NVD-AUD-01_Declaration_applicabilite_rapport.pdf) | DdA générée par l'outil |
| [Rapport EBIOS RM](exports/EBIOS-RM_Rapport_NuvaDesk_2027.pdf) | Ateliers 1 à 5, scénarios et plan de traitement |
| [Audit interne NVD-AUD-02](exports/NVD-AUD-02_Audit_interne_2027.pdf) | Audit interne 2027 et résultats étendus |
| [Déclaration d'applicabilité NVD-SMSI-DDA-01](dda/NVD-SMSI-DDA-01_Declaration_applicabilite.xlsx) | 93 mesures : applicabilité, justification, état de mise en œuvre |

## Captures

| Vue | Fichier |
|---|---|
| Audit interne : conformité et résultat étendu | `captures/audit-interne-nvd-aud-02.png` |
| Tableau de bord de pilotage | `captures/tableau-de-bord-dsh-01.png` |
| Constats et actions correctives | `captures/constats-nvd-fa-01.png` |
| Plan d'action de l'audit | `captures/plan-action.png` |
| Objectifs et diagnostics | `captures/objectifs-iso.png` |
| Analyse de risques EBIOS RM | `captures/ebios-rm.png` |

## Organisation du dépôt

```
├── README.md
├── docs/            # Livrables exportés en PDF (contexte, politiques, EBIOS RM, revue de direction…)
├── dda/             # Déclaration d'applicabilité (NVD-SMSI-DDA-01.xlsx)
├── exports/         # Exports CISO Assistant (rapports d'audit)
└── captures/        # Captures d'écran de l'outil
```

## Outillage

- **CISO Assistant** (Community Edition, intuitem), auto-hébergé avec Docker Compose sur une VM Ubuntu.
- Référentiel ISO/IEC 27001:2022 et module EBIOS RM de l'outil.
- Livrables rédigés au registre consultant, exportés en PDF.

## Limites assumées

- **Cas fictif** : l'organisation, les personnes et les données sont inventées. Les comptes utilisateurs (`@nuvadesk.ex`) n'existent pas.
- **Chronologie** : la mission se déroule de novembre 2026 à octobre 2027, mais l'outil a été utilisé en novembre 2026. CISO Assistant refusant les relevés datés dans le futur, seule la **mesure de référence** des indicateurs (07/11/2026) y est saisie. Les valeurs 2027 sont une **projection**, présentée dans la revue de direction.
- **Dates de décision** : les approbations enregistrées dans l'outil (acceptations de risques, preuves) portent leur date réelle de saisie, et non la date fictive de la mission.
- **Audit interne simulé** : les constats sont construits pour être cohérents avec les indicateurs et les objectifs, et ils sont signalés par la mention « [Simulation audit 06/2027] ».
