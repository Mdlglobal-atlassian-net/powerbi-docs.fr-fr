---
title: Contrôler l’utilisation de jeux de données dans des espaces de travail (préversion) - Power BI
description: Découvrez comment limiter le flux d’informations dans le locataire Power BI.
author: maggiesMSFT
ms.reviewer: chbraun
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 05/31/2019
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: d1ad29bebc148d9f30e8d22240dd149787251a0a
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83285437"
---
# <a name="control-the-use-of-datasets-across-workspaces-preview"></a>Contrôler l’utilisation de jeux de données dans des espaces de travail (préversion)

L’utilisation de jeux de données dans les espaces de travail constitue un moyen puissant de favoriser la culture et la vulgarisation des données au sein d’une organisation. Cependant, si vous êtes un administrateur Power BI, vous souhaitez parfois limiter le flux d’informations dans votre locataire Power BI. Avec le paramètre de locataire **Utiliser des jeux de données dans des espaces de travail**, vous pouvez limiter la réutilisation de jeu de données complètement ou partiellement par groupes de sécurité.

![Paramètres d’espace de travail d’administrateur Power BI](media/service-datasets-admin-across-workspaces/power-bi-admin-workspace-settings.png)

Si vous désactivez ce paramètre, voici les effets sur les créateurs de rapports :

- Le bouton pour copier des rapports sur les espaces de travail n’est pas disponible. 
- Dans un rapport basé sur un jeu de données partagé, le bouton **Modifier le rapport** n’est pas disponible.
- Dans le service Power BI, l’expérience de découverte affiche uniquement les jeux de données dans l’espace de travail actuel.
- Dans Power BI Desktop, l’expérience de découverte affiche uniquement les jeux de données d’espaces de travail desquels vous êtes membre.
- Dans Power BI Desktop, si les utilisateurs ouvrent un fichier .pbix avec une connexion active à un jeu de données en dehors des espaces de travail desquels ils sont membres, ils voient un message d’erreur leur demandant de se connecter à un jeu de données différent.

## <a name="provide-a-link-for-the-certification-process"></a>Fournir un lien pour le processus de certification

En tant qu’administrateur de locataire, vous pouvez fournir une URL pour le lien **En savoir plus** dans la page des paramètres **Approbation**.  Ce lien permet d’accéder à la documentation relative à votre processus de certification. Si vous n’indiquez aucune destination pour le lien **En savoir plus**, il pointe par défaut vers l’article sur la [certification de jeux de données](service-datasets-certify.md).

![En savoir plus sur la certification de jeux de données](media/service-datasets-certify-promote/power-bi-dataset-learn-more-certification.png)

## <a name="next-steps"></a>Étapes suivantes

- [Utiliser des jeux de données dans des espaces de travail (préversion)](service-datasets-across-workspaces.md)
- Des questions ? [Essayez d’interroger la communauté Power BI](https://community.powerbi.com/)
