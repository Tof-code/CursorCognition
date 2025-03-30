# ❓ FAQ – CursorCognition

Une sélection de questions fréquentes autour du système, de son comportement et de ses limites potentielles.

---

## 💡 Le système refuse de générer du code. Pourquoi ?

Probablement parce que le module `TDD` est activé et aucune spécification n’a été fournie.

**Solution :** créer une `spec_step_{x}.md` ou laisser l’agent en générer une.

---

## 🧪 Est-ce que je peux désactiver `TDD-first` ?

Techniquement oui, en modifiant la priorité dans le prompt :
```text
TDD.priority = false
```
Mais ce n’est **pas recommandé** : cela supprime le cœur cognitif de CursorCognition.

---

## 🧠 Que fait exactement le module `Φ*` ?

Il identifie des **motifs d’abstraction** dans la spécification ou le code, les **capture sous forme de snapshot**, et les utilise pour suggérer des généralisations ou des règles (`Λ`).

---

## 📜 À quoi servent les fichiers `.mdc` dans `.cursor/rules/` ?

Ce sont des **règles déclaratives** utilisées par le moteur `Λ` pour :
- Vérifier la cohérence
- Suggérer des refactors
- Déclencher des structures ou contraintes réutilisables

---

## 🔁 Est-ce que l’agent apprend ?

Oui, mais **localement**. Il apprend à travers :
- `Φ.snapshot`
- `M.memory`
- `Ψ.trace`
- `Λ.autonomy`

> Il ne s’entraîne pas sur internet. Il apprend de votre projet.

---

## 🧼 Pourquoi certaines règles sont marquées comme `_DRAFT` ?

Ce sont des **propositions générées automatiquement** par `Λ.autonomy` à partir de motifs récurrents. Elles doivent être :
- Validées
- Éventuellement renommées
- Classées par masque (`0XX`, `3XX`, etc.)

---

## ⚠️ Que faire si une règle interfère avec mon code ?

Vous pouvez :
1. Modifier ou désactiver la règle dans `.cursor/rules/`
2. Ajouter une condition de contexte (e.g., exclure un fichier ou un motif spécifique)
3. Archiver la règle si elle n’est plus utile

---

## 🧾 Que contient une trace (`Ψ`) ?

Une trace standard contient :
- La tâche et l’intention (`Ω`)
- La spécification utilisée (`TDD`)
- Le raisonnement suivi
- Les erreurs et ajustements (`Ξ`, `D⍺`)
- Les règles invoquées ou extraites (`Λ`)

---

## 🧠 Est-ce que je peux créer mes propres modules ?

Oui, si vous suivez la logique modulaire :
- Un nom unique (`MODULENAME`) + un rôle cognitif clair
- Des points d’entrée (`Σ_hooks`) et de sortie (`Ψ.trace`, `M.sync`, `Λ.extract`)

---

## 🔗 Voir aussi
- [`architecture.md`](architecture.md)
- [`tdd-first.md`](tdd-first.md)
- [`rules.md`](rules.md)
- [`memory.md`](memory.md)
- [`trace.md`](trace.md)

