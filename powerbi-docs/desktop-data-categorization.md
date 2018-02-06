---
title: "Catégorisation des données dans Power BI Desktop"
description: "Catégorisation des données dans Power BI Desktop"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 733006c1fcec2b541e0f2e3011f4c1f631608698
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2017
---
# <a name="data-categorization-in-power-bi-desktop"></a>Catégorisation des données dans Power BI Desktop
Dans **Power BI Desktop**, vous pouvez spécifier la catégorie de données pour une colonne pour que Power BI Desktop sache comment traiter ses valeurs dans une visualisation.

Quand Power BI Desktop importe des données, il obtient non seulement les données proprement dites, mais également des informations telles que les noms de la table et de la colonne, s’il s’agit d’une clé primaire, et ainsi de suite.  Avec ces informations, Power BI Desktop émet des hypothèses pour vous procurer la meilleure expérience par défaut lors de la création d’une visualisation. 

Voici un exemple : quand Power BI Desktop détecte qu’une colonne contient des valeurs numériques, il en déduit que vous souhaiterez probablement les agréger d’une façon ou d’une autre. Il la place donc dans la zone Valeurs. Pour une colonne avec des valeurs de date et d’heure, il part du principe que vous l’utiliserez probablement comme axe de hiérarchie de temps sur un graphique en courbes.

Cependant, certains cas sont un peu plus complexes, comme quand il s’agit de géographie. Examinez le tableau suivant tiré d’une feuille de calcul Excel :

![](media/desktop-data-categorization/datacategorizationtable.png)

Power BI Desktop doit-il considérer les codes de la colonne Geocode comme l’abréviation d’un pays ou d’un état ?  Cela n’est pas évident, car un code comme celui-ci peut signifier l’un ou l’autre.  Par exemple, AL peut signifier Alabama ou Albanie, AR peut signifier Arkansas ou Argentine, et CA peut signifier Californie ou Canada. Cela a son importance quand nous dessinons notre champ Geocode sur une carte.  Power BI Desktop doit-il afficher une carte du monde avec les pays en surbrillance ou une carte des États-Unis avec les états en surbrillance ?  Vous pouvez spécifier une catégorie de données pour les données comme celles-ci. La catégorisation des données affine les informations que Power BI Desktop peut utiliser pour fournir les meilleures visualisations.  

**Pour spécifier une catégorie de données**

1. Dans la vue Rapport ou Données, dans la liste **Champs** , sélectionnez le champ que vous souhaitez trier selon une catégorisation différente.
2. Dans le ruban, sous l’onglet **Outils de données, Modélisation** , cliquez sur la liste déroulante **Catégorie des données** .  Cela affiche la liste des catégories de données que vous pouvez choisir pour votre colonne.  Certaines options peuvent être désactivées si elles ne fonctionneront pas avec le type de données actuel de votre colonne.  Par exemple, si une colonne est un type de données binaires, Power BI Desktop ne vous autorise pas à choisir des catégories de données géographiques. 

![](media/desktop-data-categorization/datacategorization.gif)

C’est tout.  Tout comportement normalement applicable à un élément visuel fonctionnera désormais automatiquement.  

Vous pouvez également être intéressé par le [filtrage géographique pour les applications mobiles Power BI](desktop-mobile-geofiltering.md).
