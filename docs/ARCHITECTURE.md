# OpenG7 Social — architecture

## Mission et état

Le [README](../README.md) définit une couche de coordination économique mondiale :
publications, discussions et intentions structurées. Le dépôt est en cadrage;
aucun front Angular ni serveur métier n’est encore présent. Le dépôt versionné
ne fournit pas de manifest applicatif ni de scripts de build, lint ou test.
Une configuration locale d’outillage ne constitue pas une application livrée.

## Frontières cibles

UI routée → features Social → clients/contrats publics → API de domaine → stockage
et intégrations. Le serveur reste autoritaire pour droits, visibilité et modération.
Le domaine Social possède Post, Thread, Offer/Request, Organization et modération.
La carte et les analyses externes sont des consommateurs/intégrations explicites.

## Front et confidentialité

La structure Angular proposée dans le README est une cible à créer selon les
besoins, sans reprendre les chemins ni registres Nexus. Utiliser des composants
standalone, signals locaux, NgRx pour le réellement partagé, formulaires typés,
i18n et SSR protégé. Les primitives partagées restent neutres et sans accès API.

Séparer signaux publics et négociation privée; minimiser les données exposées.
Prévoir droits serveur, signalement, anti-abus, modération et traces vérifiables.
Une organisation vérifiée ne rend pas automatiquement tous ses contenus publics.

## Évolution

Avant de livrer un module, expliciter son contrat, sa persistance, ses droits et
ses tests. Tenir l’état réel et les versions à jour dans les manifests et ce guide.
Les règles de travail sont dans [AGENTS.md](../AGENTS.md).
