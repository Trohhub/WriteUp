# NoLimitSecu WriteUp
**Table of contents**
- [NoLimitSecu WriteUp](#nolimitsecu-writeup)
  - [Octobre 2023](#octobre-2023)
    - [CVE-2023-20198](#cve-2023-20198)
  - [Mai 2023](#mai-2023)
    - [Retex gestion de crise](#retex-gestion-de-crise)

## Octobre 2023
### CVE-2023-20198
Le podcast de NoLimitSecu sur la vulnérabilité CVE-2023-20198 se concentre sur une faille critique dans le logiciel Cisco IOS XE. Cette vulnérabilité, exploitée activement dans la nature, permet une élévation de privilèges non authentifiée via l'interface Web, donnant à un attaquant un accès administratif complet (niveau 15). Une fois ce niveau d'accès obtenu, l'attaquant peut prendre le contrôle total de l'appareil.

La découverte de cette faille a été annoncée par Cisco le 16 octobre 2023, après avoir identifié une activité suspecte liée à la création de comptes utilisateurs non autorisés et l'injection de configurations malveillantes. L'exploit a été observé pour la première fois le 18 septembre 2023.

En réponse à cette vulnérabilité, Cisco a recommandé de désactiver l'accès HTTP/S à l'interface Web de IOS XE ou de limiter cet accès à des sources de confiance via des listes de contrôle d'accès (ACL) jusqu'à la publication de correctifs appropriés.

Par ailleurs, une seconde vulnérabilité (CVE-2023-20273) a été identifiée, permettant l'injection de commandes et l'exécution de code arbitraire avec les privilèges root, ce qui a été utilisé en combinaison avec CVE-2023-20198 pour installer des implants malveillants sur les appareils compromis.

Pour plus de détails, vous pouvez consulter les analyses approfondies sur les sites de Tenable et Cato Networks, ainsi que sur le blog de Cisco Talos qui documente les observations faites durant l'enquête sur les appareils compromis.
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