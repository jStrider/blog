---
layout: post
title: "Introduction à n8n"
date: 2025-08-12
categories: [automatisation, workflow, n8n]
tags: [n8n, docker, notion, automatisation]
author: Julien
---

## Première impression

J'ai beaucoup entendu parler de l'outil **n8n**, outil d'automatisation et de workflow management. J'avais un peu de mal à concevoir l'intérêt d'un tel outil mais je me suis dit "Ok, je vais tester".

## Installation

Hop, direction OVH, je prends un petit VPS, je prends l'option de backup automatique car je suis un peu frileux et je me connais. J'aime flirter avec le danger.

Je crée ma petite entrée DNS et j'installe.

### Documentation suivie

La documentation que j'ai suivie : [Installation Docker Compose](https://docs.n8n.io/hosting/installation/server-setups/docker-compose/)

### Expérience avec Docker

J'ai l'habitude de faire tourner les applications que j'utilise dans des containers. De manière plus générale, j'ai l'habitude de Docker Compose. Honnêtement, je vais devoir essayer autre chose. Kubernetes ou Swarm quand j'aurai le temps, histoire de me familiariser avec autre chose !

Bref, l'installation de n8n on-premise est étonnamment simple. Tout est intégré au Docker Compose y compris la génération de certificat, ce qui fait qu'on se retrouve très rapidement avec un site fonctionnel.

Évidemment, c'est simple à partir du moment où on lit un minimum la doc. **RTFM** comme disait l'autre !

## Première étape : mon premier workflow

En fait, lorsque je suis arrivé devant l'interface épurée de n8n, je me suis dit : *"Ça y est, c'est installé... et maintenant ?"*

En vrai, qu'est-ce que je peux faire comme workflow ? De quoi est capable cet outil ? Est-ce qu'au fond c'est vraiment mieux qu'un petit script Python qui fait des calls API ?

## Contexte personnel : Notion et PARA

J'aime bien **Notion**. J'essaie autant que je peux de l'utiliser pour organiser ma vie perso. Je trouve l'outil assez puissant et épuré. Dernièrement j'ai essayé le template "Second Brain" de Modern Byte.

Ça m'a permis de m'introduire à la méthode de Tiago Forte : **PARA** (pour Project, Area, Resources, Archive).

Voici le workflow que j'ai mis en place, mon premier workflow (ne vous moquez pas, j'en suis plutôt fier)

Il s'agit d'un workflow qui fait la chose suivante : 

Tous les matins a 7h30, il m'envoie un recap des projets non terminés et des taches de la journée.

Comment? Avec plusieurs nodes qui permettent de faire tout un tas d'actions très poussés.

[..]