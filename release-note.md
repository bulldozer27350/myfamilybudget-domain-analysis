# Release Notes — Silo Analyse (domain-analysis)

Toutes les versions publiées de ce dépôt respectent la spécification [SemVer 2.0.0](https://semver.org/lang/fr/).

---

## [0.0.1] - 2026-11-07

### Type de release
**Version initiale** (mise en place et validation de la structure autonome multi-dépôts)

### Résumé
Première version stable du silo Analyse (`domain-analysis`), regroupant `analysis-api` et `analysis-core` avec import du BOM centralisé, cycle de build autonome et configuration de déploiement GitHub Packages.

### Changements par composant
- **`analysis-api`** : contrats, modèles, interface de service (aucun changement métier).
- **`analysis-core`** : moteur de calcul pur, sans Spring ni JPA.

### Rétro-compatibilité & Compatibilité binaire
Non applicable : version initiale, aucune version antérieure publiée.