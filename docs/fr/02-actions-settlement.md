# 2. Actions et règlement

Le cœur expose des actions ciblées : swap, modification de liquidité, donation, take, settle, mint et burn. Chaque action modifie l’état d’un pool ou le solde net de la session unlock. Cette comptabilité par delta sépare le calcul de l’état intermédiaire du règlement final.

Les contrats et bibliothèques de src/ portent les invariants de prix, de liquidité et de positions. Le code d’intégration doit traiter correctement les retours de l’unlock et ne jamais supposer qu’un appel externe est inoffensif.

Cette mécanique fournit une primitive commune sur laquelle peuvent se brancher routeurs, agrégateurs, interfaces de liquidité et stratégies plus spécialisées.

[Chapitre suivant : hooks personnalisables](03-hooks.md)
