# 🧭 Diagramme d'architecture cognitive

Ce diagramme Mermaid représente le flux principal entre les modules cognitifs de CursorCognition.

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
