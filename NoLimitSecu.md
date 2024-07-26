# NoLimitSecu WriteUp
**Table of contents**
- [NoLimitSecu WriteUp](#nolimitsecu-writeup)
  - [Octobre 2023](#octobre-2023)
    - [CVE-2023-20198](#cve-2023-20198)
  - [Mai 2023](#mai-2023)
    - [Retex gestion de crise](#retex-gestion-de-crise)

## Octobre 2023
### CVE-2023-20198

- #### Qu'elle est cette faille ?
La CVE-2023-20198 utilise sur une faille critique dans Cisco IOS XE. Cette vulnérabilité, permet une élévation de privilèges non authentifiée via l'interface Web, donnant à un attaquant un accès administratif de niveau 15. Pour faire plus simple, l'attaquant injecte du code ce qui créer un utilisateur avec les droits adnimistrateur et une fois ce niveau d'accès obtenu, l'attaquant peut prendre le contrôle total de l'appareil.

- #### Niveau privilège IOS de Cisco
**Niveau 0 (User EXEC Mode) :**

- Accès très limité.
- Seules quelques commandes de base sont disponibles, comme logout, enable, disable, exit, et help.

**Niveau 1 (User EXEC Mode) :**

- Niveau par défaut pour les utilisateurs.
- Accès limité aux commandes de base de diagnostic et de connectivité, telles que ping, traceroute, et show.

**Niveau 15 (Privileged EXEC Mode) :**

- Accès complet à toutes les commandes de configuration et de gestion.
- Les utilisateurs peuvent entrer en mode de configuration globale et modifier la configuration du système.
  
Les niveaux de privilège intermédiaires (2 à 14) peuvent être personnalisés

- #### Quand ?

La découverte de cette faille a été annoncée par Cisco le 16 octobre 2023, après avoir identifié une activité suspecte liée à la création de comptes utilisateurs non autorisés et l'injection de configurations malveillantes. L'exploit a été observé pour la première fois le 18 septembre 2023. 

- #### Les dégats ?

Le premiers scan effectuer par Cisco Talos à analysé plus de 53.000 borne cisco compromis dans le monde, et lors d'un second scan plusieurs heures plutard 8.000 en plus s'y son rajouté. Et tout cela a été l'oeuvre d'un seul individu, en tout cas au début avant l'exposition de la faille Zero Day.

 - #### Réponse ?

Suite à sa Cisco a recommandé de désactiver l'accès HTTP/HTTPS à l'interface Web de IOS XE ou de limiter cet accès à des sources de confiance via des listes de contrôle d'accès jusqu'à la publication de patch le 22 octobre 2023. Cisco a publié la mise à jour 17.9.4a pour les systèmes utilisant IOS XE. Par la suite, des mises à jour pour d'autres versions, notamment 17.6.6a et 16.12.10a, ont également été déployées.

## Mai 2023
### Retex gestion de crise

Le podcast met en avant Stéphane Lenco, qui partage son retour d'expérience sur la gestion d'une crise cyber chez Thales, suite à une attaque par le ransomware LockBit. Il détails les étapes de la gestion de cette crise et les leçons apprises pour améliorer les réponses futures aux incidents de cybersécurité.

- #### Identification de la Crise :

Lenco explique l'importance de la détection précoce des incidents. Lors de l'attaque, l'équipe de Thales a rapidement identifié des anomalies dans le système, ce qui a permis de réagir promptement.

- #### Réponse Immédiate :

La première étape a été de contenir la menace. Cela incluait l'isolement des systèmes affectés pour empêcher la propagation du ransomware. Lenco insiste sur la nécessité d'avoir des procédures claires et préétablies pour ce type de situations.

- #### Communication :

Un aspect crucial de la gestion de crise est la communication efficace, tant en interne qu'en externe. Lenco décrit comment Thales a maintenu une communication constante avec les parties prenantes, y compris les clients, les employés et les autorités régulatrices.

- #### Analyse et Apprentissage :

Après avoir géré la crise immédiate, l'équipe a effectué une analyse approfondie pour comprendre les failles exploitées. Lenco souligne l'importance de tirer des leçons de chaque incident pour améliorer les défenses futures et éviter des récurrences.

- #### Formation et Préparation :

Un autre point clé mentionné par Lenco est l'importance de la formation et des exercices réguliers de simulation de crise. Ces exercices permettent aux équipes de se préparer et de réagir plus efficacement en cas de véritable incident.

- #### Collaboration Externe :

Lenco évoque aussi la nécessité de collaborer avec des experts externes, notamment des consultants en cybersécurité et des forces de l'ordre, pour une réponse plus complète et coordonnée.