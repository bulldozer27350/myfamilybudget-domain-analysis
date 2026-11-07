# Release Notes — Silo Analyse (domain-analysis)

Toutes les versions publiées de ce dépôt respectent la spécification [SemVer 2.0.0](https://semver.org/lang/fr/).

---

## [0.0.2-SNAPSHOT] - En cours

### Type de release
**Développement en cours** (reprise après la version initiale `0.0.1`, aucune release stable
produite depuis)

### Résumé
Ajout de la documentation d'exigences du silo Analyse, sans aucun changement de code ni de
comportement métier : `analysis-api` et `analysis-core` restent identiques à la version `0.0.1`.

### Changements par composant
- **`doc/srs.adoc`** (nouveau) : Software Requirements Specification du silo Analyse — 41
  exigences fonctionnelles (`MFB-ANA-RF-001` à `MFB-ANA-RF-041`) et 12 exigences non
  fonctionnelles (`MFB-ANA-NRF-001` à `MFB-ANA-NRF-012`), chacune avec identifiant, titre, texte,
  note d'usage le cas échéant, méthode de vérification (Inspection / Analyse / Démonstration /
  Test) et traçabilité amont. Rédigé comme un fragment AsciiDoc sans titre de document, destiné
  à être concaténé (`include::`) au SRS consolidé de l'application MyFamilyBudget.
- **`doc/irs.adoc`** (nouveau) : Interface Requirements Specification spécifiant l'interaction
  entre l'application MyFamilyBudget et ce silo — nature de l'interface (appel Java synchrone
  intra-JVM, sans réseau), modèle de données échangé en entrée et en sortie (types, formats,
  règles d'arrondi), responsabilités de traduction côté application, contrat de build/JPMS, et
  règles de compatibilité (26 exigences `MFB-ANA-INT-001` à `MFB-ANA-INT-026`, chacune avec sa
  méthode de vérification). Même format de fragment AsciiDoc que `srs.adoc`, destiné à la même
  concaténation applicative.
- **`README.md`** : ajout d'un pointeur vers `doc/srs.adoc` et `doc/irs.adoc`.
- **`pom.xml`, `analysis-api/pom.xml`, `analysis-core/pom.xml`** : reprise du développement en
  continu après la release `0.0.1`, version bumpée vers `0.0.2-SNAPSHOT` conformément à l'étape 4
  du processus de release documenté dans `README.md`.

### Rétro-compatibilité & Compatibilité binaire
Aucun changement de code : compatibilité binaire et fonctionnelle strictement identique à
`0.0.1`. Ce patch est documentaire et de gestion de version uniquement.

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
