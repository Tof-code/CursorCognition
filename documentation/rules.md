# 🔖 Module `Λ` : Règles cognitives et évolution

Le module `Λ` est le centre de la **régulation structurelle** et de l’**auto-apprentissage** dans CursorCognition.
Il permet à l’agent de **comprendre les motifs récurrents**, d’**extraire des bonnes pratiques**, et de **créer ses propres règles** sous forme de fichiers `.mdc`.

---

## 🚀 Rôle principal de `Λ`

- Appliquer des règles existantes (dans `.cursor/rules/`)
- Extraire des règles à partir de motifs (`Φ.snapshot`)
- Créer automatiquement des fichiers `_DRAFT.mdc`
- Valider ou ajuster des structures de code, noms, patterns, tests

---

## 📁 Organisation des fichiers de règles

Les fichiers sont classés par **masques symboliques** :

```json
masks[
  "0XX": "Core standards",
  "1XX": "Tools & Language configs",
  "2XX": "Framework-specific",
  "3XX": "Testing",
  "8XX": "Workflows",
  "9XX": "Templates & Motifs",
  "_name.mdc": "Private logic"
]
```

Ces masques ne sont **pas des noms stricts**, mais des **identifiants sémantiques**. Ils guident l’organisation logique.

---

## 🏛️ Modes d’activation

- **Λ.pattern_alignment** : vérifie si une structure suit une règle connue
- **Λ.autonomy** : détecte des motifs émergents et propose des règles
- **Λ.check_applicability** : filtre les règles pertinentes selon le contexte
- **Λ.extract_from(Φ, Ψ)** : transforme une abstraction ou trace en règle candidate

---

## 🔨 Exemple de règle simple

```markdown
### Règle 3XX-TRI-001 : Tri stable obligatoire

**Contexte :** toute fonction de tri sur des objets avec priorité

**Motif :**
- Entrées avec {id, priorité}
- Sortie triée décroissante
- Ordre d’origine conservé à priorité égale

**Test d’application :** OK si stable, WARNING sinon
```

---

## 🌐 Interaction avec les autres modules

| Source | Rôle |
|--------|------|
| `Φ.snapshot` | Source principale de motifs abstraits |
| `TDD.loop` | Crée des tests à partir des règles |
| `Ψ.capture` | Logique cognitive associée à une règle |
| `Ξ.cleanup_phase` | Propose une généralisation post-nettoyage |
| `D⟁.log_to_memory` | Archive des tensions répétitives pour créer des règles |

---

## ✨ Création autonome

Si un motif se répète dans le projet :
- `Φ` le capture
- `Ψ` le confirme via trace décisionnelle
- `Λ.autonomy` propose une règle
- La règle est écrite dans `.cursor/rules/_DRAFT_{motif}.mdc`

Une fois validée, elle peut être renommée, masquée et activée.

---

## 📆 Cycle d’adoption d’une règle

1. **Observation** : motif récurrent détecté (`Φ` ou `Ξ`)
2. **Proposition** : `_DRAFT.mdc` généré par `Λ`
3. **Validation** : l’utilisateur (ou l’agent en mode confiance) accepte ou modifie
4. **Application** : règle active, surveille les structures similaires

---

## 🛠️ Personnalisation

Vous pouvez ajouter vos propres règles :
- En créant un fichier `.cursor/rules/_name.mdc`
- En utilisant la même structure que les règles internes
- En définissant vos propres masques si besoin

---

> 🔗 Voir aussi : [`tdd-first.md`](tdd-first.md), [`architecture.md`](architecture.md), [`memory.md`](memory.md)
