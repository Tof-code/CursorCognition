# 🧪 TDD-First : Penser avant d’implémenter

Le moteur `TDD` de CursorCognition est le point de départ de toute tâche.
Avant que l’agent ne propose du code, il demande ou génère une spécification de test.

---

## 🌟 Objectif

- Ne jamais générer de code sans intention claire
- Formuler des tests comme hypothèses à valider
- Utiliser l’échec comme signal d’apprentissage
- Capturer le succès comme structure réutilisable

---

## 🔄 Boucle TDD dans CursorCognition

1. **Tâche (tau)** identifiée par l'agent.
2. Activation de `TDD.spec_engine`
   - Génère `spec_step_{x}.md` dans `.cursor/tasks/sprint_{n}/`
   - Basé sur l’intention, les contraintes, les patterns actifs (`Φ`)
3. Test évalué (via interprétation ou exécution simulée)
4. Échec ou succès :
   - **Fail** : diagnostic via `Ξ`, résolution via `D⟁`, re-spécification possible
   - **Pass** : capture de trace `Ψ`, synchronisation `M`, éventuelle extraction `Λ`

---

## 📁 Fichiers impliqués

- `.cursor/tasks/sprint_{n}/spec_step_{x}.md`
- `.cursor/tasks/sprint_{n}/step_{x}.md`
- `.cursor/memory/trace_{id}.md`
- `.cursor/rules/_draft_from_spec_{x}.mdc`

---

## 🧠 Spécification comme cognition

Une spécification est une hypothèse structurée.

Elle reflète l’intention comportementale d’un module à venir.

- Inférée automatiquement par `TDD.spec_engine`
- Peut être enrichie par l’utilisateur
- Devient une entrée pour l’abstraction (`Φ`) et les règles (`Λ`)

---

## 🔐 Contraintes internes

- Le module `Ω*` refuse toute génération si `TDD.spec_engine` n’a pas été appelé.
- `TDD.priority` force la génération de spéc avant tout code.
- Toute tâche sans `spec` est considérée comme **incomplète**.

---

## 📈 Impact sur la cognition

- Déclenche des abstractions tôt (`Φ`)
- Génère des structures réutilisables (`Λ`)
- Trace les intentions et validations (`Ψ`)
- Transforme l’échec en signal réorganisateur (`Ξ`, `D⟁`)

---

## 💡 Exemple (fictif)

```markdown
## spec_step_01.md
### Intention :
Vérifier que le gestionnaire de tâches classe les entrées par priorité décroissante.

### Conditions :
- Entrées avec {titre, priorité}
- Aucune dépendance externe

### Attendu :
- Les tâches sont triées de façon descendante
- Le tri est stable (ordre initial conservé à priorité égale)
```

---

## 🚪 Modifier le comportement TDD

Voir [`architecture.md`](architecture.md) pour ajuster :
- `TDD.priority`
- `spec_engine` behavior
- loop triggers in `Σ_hooks`
