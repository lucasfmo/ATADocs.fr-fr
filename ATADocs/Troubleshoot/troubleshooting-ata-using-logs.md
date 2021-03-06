---
# required metadata

title: Résolution des problèmes liés à ATA à l’aide des journaux ATA | Microsoft Advanced Threat Analytics
description: Décrit comment vous pouvez utiliser les journaux ATA pour résoudre les problèmes
keywords:
author: rkarlin
manager: stevenpo
ms.date: 04/28/2016
ms.topic: article
ms.prod: identity-ata
ms.service: advanced-threat-analytics
ms.technology: security
ms.assetid: b8ad5511-8893-4d1d-81ee-b9a86e378347

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: bennyl
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Résolution des problèmes liés à ATA à l’aide des journaux ATA
Les journaux ATA offrent un aperçu de ce que fait chaque composant ATA à un moment donné.

## Journaux de la passerelle ATA
Les journaux de la passerelle ATA sont situés dans un sous-dossier appelé **Logs**. Dans l’emplacement de l’installation par défaut, il se trouve ici : **C:\Program Files\Microsoft Advanced Threat Analytics\Gateway\Logs**.

La passerelle ATA dispose des journaux suivants :

-   **Microsoft.Tri.Gateway.log** : ce journal contient tout ce qui se produit dans la passerelle ATA (y compris les erreurs et la résolution).

    Utilisation principale : obtention de l’état général de toutes les opérations dans l’ordre chronologique dans lequel elles se sont produites.

-   **Microsoft.Tri.Gateway-Resolution.log** : ce journal contient les détails de la résolution des entités visibles dans le trafic par la passerelle ATA.

    Utilisation principale : examen des problèmes de résolution des entités.

-   **Microsoft.Tri.Gateway-Errors.log** : ce journal contient uniquement les erreurs interceptées par la passerelle ATA.

    Utilisation principale : exécution de vérifications d’intégrité et examen des problèmes qui doivent être mis en corrélation avec des heures spécifiques.

-   **Microsoft.Tri.Gateway-ExceptionStatistics.log** : ce journal regroupe l’ensemble des erreurs et exceptions similaires, et évalue leur nombre.
    Ce fichier est vide lors de chaque démarrage du service de la passerelle ATA et est mis à jour toutes les minutes.

    Utilisation principale : détermination d’éventuels nouveaux problèmes ou erreurs liés à la passerelle ATA ; comme les erreurs sont regroupées, il est plus facile de constater la présence d’un nouveau type d’erreur ou de problème.

> [!NOTE]
> Les trois premiers fichiers journaux ont une taille maximale de 50 Mo. Quand cette taille est atteinte, un nouveau fichier journal est ouvert et le précédent est renommé en « &lt;nom_fichier_origine&gt;-Archive-00000 » où le nombre augmente chaque fois qu’il est renommé.

### Journaux du centre ATA
Les journaux du centre ATA sont situés dans un sous-dossier appelé **Logs**. Dans l’emplacement de l’installation par défaut, il se trouve ici : **C:\Program Files\Microsoft Advanced Threat Analytics\Center\Logs**.

Le centre ATA dispose des journaux suivants :

-   **Microsoft.Tri.Center.log** : ce journal contient tout ce qui se produit dans le centre ATA (y compris les détections et les erreurs).

    Utilisation principale : obtention de l’état général de toutes les opérations dans l’ordre chronologique dans lequel elles se sont produites.

-   **Microsoft.Tri.Center-Detection.log** : ce journal contient uniquement les détails des détections du centre ATA.

    Utilisation principale : examen des problèmes de détection.

-   **Microsoft.Tri.Center-Errors.log** : ce journal contient uniquement les erreurs interceptées par le centre ATA.

    Utilisation principale : exécution de vérifications d’intégrité et examen des problèmes qui doivent être mis en corrélation avec des heures spécifiques.

-   **Microsoft.Tri.Center-ExceptionStatistics.log** : ce journal regroupe l’ensemble des erreurs et exceptions similaires, et évalue leur nombre.
    Ce fichier est vide lors de chaque démarrage du service du centre ATA et est mis à jour toutes les minutes.

    Utilisation principale : détermination d’éventuels nouveaux problèmes ou erreurs liés au centre ATA ; comme les erreurs sont regroupées, il est plus facile de constater la présence d’un nouveau type d’erreur ou de problème.

> [!NOTE]
> Les trois premiers fichiers journaux ont une taille maximale de 50 Mo. Quand cette taille est atteinte, un nouveau fichier journal est ouvert et le précédent est renommé en « &lt;nom_fichier_origine&gt;-Archive-00000 » où le nombre augmente chaque fois qu’il est renommé.

### Journaux de la console ATA
Les journaux de la console ATA (les journaux de l’API de gestion) sont situés dans un sous-dossier appelé **Logs**. Dans l’emplacement de l’installation par défaut, il se trouve ici : **C:\Program Files\Microsoft Advanced Threat Analytics\Center\Management\Logs**.

La console ATA dispose des journaux suivants :

-   **w3wp.log** : ce journal contient tout ce qui se produit dans le processus de gestion (IIS).


-   **w3wp-Errors.log** : ce journal contient uniquement les erreurs interceptées par le processus de gestion (IIS).


-   **8e75f9f1-ExceptionStatistics.log** : ce journal regroupe l’ensemble des erreurs et exceptions similaires, et évalue leur nombre.
    Ce fichier est vide lors de chaque démarrage du service de la passerelle et est mis à jour toutes les minutes.

    Utilisation principale : détermination d’éventuels nouveaux problèmes ou erreurs liés au centre ATA ; comme les erreurs sont regroupées, il est plus facile de constater la présence d’un nouveau type d’erreur ou de problème.

> [!NOTE]
> Les deux premiers fichiers journaux ont une taille maximale de 50 Mo. Quand cette taille est atteinte, un nouveau fichier journal est ouvert et le précédent est renommé en « &lt;nom_fichier_origine&gt;-Archive-00000 » où le nombre augmente chaque fois qu’il est renommé.

### Journaux de déploiement ATA
Les journaux de déploiement ATA (installation) sont situés dans le répertoire temp de l’utilisateur qui a installé le produit. Dans l’emplacement de l’installation par défaut, il se trouve ici : **C:\Users\Administrator\AppData\Local\Temp** (ou un répertoire au-dessus de %temp%).

Journaux de déploiement du centre ATA :

-   **Microsoft Advanced Threat Analytics Center_20150601104213.log** : ce journal répertorie les étapes du processus de déploiement du centre ATA.
Utilisation principale : suivi du processus de déploiement du centre ATA.

-   **Microsoft Advanced Threat Analytics Center_20150601104213_0_MongoDBPackage.log** : ce journal répertorie les étapes du processus de déploiement de MongoDB sur le centre ATA.
Utilisation principale : suivi du processus de déploiement de MongoDB.

-   **Microsoft Advanced Threat Analytics Center_20150601104213_1_MsiPackage.log** : ce fichier journal répertorie les étapes du processus de déploiement des fichiers binaires du centre ATA.
Utilisation principale : suivi du déploiement des fichiers binaires du centre ATA.

Journaux de déploiement de la passerelle ATA :

-   **Microsoft Advanced Threat Analytics Gateway_20151214014801.log** : ce journal répertorie les étapes du processus de déploiement de la passerelle ATA.
Utilisation principale : suivi du processus de déploiement de la passerelle ATA.

-   **Microsoft Advanced Threat Analytics Gateway_20151214014801_001_MsiPackage.log** : ce fichier journal répertorie les étapes du processus de déploiement des fichiers binaires de la passerelle ATA.
Utilisation principale : suivi du déploiement des fichiers binaires de la passerelle ATA.


<!--HONumber=Apr16_HO2-->


