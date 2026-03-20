---
title: Traitement du ticket
icon: tabler/outline/stack-middle
summary: Traiter un ticket efficacement
toc: true
---

# :tabler-outline-stack-middle: Traitement du ticket

!!! info
    **Rappel du ‘tronc commun’**
    
    1. Catégorisation (assistanc technique, incident)


       1. Que faire pour améliorer la catégorisation
    2. Identification de l’incident / de la demande


       1. lecture des vidéo / message / screenshot
    3. Next step (voir [aide à la résolution](https://outline.teclib.com/doc/atelier-professionel-services-zWtbkyGGuY#h-aide-a-la-resolution))
    4. Faire un patch, le vérifier, l’appliquer / le livrer ….


       1. Que faire pour améliorer
    5. Communication


       1. Que faire pour améliroer (template etc ..)
    6. Utilisation des outils (DevTrack, GlpiCloud, bssh)


       1. Que faire pour améliorer (Doc, commande prêt à copier ….)
    7. Documentation suite au traitement d’un ticket


       1. Identifier un manque dans la documentation
     2. Faire la documentation

## Aide à la recherche de solution


1. Bien comprendre le besoin / l’incident (que faire si le client à mal exprimé son pb / sa demande) 
2. Vérifier les logs de l’application (backend)

   
   1. Pouvons nous améliorer l’affichage
   2. Avoir des filtres de dates
   3. Avoir des badges : 1 error, 2 warning, +99 notice (plus lien vers le error level)
   4. Améliorer le pugin Teclib Inventory Connector pour télécharger directement les logs dans un nouveau suivi [plugin support](/doc/fe069c1c-ebe2-4fc4-b21d-b518d2a7ee4d))
3. Vérifier les logs du navigateur (frontend)
4. Vérifier l’intégrité de GLPI (fichiers modifiés)
5. Comment vérifier si déjà corriger / en cours / pas traité
6. Comment reproduire
7. Désactgiver les plugins pour identifier si le pb vient du coeur ou des plugins
8. Quel env pour être ISO avec l’env du client (TGU, Version de GLPI)
9. Git Bisect

:::


## Vérifications initiales

* Consentement de l’utilisateur (point important)
* Présence des fichiers de logs
* Vérifier si les fichiers de GLPI ont été modifiés
* Identification de l’incident ou de la demande
* Analyse des éléments fournis :
  * vidéos
  * messages
  * captures d’écran
* Vérifier l’existence d’un TGU :
  * Si absent, définir la marche à suivre
* Prendre connaissance de l’environnement :
  * système d’exploitation (OS)

## Validation avant traitement

* Y a-t-il des ambiguïtés empêchant de commencer le traitement ? → Si oui : demander des compléments via un suivi
* Ai-je toutes les étapes et informations nécessaires pour :
  * analyser
  * comprendre
  * reproduire le problème → Si non : demander des compléments via un suivi
* Consulter la documentation Help pour aider à l’identification du problème

## Catégorisation

### Objectif

Classer correctement le ticket (assistance technique, incident, etc.)

### Points à définir

* Quand et comment catégoriser ?
* Quelles règles appliquer pour améliorer la catégorisation ?


## Améliorations / Documentation à envisager

### Logs

* Améliorer la qualité et la pertinence des logs (ciblage)
* Faciliter le téléversement des logs vers le support :
  * intégration dans le fichier « system »
  * ajout d’un bouton de téléchargement
* Mettre en place un outil de parsing des logs :
  * éviter de demander aux partenaires / clients de filtrer eux-mêmes
* Définir une procédure de recherche dans les logs :
  * mots-clés (ERROR, WARNING, etc.)
  * filtrage par date (plage, jour précis, etc.)

### TGU

* Vérifier si un TGU existe :
  * si absent, définir la procédure à suivre
* Documenter la procédure de création d’un TGU :
  * inclure l’ajout de tags côté support

### Patch

* Définir une règle pour éviter l’envoi de patchs sur un cloud public