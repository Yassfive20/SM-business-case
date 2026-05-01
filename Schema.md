00 — Schema du Wiki | Business Case SM Yassine Dria
> **Ce fichier est le contrat de fonctionnement du wiki.** Il dit à toute instance future de Claude comment opérer dans ce projet. À lire en premier.
---
1. Mandat du projet
Construire un Business Case de promotion Manager → Senior Manager pour Yassine Dria, à présenter devant le comité de Partners de la practice EA (SAP) de Deloitte France.
Livrables :
Pitch deck PowerPoint (forme finale)
Speech aligné slide par slide
Speaker notes pour la défense orale
Statut actuel (au démarrage du wiki) : un BCase HTML standalone existe (16 slides : 11 + 5 appendices). Il sert de baseline V1 à itérer.
---
2. Ton et posture éditoriale (NON NÉGOCIABLE)
Toute production écrite doit respecter :
Charismatique — la promotion est aussi politique. Le candidat doit dégager de l'autorité, pas mendier un grade.
Axé ROI — chaque initiative se chiffre (k€, MD, % attrition évitée, RFP capturés). Pas de bullet sans impact.
Souveraineté technologique — angle Deloitte FR vs dépendance roadmap éditeur (SAP). C'est un différenciateur.
Leadership de practice — Yassine n'est plus un expert solo, il construit la capacité d'une practice. Vocabulaire : "je structure", "j'engage", "je redresse", "j'arme", "je capte le gisement".
À bannir :
Le ton CV ("je suis passionné par…")
Les passifs ("a été mené")
Les chiffres décoratifs sans implication business
Les superlatifs gratuits ("excellent", "remarquable")
Toute formulation qui sent l'auto-promotion défensive
---
3. Persona du candidat (résumé persistant)
Nom : Yassine Dria
Grade : Manager Deloitte EA-SAP, Paris
Ancienneté Deloitte : depuis 2018 (Capgemini avant : 2018-2021)
Ancienneté Manager : 2 ans
Expertise solution : SAP EWM (signature), GTS, TM, IM, HUM, LE
Expertise sectorielle : Pharma, Arômes, Énergie, Mining
Mission anchor (chargeable) : Servier — Lead Architect Logistics du Core Model pharma global, depuis fév. 2025
Responsabilité interne : Lead Talent Group Supply Chain France, depuis sept. 2025 (45+ consultants, périmètre EWM/GTS/TM/LGM/IM/HUM/LE)
Volet IA : Co-auteur livre blanc IA SAP avec l'USF, contributeur AI Discovery Challenge, focus SAP Joule + Business Agent Platform (BTP)
Formation : Ingénieur UTBM (logistique & génie industriel) + échange KAIST Corée du Sud
Langues : FR, EN, AR
→ Détail complet : `candidate/profile.md`
---
4. Grille d'évaluation Partners (les 7 critères impérieux)
Toute slide, toute itération, tout argument doit être traçable à au moins un de ces 7 critères. Si un élément ne sert aucun critère → il sort.
Gestion / Delivery — KPIs attendus (chargeabilité, marge, satisfaction client, livraisons à temps)
Management RH — encadrement, mentorat, attrition, formation, recrutement
Éminence — visibilité externe (publications, conférences, partenariats), thought leadership
Développement commercial — RFP gagnés, pipe, accounts ouverts, réponses à appels d'offres
Marché — connaissance et anticipation des dynamiques (technologie, secteur, concurrence)
Points forts — différenciateurs uniques du candidat (ce qu'aucun autre Manager n'apporte)
Axes d'amélioration / préconisations — lucidité du candidat sur ses propres limites
→ Détail + scoring par itération : `evaluation/grille_partners.md`
---
5. Architecture du wiki
```
wiki/
├── 00_index.md               ← catalogue de toutes les pages
├── 00_log.md                 ← journal chrono des itérations
├── 00_schema.md              ← CE FICHIER
│
├── candidate/                ← qui est Yassine (factuel)
├── narrative/                ← la thèse, les angles, les messages
├── market/                   ← le contexte de marché documenté
├── evaluation/               ← la grille et l'auto-critique
├── references/               ← patterns extraits Berod & Serres
└── deliverables/             ← slides, speech, speaker notes (par version)
```
---
6. Workflow d'itération (à respecter rigoureusement)
Op 1 — INGEST (nouvelle source)
Lire la source
Extraire facts → page concernée dans `candidate/`, `market/` ou `references/`
Si la source change un angle stratégique → mettre à jour `narrative/`
Logger dans `00_log.md` : `## [YYYY-MM-DD] ingest | <nom source> | <pages touchées>`
Op 2 — ITERATE (réécrire une slide ou le speech)
TOUJOURS lire d'abord `narrative/thesis_central.md` et `evaluation/grille_partners.md`
TOUJOURS vérifier `narrative/angles_explores.md` pour ne PAS reproposer un angle déjà écarté
Modifier la slide cible dans `deliverables/slide_outline_vN.md`
Vérifier la cohérence avec les slides amont/aval
Logger : `## [YYYY-MM-DD] iterate | slide N | <résumé du changement>`
Op 3 — CRITIQUE (auto-évaluation)
Pour chaque critère grille → noter /5 avec justification
Identifier les gaps → `evaluation/gaps_identifies.md`
Anticiper les questions Partners → `evaluation/partner_questions_anticipees.md`
Logger : `## [YYYY-MM-DD] critique | version vN | <score global>`
Op 4 — LINT (santé globale)
Vérifier cohérence chiffres entre pages (un même KPI doit dire la même chose partout)
Repérer claims orphelins (sans source dans `market/` ou `candidate/`)
Détecter angles sous-exploités vs grille
Lister TODO
---
7. Conventions de versionning
Versions : v1, v2, v3… (entiers seulement, pas de minor)
Chaque version = une livraison cohérente du pitch
La version courante est explicite dans `00_index.md`
Les anciennes versions ne sont pas supprimées : elles vivent dans `deliverables/archive/` à terme
Le speech et les slides d'une même version DOIVENT être cohérents (mêmes chiffres, même ordre d'arguments)
---
8. Règles de rédaction
Chiffres : toujours sourcés (nom de la source dans `market/` ou `candidate/`)
Claims qualitatifs : si pas de preuve → reformuler en intention ("ambition de…") ou supprimer
Acronymes SAP : EWM, GTS, TM, LGM, IM, HUM, LE, BTP, SCM, PLM — pas besoin de définir, le comité les connaît
Langue : Français pour tous les livrables. Wiki en français aussi (cohérence).
Date de référence : on raisonne en FY26 (en cours), FY27 (engagements à venir), FY28 (vision).
---
9. Garde-fous critiques
❌ Ne jamais inventer un chiffre. Si un chiffre manque → flag `[À CONFIRMER]` dans la slide.
❌ Ne jamais copier la prose des sources brutes (notamment les études GTS) — toujours reformuler.
❌ Ne jamais revenir sur un angle écarté sans loguer pourquoi on le réintroduit.
❌ Ne jamais produire une slide qui n'adresse aucun des 7 critères grille.
✅ Toujours challenger : "qu'est-ce qu'un Partner sceptique objecterait ici ?"
✅ Toujours privilégier 1 message fort par slide vs 4 messages tièdes.
---
Dernière mise à jour : 2026-04-25 (création du wiki)
