# 1. Le singleton PoolManager

Uniswap v4 concentre l’état de tous les pools dans un contrat central, PoolManager.sol. Cette architecture évite de déployer un contrat de pair par pool et rend les opérations multi-pools plus composables. Un intégrateur commence une session par unlock, puis exécute une séquence d’actions avant la clôture.

Le protocole suit les soldes nets dus par l’appelant ou par le pool. Tant que la somme des deltas est réglée au moment de la libération, plusieurs actions peuvent être combinées dans une seule interaction logique.

[Chapitre suivant : actions et règlement](02-actions-settlement.md)
