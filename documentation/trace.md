# 🧾 Module `Ψ` : Trace cognitive & réflexion adaptative

Le module `Ψ` est le **registre mental** de CursorCognition. Il enregistre les raisonnements, les décisions, les erreurs, les motifs, et les règles activées. Il sert à la fois de **journal**, de **métacognition**, et de **système de rétroaction**.

---

## 🧠 Rôles de `Ψ`

- Capturer chaque étape de raisonnement (`Ω*`)
- Documenter les abstractions générées (`Φ*`)
- Tracer les règles déclenchées ou créées (`Λ`)
- Archiver les erreurs récurrentes (`Ξ`)
- Noter les contradictions rencontrées (`D⍺`)
- Servir de mémoire narrative consultable

---

## 🗂️ Structure des fichiers

Les traces sont stockées dans :
```
.cursor/memory/trace_{task_id}.md
```
Chaque fichier correspond à **une tâche**, **un test**, ou **un sprint**.

---

## 📋 Contenu typique d’un `trace_{id}.md`

```markdown
# trace_073.md

## Tâche : Implémenter un validateur d’email

### Raisonnement (`Ω`)
- L’adresse est une chaîne avec contraintes formelles
- Doit inclure un `@`, un nom de domaine, et un TLD valide

### Spécification (`TDD`)
- Tests sur des cas valides/invalides
- Construction via regex + test splitting

### Abstraction (`Φ`)
- Motif : `match-and-split`
- Snapshot : `Φ.email-validator.basic`

### Règle déclenchée (`Λ`)
- `3XX-REGEX-SAFE`

### Erreur rencontrée (`Ξ`)
- Erreur sur TLD optionnel (résolue par fallback logique)

### Résultat : ✅ Spéc valide, implémentation stable
```

---

## 💬 Dialogue & feedback

Si `Ψ.dialog_enabled = true` :
- Le système peut **engager un dialogue de réflexion** après chaque sprint
- Il peut **poser des questions sur les choix**, proposer des améliorations
- Il peut **enrichir la mémoire automatiquement** (`M.append_if_relevant`)

---

## 🔁 Sprint review

À la fin d’un sprint :
- `Ψ.sprint_reflection` résume le raisonnement, les choix faits, les abstractions consolidées
- Il génère une **trace de décision** utile pour :
  - Post-mortem technique
  - Création de nouvelles règles
  - Partage cognitif en équipe

---

## 🧩 Interactions transversales

| Source | Type de capture |
|--------|------------------|
| `Ω*` | Raisonnement logique |
| `Φ*` | Abstraction / structure |
| `Ξ*` | Erreurs / dérives détectées |
| `Λ`  | Règles actives ou extraites |
| `TDD`| Succès ou échec de spécification |
| `M`  | Ajout de contexte |  
| `D⟠` | Contradictions résolues ou ouvertes |

---

## 🧭 Utilité stratégique

`Ψ` permet :
- Une **traçabilité des décisions**
- Une **analyse postérieure** (via Git ou autre)
- Une **formation de modèles de raisonnement réutilisables**
- Une base pour entraîner d’autres IA avec une logique explicite

> CursorCognition ne pense pas dans le vide. Il documente **comment** il pense — et pourquoi.

---

## 🔗 Voir aussi :
- [`memory.md`](memory.md)
- [`tdd-first.md`](tdd-first.md)
- [`architecture.md`](architecture.md)
