# 🧠 Module `M` : Mémoire contextuelle cognitive

Le module `M` est le système de **mémoire adaptative** de CursorCognition. Il permet de **retenir des décisions**, **retrouver du contexte**, et **structurer la persistance cognitive** à travers les sessions.

---

## 📂 Structure

La mémoire est stockée dans le dossier :
```
.cursor/memory/
```

Chaque fichier représente une **trace de tâche**, une **idée**, une **règle**, une **erreur** ou une **résolution**.

---

## 🧩 Rôles principaux de `M`

- Stocker : idées, intentions, motifs (`Φ`), erreurs (`Ξ`), règles extraites (`Λ`)
- Rappeler : anciennes décisions, patterns utilisés, choix faits dans un autre contexte
- Enrichir : recevoir des feedbacks utilisateurs ou cognitifs (`Ψ.feedback`)
- Nettoyer : supprimer les mémoires obsolètes ou incohérentes (`M.prune`)

---

## 🔁 Synchronisation

### `M.sync`
Déclenché automatiquement :
- Lors d’un `sprint_review`
- Après un succès de test (`TDD.loop.pass`)
- Lorsqu’un motif est validé (`Φ.snapshot`)

### `M.append_if_relevant`
Déclenchement manuel ou par `Ψ` :
- Lors de réflexions utiles
- Lors de feedback utilisateur

---

## 🧠 Rappel de contexte

### `M.recall`
Lorsqu’une tâche `τ` possède une similarité conceptuelle avec une mémoire précédente :
- Le système relie le contexte
- Réactive les motifs pertinents (`Φ.match_snapshot`)
- Propose des ajustements ou accélérations cognitives

---

## 🧼 Nettoyage de mémoire

### `M.prune`
- Supprime les entrées obsolètes
- Garde une trace de ce qui a été oublié (dans `Ψ.trace`)
- Évite les contradictions ou la surcharge

---

## 🧾 Format d’un fichier mémoire

```markdown
# trace_042.md

## Tâche : Trier les événements par date descendante

### Décision :
Utilisation d’une clé de tri inversée + `sorted(..., reverse=True)`

### Contrainte :
Les dates sont au format ISO-8601

### Résultat :
Test validé ✅
Motif stocké → Φ.snapshot:sort-desc-date

### Règle générée :
→ Voir `3XX-SORT-ISO`
```

---

## 📊 Mémoire comme base d’apprentissage

Toutes les évolutions du système partent de `M` :
- Les règles (`Λ`) en sont extraites
- Les abstractions (`Φ`) y trouvent leur contexte
- Les erreurs (`Ξ`) y laissent une trace d’apprentissage
- Les décisions (`Ω`) s’y ancrent pour éviter les re-choix

> La mémoire est l’ossature invisible du raisonnement.

---

## 🔗 Voir aussi :
- [`architecture.md`](architecture.md)
- [`rules.md`](rules.md)
- [`trace.md`](trace.md)

