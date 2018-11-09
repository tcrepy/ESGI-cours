# Gestion de projet 
---

## Qu'est-ce qu'un projet ?

- Objectifs
- Equipe
- Deadlines

#### Un projet c'est MALIN

- Mesurable
- Atteignable
- Limité
- Identifié
- Négocié

# Projet Agile
---

Le triangle de fer (qualité / cout / delais) n'existe pas en agile
On met la priorité sur les delais en agile

## [Agile Manifesto](agilemanifesto.org)


### 4 piliers : 

1. Les individus et les interactions plus que le processus client
    - On préfère organiser un meetup plutôt que demander par mail
2. Des logiciels opérationnels plutôt qu'une doc exhaustive
   - le client demande à l'équipe le niveau de documentation dont elle a besoin pour développer le projet
3. La collaboration avec le client plus que la négociation contractuelle
    - On avance avec le client
4. L'adaptation au changement plus que le suivi d'un plan

## SCRUM

![scrum](https://slidesalad-yfnrup2alohuirz.netdna-ssl.com/wp-content/uploads/2017/11/013-Scrum-Process.jpg)

Fonctionne par sprint, avec un scrum master, un product owner, et les développeurs

permet de rendre un produit fonctionnel à la fin de chaque sprint

pas de cahier des charges, juste des users stories

### Product Owner : 
- Maximise la valeur du produit
- maximise le travail de l'equipe 
- définit l'ordre de dév des fonctionnalités
- explicite les éléments du backlog
- rédige les user strories
- prend les décisions importantes concernant l'orientation du projet
- s'assure que le backlog du produit est visible et compris de l'équipe
- Fix les objectifs d'un sprint au dévut de celui-ci

Il s'agit d'une personne et non d'un comité

Il est seul à diriger l'activité de l'équipe de développement (il fait le lien entre l'équipe et le client). Toutes les demandes passent par lui

Dans l'idéal, il travaille dans la même pièce que l'équipe

Il est important qu'il reste très disponible pour répondre aux questions de l'équipe

### Scrum Master

Il est responsable de la compréhension, de l'adhésion et de la mise en oeuvre de la méthode

- Communique la vision et les objectifs à l'équipe
- apprend au propriétaire du produit à rédiger les composantes du backlog
- facilite les rituels Scrum
- coach l'équipe de développement
- facilite l'intégration de la méthode à l'entreprise, surtout si celle-ci n'est pas agile
- ecarte les éléments pouvant perturber l'équipe
- Travailler avec les autres facilitateurs animateurs pour coordonner plusieurs équipes s'il y a lieu

### Planning poker

On echange pour estimer la durée et la compléxité des US

carte d'estimation : 
- on prend chaque US rédigés par le PO 
- Echange sur la fonctionnalité (technique)
- On estime leur complexité en point selon une suite de fibonacci (0,1,2,3,5,8,13...) ou en taille de teeshirt (XS, S, M...)
- Discussion sur l'estimation
- validation de l'estimation

### Sprint

A une durée d'un mois ou moins au cours duquel une version terminée est livrée

- L'objectif de sprint est fixe
- les objectifs de qualité sont maintenus. ils ne sont jamais revus à la baisse
- le perimètre peut etre clarifié et renégocié entre le PO et l'équipe selon ce qu'elle apprend

### Daily meeting

on parle de 3 sujets :
- ce qui a été réalisé la veille
- ce qui va etre réalisé aujourd'hui
- qu'est ce qui peut nous bloquer

15 min, au meme endroit, avec comme sujet que le sprint en cours

### Démonstration

à la fin du sprint

sont présents : 
- users
- PO
- SM
- Dev
- Ceux qui souhaitent y assister

Déroulement : 
- PO et SM explique les US qui ont été terminés ou non
- Dev discute du sprint
- dev demontre le travail réalisé
- le PO valide les US présentées ou non
- PO expose le product backlog tel qu'il est (ce qui reste et ce qui a été fait)
- Revue des délais budget fonctionnalités

ne doit pas exceder 4h

### Retrospective

occacion pour l'équipe de s'inspecter et de créer un plan d'amélioration qui sera mis en place au cours du sprint suivant

Les utilisateurs peuvent étre là

- Elle arrive tout de suite après la démo et avant le prochain sprint
- ne doit pas exceder 3h
- le SM anime et participe à la réunion

- on plante le décors 
- collecte des info
- générer des informations
- planifier des actions
- clore la rétrospective avec un return on time invested - ROTI (on note de 1 à 5 la retrospective)

## Scrum - Niveau

### Thème - Road Map

Correspond à la totalité du projet (6mois-1an)

### Epic - Release (Feature)

version majeure de l'app (2-3 mois)

### US -Sprint

1-4 semaines - Sortie mineure


## Backlog

Contenu 
- theme - road map
- features
- US
- Priorité
- statut (des US)
- macro chiffrage (on estime les points des features)
- chiffrage final

C'est une liste de toutes les fonctionnalités recherchés

## Users Stories

Card - conversation - confirmation (planning poker)

une user storie se redige de cette facon

- Recit métier : 
  - **En tant que** user
  - **je veux** réalisation d'une action
  - **afin de** objectif
- priorité 
- statut (redigée, attribuée, en cours...)
- régle de gestion : 
  - Exemple : on doit pouvoir envoyer plusieurs photos mais pas plus de 7
- NFR (spécificité technique) : 
  -  exemple : Une photo ne doit pas dépasser 500ko
- Critère d'acceptation (reprend les regles de gestion)
  - exemple : Etant donné que je suis sur la conversation avec une personne ou un groupe, je peux envoyer plusieurs photos qui s'afficheront en miniature et voir l'icone envoyé sur le message

##### INVEST

- Indépendant
- Négotiable
- Valuable
- Estimable
- Simple (small)
- Testable

Une US est une fonctionnalité unique qui est décrite de manière à pouvoir etre dev en un sprint

Une US doit apporter une valeur à l'utilisateur

Une US repond à 3 questions : 
- Who
- What
- Why

Les US : 
- Elles sont rédigées par le PO
- en cas d'oubli faire une US corrective à intégrer au prochain sprint
- en cas d'US trop importante (chiffrage / travail), la découper en plusieurs US
- Une US ne peut pas etre technique

Agile ne veut pas dire pas de doc

Voir méthode [story mapping](https://blog.myagilepartner.fr/index.php/2017/07/29/story-mapping-bien-comprendre-sa-creation/)