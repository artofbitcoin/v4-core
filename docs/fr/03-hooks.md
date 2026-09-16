# 3. Hooks personnalisables

À l’initialisation d’un pool, un hook peut être associé au cycle de vie. Les points before et after peuvent entourer l’initialisation, l’ajout ou le retrait de liquidité, le swap et la donation. Le hook peut ainsi ajouter une logique de frais, de politique ou de stratégie autour du pool.

Le choix du hook est figé pour le pool après son initialisation : l’intégrateur doit donc vérifier les permissions, le code et les hypothèses du hook avant d’utiliser la pool. La flexibilité ne supprime pas le risque ; elle le déplace vers les extensions et leurs interfaces.

Le dépôt illustre ainsi une architecture de noyau minimal et de comportements composables, avec des invariants qui doivent rester respectés à chaque callback.

[Chapitre suivant : sécurité et périmètre](04-security-scope.md)
