# Certification CPiN

## Introduction

## QCM

## Cas pratiques

Le but de cette partie est d'évaluer les compétences du candidats sur la manipulation de l'offre CPiN à travers différents exercices correspondant à des cas d'usages usuels.

L'ensemble des exercices se fait sur les environnements OVH.

### CAS 1 : Déployer une application simple (1 point)

#### Présentation

Ce Labs permet de vérifier la capacité du candidat à déployer une application simple depuis la console CPiN via fichiers manifests déjà existants.

Détail de l'application :

 - Un backend en Java qui expose une API REST
 - Une base de données postgres

Objectifs :
 - Utilisation de la console et des différents services offerts par CPiN
 - Construire et déployer une application "simple" sur CPiN

#### Exercice

Créer un projet sur la console préfixé par "crt-" puis vos initiales. Ajouter les examinateurs avec des droits de lecture sur le projet et les environnements créés.

Ajouter les repos de code suivants (en faire un fork ou créer une branche dédié du type : "certification/nom_candidat")

 - Repo applicatif : https://github.com/cloud-pi-native/tuto-java
 - Repo infra : https://github.com/cloud-pi-native/tuto-java-infra-manifest

Construire l'image backend et ajuster la partie infrastrucrure pour déployer à partir de déjà existants :
 - un ingress sur une URL conforme à DSO sur OVH
 - un service
 - un déploiement pour l'application Java

> Demander aux examinateurs de confirmer le bon déploiement avant de passer à la suite. La confirmation se fait via l'URL :

https://<MON_DOMAINE>/api/demo/demo

### CAS 2 : SOPS (1 point)

#### Présentation

Ce lab permet de vérifier la capacité du candidat à traiter les éléments de type secret dans une approche gitops

Objectifs:
 - Utilisation de la console et des services proposés par CPiN
 - Utilisation de SOPS

#### Exercice

Utiliser SOPS pour créer un secret contenant l'utilisateur et le mot de passe de la base de données puis modifier le deploiement pour utiliser ce secret à la place des variables en dur du déploiement.

Rappel de documentation : 
 - gestion des secrets : https://cloud-pi-native.fr/guide/secrets-management.html
 - documentation interne projet : https://gitlab.apps.dso.numerique-interieur.com/forge-mi/transverse/documentation-dso-projets-interne

> Demander aux examinateurs de confirmer la bonne modification des secrets. 

> une fois validé, supprimer l'environnement créé ainsi que le repo d'infra pour éviter les collisions dans la suite des labs.

### CAS 3 : Corriger un chart HELM d'exemple (3 points)

#### Présentation

Ce lab permet de vérifier la capacité du candidat à traiter des problèmes remontés par un projet.

Objectifs:
 - Utilisation de la console et des services proposés par CPiN
 - Analyse de différentes erreurs et logs
 - Debug de deploiement applicatifs

### Exercice

Ajouter le repo contenant le chart HELM : https://github.com/cloud-pi-native/helm-cert (en faire un fork ou créer une branche dédié du type : "certification/nom_candidat") et l'intégrer à son projet CPiN.

Créer un nouvel environnement nommé lab2 de type small pour débuter ce lab.

Corriger **le chart helm et le repo applicatif** correspondant pour déployer convenablement l'application.

> Demander aux examinateurs de confirmer le bon déploiement avant de passer à la suite. La confirmation se fait via l'URL :

https://<MON_DOMAINE>/api/demo/demo



