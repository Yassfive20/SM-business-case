📚 Wiki Business Case SM Yassine — README
> \*\*Build initial complet : 25 pages markdown\*\* organisées selon le pattern LLM Wiki.
>
> Ce dossier est conçu pour être uploadé dans le \*\*Project Knowledge\*\* de Claude (claude.ai) afin de devenir persistant entre les sessions.
---
🚀 Quick start — Upload dans le Project Knowledge
Décompresser ce zip dans un dossier local (ex: `wiki\_yassine/`)
Ouvrir ton projet sur claude.ai
Dans la sidebar du projet, cliquer sur "Project knowledge"
Drag & drop tous les fichiers `.md` (sans la structure de dossiers — claude.ai ne préserve pas l'arborescence)
⚠️ Renommer optionnellement chaque fichier avec un préfixe pour préserver le contexte :
`00\_schema.md` → garder
`candidate/profile.md` → renommer en `candidate\_profile.md`
`narrative/thesis\_central.md` → renommer en `narrative\_thesis\_central.md`
etc.
Une fois uploadés, dans toute nouvelle conversation, Claude pourra rechercher dans le wiki avec `project\_knowledge\_search`
---
🔄 Workflow recommandé pour les itérations
Quand tu veux modifier une slide
Tu écris : "Réécris la slide 7 avec [contrainte X]"
Claude consulte automatiquement (en interne) :
`00\_schema.md` — pour le ton et les conventions
`narrative/thesis\_central.md` — pour la cohérence stratégique
`narrative/angles\_explores.md` — pour ne pas reproposer un angle écarté
`evaluation/grille\_partners.md` — pour vérifier la couverture critère
Claude propose la nouvelle slide + log la modification dans `00\_log.md`
Quand tu veux que je fasse une auto-critique
Tu écris : "Évalue ce que je viens de produire contre la grille"
Claude consulte `evaluation/grille\_partners.md` + `evaluation/self\_assessment\_v1.md`
Claude produit un scoring honnête sur les 7 critères
Quand Yassine te donne une nouvelle donnée
Tu écris : "Ajoute ce KPI : chargeabilité Yassine FY26 = 87%"
Claude met à jour la page concernée (ici `candidate/achievements\_FY26.md` + `candidate/mission\_anchor\_servier.md`)
Claude propage l'info dans les slides où elle apparaît
Claude log dans `00\_log.md`
---
🗂️ Carte du wiki
```
wiki/
├── 00\_schema.md                          ← À LIRE EN PREMIER (contrat de fonctionnement)
├── 00\_index.md                           ← Catalogue navigable
├── 00\_log.md                             ← Journal chrono
│
├── candidate/                            ← QUI est Yassine
│   ├── profile.md                        (parcours complet)
│   ├── mission\_anchor\_servier.md         (mission chargeable)
│   ├── tg\_lead\_responsabilite.md         (rôle Lead TG)
│   └── achievements\_FY26.md              (réalisations datées)
│
├── narrative/                            ← LA THÈSE stratégique
│   ├── thesis\_central.md                 (la phrase pivot)
│   ├── 3\_vagues\_marche.md                (l'angle d'attaque)
│   ├── angles\_explores.md                (registre des arbitrages)
│   └── messages\_cles\_par\_critere.md      (mapping message → grille)
│
├── market/                               ← LE CONTEXTE documenté
│   ├── gts\_thesis.md                     (synthèse GTS)
│   ├── ewm\_market.md                     (synthèse EWM)
│   ├── ia\_sap\_landscape.md               (synthèse IA SAP)
│   └── deloitte\_positioning.md           (positionnement Deloitte FR)
│
├── evaluation/                           ← LA CRITIQUE objective
│   ├── grille\_partners.md                (les 7 critères — référence)
│   ├── self\_assessment\_v1.md             (scoring v1 : 21/35)
│   ├── gaps\_identifies.md                (13 gaps actionables)
│   └── partner\_questions\_anticipees.md   (Q\&A préparées)
│
├── references/                           ← LES PATTERNS d'autres SM
│   ├── pattern\_berod.md                  (BCase Ariba 2021)
│   ├── pattern\_serres.md                 (BCase Supply Chain 2021 — jumeau)
│   └── patterns\_communs.md               (synthèse best practices)
│
└── deliverables/                         ← LE PITCH concret
    ├── slide\_outline\_v1.md               (plan slide-par-slide)
    ├── speech\_pitch\_v1.md                (texte du speech)
    └── speaker\_notes\_v1.md               (notes par slide)
```
---
📋 Synthèse de l'état actuel (au 25 avril 2026)
Ce qui est en place
✅ Diagnostic v1 : 21/35 (60%) — défendable mais pas victorieux
✅ Forces identifiées : Marché (5/5) + Management RH (4/5)
✅ Gaps prioritaires : Dév. commercial, Points forts explicites, Axes d'amélioration
✅ Plan v2 : 3 chantiers majeurs + 10 enrichissements
Ce qu'il faut récupérer côté Yassine
KPIs delivery Servier (chargeabilité, marge, volume MD)
Quote sponsor Servier (si possible)
Quote consultant encadré (si possible)
Volumes des 4 missions EWM déclinées (Sanden, Safran, autres)
Pipe FY27 chiffré avec probabilités
Réconciliation effectifs TG (FTE staffing vs communauté)
Date prise TG (sept 2025 vs nov 2026 — incohérence dans les sources)
Date publication livre blanc USF
Statut formel CoE Logistique
Ce qui peut être lancé en parallèle (côté Coach)
Slide ROI quantifié du redressement TG (priorité 1)
Réécriture slide 11 avec différenciateurs explicites (priorité 1)
Slide axes d'amélioration explicites (priorité 1)
Validation sources chiffres marché EWM (priorité 2)
Frise chronologique du parcours pour appendice E (priorité 3)
---
💡 Tips pour bien utiliser ce wiki avec Claude
À FAIRE
✅ Demander à Claude de toujours consulter le wiki avant de produire une slide
✅ Lui rappeler de logger chaque modification dans `00\_log.md`
✅ Lui demander régulièrement de faire des "lint checks" (cohérence chiffres, contradictions, gaps)
✅ Garder ce README à la racine du Project Knowledge
À ÉVITER
❌ Ne pas écraser une page sans loguer la modification
❌ Ne pas ressortir un angle déjà écarté (cf. `narrative/angles\_explores.md`)
❌ Ne pas inventer un chiffre — toujours flagger `\[À CONFIRMER]` si manquant
❌ Ne pas oublier de re-uploader la version mise à jour dans le Project Knowledge après chaque session significative
---
🔄 Procédure de mise à jour entre sessions
À la fin d'une session productive avec Claude :
Demander : "Génère un .zip de l'état actuel du wiki avec les modifications de cette session"
Claude package
Tu télécharges, tu extrais
Dans le Project Knowledge claude.ai, tu remplaces les fichiers modifiés (suppression + re-upload)
La session suivante repart sur l'état à jour
---
📞 Questions sur le wiki ?
Demander à Claude : "Comment fonctionne le wiki ?" — il consultera ce README et `00\_schema.md` pour répondre.
---
Construit le 2026-04-25. Build initial = 25 pages, 185 KB.
