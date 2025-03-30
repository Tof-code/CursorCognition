# 🧬 Architecture de CursorCognition

CursorCognition repose sur une **architecture cognitive modulaire**, inspirée de la pensée en réseau, de la cognition distribuée et du raisonnement par tension et émergence.

Chaque module agit comme une **unité de traitement spécialisée**, interconnectée aux autres par des signaux, des contextes et des rétroactions.

---

## 🧠 Vue d'ensemble

| Module | Fonction principale | Inspiration |
|--------|---------------------|-------------|
| `Ω*`   | Noyau de raisonnement adaptatif | Logique ⨁ heuristique ⨁ mode |
| `Φ*`   | Détection d’abstraction et motifs | Perception ⨁ divergence contrôlée |
| `Λ`    | Système de règles évolutif | Rétro-ingénierie ⨁ apprentissage |
| `M`    | Mémoire contextuelle structurée | Consolidation mnésique |
| `T`    | Planification des tâches | Sprint structuré + rétro boucle |
| `TDD`  | Spécification test-first | Hypothèse vérifiable avant code |
| `Ξ`    | Diagnostic et nettoyage | Auto-dépuration et audit |
| `D⍺`   | Résolution de contradictions | Régulation logique |
| `Ψ`    | Trace cognitive & dialogue | Méta-réflexion + journalisation |

---

## 🧩 Détails par module

### `Ω*` – Noyau de raisonnement

- Prend une tâche (`τ`) et la transforme en **sous-problèmes cognitifs**
- Sélectionne un **mode de pensée** parmi :
  `deductive`, `analogical`, `skeptical`, `speculative`, etc.
- Évalue la **fiabilité des hypothèses (`Ωₜ`)**
- Propulse la tâche vers les modules pertinents : `Φ`, `TDD`, `Λ`, `Ψ`

---

### `Φ*` – Abstraction & motifs émergents

- Repère les **structures récurrentes** dans le code, les spécs, les idées
- Crée des **snapshots** sémantiques stockés dans la mémoire (`Φ.snapshot`)
- Détecte les **dérives d’abstraction** et les **écarts d’intention**
- Sert de base pour généraliser ou refactorer plus tard

---

### `Λ` – Générateur et régulateur de règles

- Applique des règles déjà présentes dans `.cursor/rules/`
- Génère de **nouvelles règles à partir des motifs** (`Φ`)
- Classe les règles par **masques (`0XX`, `3XX`, `9XX`, etc.)**
- Peut créer automatiquement un fichier `_DRAFT.mdc` si un motif est significatif

---

### `M` – Mémoire contextuelle persistante

- Stocke des traces, décisions, intentions, échecs et résolutions
- Peut être enrichie manuellement ou par `Ψ`, `Φ`, `Λ`
- Utilise `.cursor/memory/` comme base de stockage
- Active des souvenirs lors de tâches similaires (`M.recall`)

---

### `T` – Gestion des tâches et sprints

- Organise les tâches dans `.cursor/tasks/` avec :
  - `backlog.md`
  - `sprint_{n}/step_n.md`
  - `review.md`
- Permet une boucle complète : plan → spec → implémentation → revue
- Synchronise automatiquement avec mémoire, règles et abstractions

---

### `TDD` – Spécification pilotée par tests

- Le module **central dans le flux CursorCognition**
- Empêche toute génération de code sans spécification préalable
- Crée automatiquement des fichiers `spec_step_x.md`
- Apprend des tests qui échouent
- Archive tout passage de test réussi dans la mémoire (`Ψ + M + Λ`)

---

### `Ξ` – Diagnostic & nettoyage

- Surveille :
  - Code mort
  - Imports inutiles
  - Logique cassée
  - Redondances
- Archive tout bloc retiré (si demandé)
- Peut déclencher un nettoyage via `sprint_review` ou erreur

---

### `D⍺` – Résolution de contradictions

- Surveille les **tensions logiques, incohérences, doublons**
- Propose des stratégies :
  - Priorisation
  - Re-abstraction
  - Scoping
- Archive les tensions non résolues pour future itération

---

### `Ψ` – Trace cognitive & métadialogue

- Journalise chaque étape cognitive dans `.cursor/memory/trace_{id}.md`
- Capture :
  - Raisonnement
  - Abstractions
  - Erreurs
  - Règles invoquées
- Peut **engager un dialogue réflexif** si activé (`Ψ.dialog_enabled = true`)
- Sert de support de **rétro-ingénierie de décision**

---

## 🔗 Connexions transversales

Tous les modules sont interreliés.  
Exemples :
- `Ω_H` déclenche `TDD`, `Φ`, `Ψ`, `Λ`
- `Φ.snapshot` sert de source à `Λ.autonomy`
- `TDD` envoie ses résultats à `M`, `Λ`, `Ψ`
- `D⍺` alimente `Λ` en tensions génératrices de règles

---

## 📐 Schéma 
```mermaid
graph LR
    T[Tâches (T)]
    TDD[TDD: Spécification par test]
    Omega[Ω*: Raisonnement central]
    Phi[Φ*: Abstraction & motifs]
    Lambda[Λ: Règles]
    M[M: Mémoire contextuelle]
    Xi[Ξ: Diagnostic & Nettoyage]
    D[D⟠: Résolution de contradictions]
    Psi[Ψ: Trace cognitive & feedback]

    T --> TDD
    TDD --> Phi
    TDD --> Omega
    Omega --> Phi
    Omega --> Lambda
    Omega --> Psi
    Phi --> Lambda
    Phi --> M
    Lambda --> Psi
    TDD --> Psi
    TDD --> Xi
    Xi --> Psi
    Xi --> D
    D --> Psi
    Psi --> M
    M --> Omega
```


Tu peux contribuer ici : [`docs/contributing.md`](contributing.md)


