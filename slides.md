---
theme: default
colorSchema: dark
css: ./styles.css
layout: default
section: Introduction
title: Monolithes, Modules & Évolutivité
subtitle: Projet de recherche Web V
chain: multi
---

- {v-click} Comparer trois blockchains de couche 1 : Ethereum, Solana et Sui.
- {v-click} Comprendre comment elles abordent la trilemme.
- {v-click} Pourquoi Solana et Sui sont vues comme « ETH-killers » ?

---
layout: default
section: Introduction
title: Objectifs de la présentation
chain: multi
---

- {v-click} Donner une intuition technique, pas juste marketing.
- {v-click} Mettre l’accent sur la structure interne plutôt que les prix.
- {v-click} Montrer l’impact des choix d’architecture sur devs et utilisateurs.

---
layout: default
section: Introduction
title: Plan
chain: multi
---

- {v-click} Trilemme, puis origines.
- {v-click} Ethereum (rappel) ; Solana (PoH, Sealevel).
- {v-click} Sui (Move, objet, Mysticeti) en profondeur.
- {v-click} Contrats, compatibilité, sécurité, performance.
- {v-click} Expérience dev et choix de L1.

---
layout: default
section: Trilemme
title: La trilemme des blockchains
chain: multi
image: https://quickchart.io/chart?c=%7B%22type%22%3A%20%22radar%22%2C%20%22data%22%3A%20%7B%22labels%22%3A%20%5B%22S%5Cu00e9curit%5Cu00e9%22%2C%20%22D%5Cu00e9centralisation%22%2C%20%22Scalabilit%5Cu00e9%22%5D%2C%20%22datasets%22%3A%20%5B%7B%22label%22%3A%20%22Trilemme%22%2C%20%22data%22%3A%20%5B9%2C%209%2C%206%5D%2C%20%22backgroundColor%22%3A%20%22rgba%28177%2C143%2C255%2C0.35%29%22%2C%20%22borderColor%22%3A%20%22%23b18fff%22%7D%5D%7D%2C%20%22options%22%3A%20%7B%22plugins%22%3A%20%7B%22legend%22%3A%20%7B%22labels%22%3A%20%7B%22color%22%3A%20%22white%22%7D%7D%7D%2C%20%22scales%22%3A%20%7B%22r%22%3A%20%7B%22angleLines%22%3A%20%7B%22color%22%3A%20%22%23444%22%7D%2C%20%22grid%22%3A%20%7B%22color%22%3A%20%22%23555%22%7D%2C%20%22pointLabels%22%3A%20%7B%22color%22%3A%20%22white%22%7D%2C%20%22ticks%22%3A%20%7B%22display%22%3A%20false%7D%7D%7D%7D%7D
caption: Diagramme radar des compromis du trilemme.
---

- {v-click} Une blockchain veut être sécurisée, décentralisée et scalable.
- {v-click} En pratique, on optimise souvent deux axes au détriment du troisième.
- {v-click} Les choix d’architecture reflètent ce compromis.

---
layout: default
section: Trilemme
title: Axes de la trilemme
chain: multi
---

- {v-click} Sécurité : résistance aux attaques, finalité forte.
- {v-click} Décentralisation : nombreux validateurs, barrières d’entrée faibles.
- {v-click} Évolutivité : débit, latence, coûts maîtrisés.

---
layout: default
section: Trilemme
title: Ethereum dans la trilemme
chain: ethereum
image: https://cryptologos.cc/logos/ethereum-eth-logo.png?v=040
caption: Logo officiel Ethereum.
---

- {v-click} Priorise sécurité + décentralisation au niveau L1.
- {v-click} Évolutivité repoussée vers les L2 (rollups, validiums…).
- {v-click} Matériel de validation relativement accessible.

---
layout: default
section: Trilemme
title: Solana dans la trilemme
chain: solana
image: https://cryptologos.cc/logos/solana-sol-logo.png?v=040
caption: Logo officiel Solana.
---

- {v-click} Priorise fortement l’évolutivité sur la couche 1.
- {v-click} Exige un matériel de validation plus puissant.
- {v-click} Vise une décentralisation « suffisante » malgré des blocs denses.

---
layout: default
section: Trilemme
title: Sui dans la trilemme
chain: sui
image: https://cryptologos.cc/logos/sui-sui-logo.png?v=040
caption: Logo officiel Sui.
---

- {v-click} Modèle objet pour paralléliser les transactions.
- {v-click} Évolutivité sans sacrifier la sécurité BFT.
- {v-click} Architecture modulaire : consensus, exécution, stockage.

---
layout: default
section: Origines
title: Ethereum – origines
chain: ethereum
image: https://cryptologos.cc/logos/ethereum-eth-logo.png?v=040
caption: Identité visuelle Ethereum.
---

- {v-click} Lancé en 2015 par Vitalik Buterin et des cofondateurs.
- {v-click} Objectif : aller au-delà du simple transfert de valeur.
- {v-click} Vision : une « machine virtuelle mondiale » programmable.

---
layout: default
section: Origines
title: Solana – origines
chain: solana
image: https://cryptologos.cc/logos/solana-sol-logo.png?v=040
caption: Identité visuelle Solana.
---

- {v-click} Projet initié par Anatoly Yakovenko et Solana Labs.
- {v-click} Whitepaper centré sur Proof of History (PoH).
- {v-click} Objectif : blockchain haute performance pour usages massifs.

---
layout: default
section: Origines
title: Sui – origines
chain: sui
image: https://cryptologos.cc/logos/sui-sui-logo.png?v=040
caption: Identité visuelle Sui.
---

- {v-click} Développé par Mysten Labs, ex-équipe Diem (Meta).
- {v-click} Mainnet lancé en 2023.
- {v-click} Cible : simplifier la gestion d’actifs via modèle objet + Move.

---
layout: default
section: Ethereum
title: Ethereum aujourd’hui
chain: ethereum
---

- {v-click} Transition PoW → PoS (The Merge).
- {v-click} Consensus LMD-GHOST + Gasper pour la finalité.
- {v-click} Rôle : couche de règlement sécurisée pour un écosystème L2.

---
layout: default
section: Ethereum
title: Rôle des L2
chain: ethereum
---

- {v-click} Rollups optimistes et zk-rollups absorbent le trafic.
- {v-click} Données compressées sur Ethereum, exécution déportée.
- {v-click} Impact dev : choisir L2, arbitrer coûts et latence.

---
layout: default
section: Solana
title: PoH + Tower BFT
chain: solana
---

- {v-click} PoH : séquence de hachages servant d’horloge cryptographique.
- {v-click} Ordonnancement sans synchronisation constante.
- {v-click} Tower BFT : consensus PoS au-dessus de PoH avec lockouts.
- {v-click} Lockouts dissuadent les changements de fork (coût d’opportunité).

---
layout: default
section: Solana
title: Exécution parallèle avec Sealevel
chain: solana
---

- {v-click} Sealevel : moteur d’exécution parallèle basé sur les comptes.
- {v-click} Transactions déclarent les comptes lus/écrits.
- {v-click} Transactions indépendantes exécutées en parallèle.
- {v-click} Efficace pour flux DeFi / NFT massifs.

---
layout: default
section: Solana
title: SPL / Token-2022
chain: solana
---

- {v-click} SPL : standard de tokens natif (équivalent ERC).
- {v-click} Token-2022 ajoute intérêts, frais, hooks avancés.
- {v-click} Primitives DeFi et NFT directement sur ces standards.

---
layout: default
section: Sui
title: Sui en un coup d’œil
chain: sui
---

- {v-click} Layer 1 basé sur Move (héritage Diem).
- {v-click} Données centrées sur les objets, pas sur des comptes globaux.
- {v-click} Transactions pensées pour être fortement parallélisables.

---
layout: default
section: Sui
title: Modèle objet – principes
chain: sui
---

- {v-click} Tout est objet : tokens, NFT, coffres, marketplaces…
- {v-click} Chaque objet a un propriétaire ou un statut (shared, immutable).
- {v-click} Les transactions déclarent explicitement les objets touchés.

---
layout: default
section: Sui
title: Owned vs Shared objects
chain: sui
---

- {v-click} Owned : objet détenu par une seule adresse (ex : un NFT).
- {v-click} Shared : objet partagé entre plusieurs utilisateurs (ex : un DEX).
- {v-click} Objets disjoints = exécution parallèle sans blocage.
- {v-click} Certains cas simples évitent même le consensus complet.

---
layout: default
section: Sui
title: Parallélisme grâce au modèle objet
chain: sui
---

- {v-click} Deux transactions sur des objets distincts ne se bloquent pas.
- {v-click} Le throughput dépend de la contention sur les mêmes objets.
- {v-click} Favorise des objets indépendants plutôt que des contrats monolithiques.

---
layout: default
section: Sui
title: Mysticeti – pourquoi
chain: sui
---

- {v-click} Remplace Narwhal/Bullshark comme protocole de consensus.
- {v-click} Toujours basé sur un DAG pour réduire la latence.
- {v-click} Moins de tours de messages → finalité plus rapide.
- {v-click} Ressources recentrées sur l’exécution plutôt que la communication.

---
layout: default
section: Sui
title: Langage Move sur Sui
chain: sui
---

- {v-click} Move : langage orienté ressources, pensé pour les actifs.
- {v-click} Types Move empêchent la duplication accidentelle de tokens.
- {v-click} Move sur Sui épouse le modèle objet (modules, structs, capacités).

---
layout: default
section: Contrats
title: Ethereum – standards de contrats
chain: ethereum
---

- {v-click} Solidity / Vyper comme langages principaux.
- {v-click} Standards ERC-20, ERC-721, ERC-1155…
- {v-click} Tooling massif : OpenZeppelin, Foundry, Hardhat, etc.

---
layout: default
section: Contrats
title: Solana – programmes on-chain
chain: solana
---

- {v-click} Contrats surtout en Rust via le SDK Solana.
- {v-click} Anchor simplifie macros, schémas et IDL.
- {v-click} Les comptes remplacent un storage global monolithique.

---
layout: default
section: Contrats
title: Sui – Move et standards d’objets
chain: sui
---

- {v-click} Contrats = modules Move déployés on-chain.
- {v-click} Standards basés sur des objets (coins, NFT…) plutôt que ERC.
- {v-click} Objets composables : un objet peut posséder d’autres objets.

---
layout: default
section: Compatibilité
title: Portage Ethereum ↔ autres
chain: multi
---

- {v-click} EVM devenu un standard de facto.
- {v-click} Porter EVM → Solana ou Sui implique souvent réécriture.
- {v-click} Solutions : sidechains EVM, VM compatibles, transpileurs.

---
layout: default
section: Compatibilité
title: Solana – compatibilité
chain: solana
---

- {v-click} Architecture très différente de l’EVM (Sealevel, comptes).
- {v-click} Portage = repenser stockage et accès aux données.
- {v-click} Couches EVM expérimentales existent mais ne sont pas natives.

---
layout: default
section: Compatibilité
title: Sui – compatibilité
chain: sui
---

- {v-click} Modèle objet + Move = changement de paradigme vs EVM.
- {v-click} Portage → remodeler les assets en objets owned/shared.
- {v-click} Plus de travail au départ, mais modèles d’actifs plus riches.

---
layout: default
section: Sécurité
title: Ethereum – incidents historiques
chain: ethereum
---

- {v-click} Exemples : The DAO, bugs de contrats, forks correctifs.
- {v-click} Surface d’attaque énorme malgré audits et bug bounties.
- {v-click} Tooling formel et sécurité restent essentiels.

---
layout: default
section: Sécurité
title: Solana – interruptions réseau
chain: solana
---

- {v-click} Plusieurs interruptions depuis le lancement.
- {v-click} Causes : bugs runtime, congestion, ordonnancement.
- {v-click} Culture performance → cycle de risques plus rapide.

---
layout: default
section: Sécurité
title: Décentralisation & matériel
chain: multi
---

- {v-click} Ethereum : entrée validateur plus accessible (selon config).
- {v-click} Solana / Sui : besoins matériels plus élevés pour suivre le débit.
- {v-click} Trade-off : plus de performance, barrière d’entrée plus haute.
- {v-click} Sui reste jeune : vigilance sur maturité des devs Move.

---
layout: default
section: Performance
title: Comment lire les TPS ?
chain: multi
---

- {v-click} TPS théoriques vs TPS observés en production.
- {v-click} Transactions simples vs complexes (DeFi, NFT…).
- {v-click} Latence et finalité comptent autant que le TPS brut.
- {v-click} Toujours regarder la méthodologie de mesure.

---
layout: default
section: Performance
title: Ethereum – performance
chain: ethereum
---

- {v-click} L1 limitée en TPS mais très sécurisée.
- {v-click} Stratégie : externaliser sur de multiples L2 spécialisés.
- {v-click} Pas d’ambition de tout traiter sur la couche 1.

---
layout: default
section: Performance
title: Solana & Sui – performance
chain: sui
---

- {v-click} Solana : PoH + Tower + Sealevel → finalité rapide sur L1.
- {v-click} Sui : parallélisme objet + Mysticeti réduit la latence de consensus.
- {v-click} Solana exige matériel réseau costaud ; Sui optimise la contention.
- {v-click} Potentiel fort pour apps interactives temps réel (surtout Sui).

---
layout: default
section: Expérience dev
title: Ethereum – DX
chain: ethereum
---

- {v-click} Tooling mature : Hardhat, Foundry, Truffle…
- {v-click} Abondance de templates et de librairies (OpenZeppelin).
- {v-click} Documentation massive mais parfois fragmentée.

---
layout: default
section: Expérience dev
title: Solana – DX
chain: solana
---

- {v-click} Rust + Anchor : robuste mais courbe d’apprentissage réelle.
- {v-click} Outils : Solana CLI, explorers, frameworks d’indexation.
- {v-click} Debug plus complexe à cause du parallélisme et des comptes.

---
layout: default
section: Expérience dev
title: Sui – DX
chain: sui
---

- {v-click} Sui CLI, Explorer, SDK TypeScript pour dApps.
- {v-click} Move impose discipline stricte sur les modèles d’actifs.
- {v-click} Documentation en progression, écosystème jeune mais dynamique.

---
layout: default
section: Expérience dev
title: Choisir sa L1 comme dev
chain: multi
---

- {v-click} Ethereum : compatibilité maximale, choix de L2 variées.
- {v-click} Solana : performance brute pour apps temps réel massives.
- {v-click} Sui : modèle objet idéal pour actifs complexes et parallélisme.
- {v-click} Choisir selon use case, équipe et tolérance aux risques.

---
layout: default
section: Conclusion
title: Synthèse & message final
chain: multi
---

- {v-click} Chaque L1 fait des compromis différents dans la trilemme.
- {v-click} Ethereum : couche de règlement sécurisée + écosystème L2.
- {v-click} Solana : performance maximale sur une L1 monolithique.
- {v-click} Sui : modèle objet + Mysticeti pour parallélisme et finalité rapide.
- {v-click} Pas de « meilleur » absolu : aligner avec le use case.

---
layout: default
section: Conclusion
title: Questions / Réponses
chain: multi
---

- {v-click} Merci de votre attention !
- {v-click} Questions, commentaires, débats ?
