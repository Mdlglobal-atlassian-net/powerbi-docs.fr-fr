---
title: "Créer un segment réactif que vous pouvez redimensionner dans Power BI"
description: "Découvrez comment créer un segment réactif que vous pouvez redimensionner pour l’ajuster à votre rapport"
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 12/08/2017
ms.author: maggies
ms.openlocfilehash: f95f126cc6a7c95fbe3227b712281a7d3f81e320
ms.sourcegitcommit: b780b7108fd9b52398b8377b52836f0e0fedc96e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2017
---
# <a name="create-a-responsive-slicer-you-can-resize-in-power-bi-preview"></a>Créer un segment réactif que vous pouvez redimensionner dans Power BI (Preview)

Les segments réactifs peuvent être redimensionnés de manière à s’ajuster à n’importe quel emplacement de votre rapport. Vous pouvez redimensionner les segments réactifs à la taille et la forme de votre choix (horizontal, carré, vertical). Les valeurs qu’ils contiennent sont réorganisées au fur et à mesure. Dans Power BI Desktop et dans le service Power BI, vous pouvez rendre réactifs des segments horizontaux et des segments date/plage. L’amélioration des zones tactiles des segments de date/plage permet de les modifier rapidement. Vous pouvez choisir la taille des segments réactifs. Ils se redimensionnent également de manière automatique sur les rapports du service Power BI ainsi que dans les applications mobiles Power BI. 

![Les segments réactifs peuvent prendre différentes formes](media/power-bi-slicer-filter-responsive/responsive-slicer-gif.gif)

## <a name="create-a-slicer"></a>Création d’un segment

Pour créer un segment dynamique, la première étape consiste à créer un segment de base. 

1. Dans le volet **Visualisations**, sélectionnez l’icône ![Segment](media/power-bi-slicer-filter-responsive/power-bi-slicer-icon.png) **icône Segment**.
2. Faites glisser le champ sur lequel effectuer le filtrage vers la zone **Champ**.

    ![Ajouter un champ au segment](media/power-bi-slicer-filter-responsive/power-bi-slicer-field.png)

## <a name="convert-to-a-horizontal-slicer"></a>Convertir en segment horizontal

1. Une fois le segment sélectionné, dans le volet **Visualisations**, sélectionnez l’onglet **Format**.
2. Développez la section **Général**, puis pour **Orientation**, sélectionnez **Horizontal**.

    ![Définir le segment sur horizontal](media/power-bi-slicer-filter-responsive/power-bi-slicer-horizontal.png) 

1.  Vous pouvez l’agrandir de manière à afficher plus de valeurs.

     ![Agrandir le segment](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-horizontal.png)

## <a name="make-it-responsive-and-experiment-with-it"></a>Rendre un segment réactif et le tester

Cette étape est facile. 

1. Juste en dessous de l’option **Orientation**, dans la section **Général** de l’onglet **Format**, définissez **Réactif (Preview)** sur **Activé**.  

    ![Le segment est désormais réactif](media/power-bi-slicer-filter-responsive/power-bi-slicer-wide-responsive.png)

1. Vous pouvez ensuite faire quelques essais. Faites glisser les angles pour modifier la taille et la largeur. S’il est suffisamment petit, il se transforme en simple icône de filtre.

    ![Segment réactif à la taille minimale, représenté par une icône de filtre](media/power-bi-slicer-filter-responsive/power-bi-slicer-small-filter-icon.png)

## <a name="add-it-to-a-phone-report-layout"></a>Ajouter le segment à une disposition de rapport sur téléphone

Dans Power BI Desktop, vous pouvez créer une disposition de téléphone pour chaque page d’un rapport. Si une page possède une disposition de téléphone, elle s’affiche sur un téléphone mobile en mode portrait. Sinon, vous devez la consulter en mode paysage. 

1. Dans le menu **Affichage**, sélectionnez **Mode téléphone**.

     ![Icône Mode téléphone, menu Affichage](media/power-bi-slicer-filter-responsive/power-bi-phone-layout-menu.png)
    
1. Faites glisser les éléments visuels à inclure dans le rapport de téléphone vers la grille. Lorsque vous faites glisser le segment réactif, donnez-lui la taille souhaitée (dans cet exemple, une simple icône de filtre).

    ![Ajouter le segment à la disposition de rapport sur téléphone](media/power-bi-slicer-filter-responsive/power-bi-slicer-phone-layout.png)

Consultez davantage d’informations sur la création de [rapports optimisés pour les applications mobiles Power BI](desktop-create-phone-report.md).

## <a name="make-a-time-or-range-slicer-responsive"></a>Rendre réactif un segment d’heure ou de plage

Vous pouvez suivre la même procédure pour rendre une vignette ou un segment de plage réactif. Après avoir défini **Réactif** sur **Activé**, vous allez remarquer les modifications suivantes :

- Les éléments visuels optimisent l’ordre des zones d’entrée en fonction de la taille autorisée sur le canevas. 
- L’affichage des éléments de données est modifié de manière à optimiser l’utilisation du segment, en fonction de la taille qui lui est réservée sur le canevas. 
- De nouvelles poignées rondes sur les curseurs permettent d’optimiser les interactions tactiles. 
- Lorsqu’un élément visuel devient trop petit pour être utile, il se transforme en icône représentant le type d’élément visuel. Il suffit d’un double-clic pour l’ouvrir en mode focus et interagir avec lui. Vous réalisez ainsi un précieux gain de place sur la page de rapport, sans perdre la fonctionnalité.

## <a name="next-steps"></a>Étapes suivantes

- [Didacticiel : Segments dans le service Power BI](power-bi-visualization-slicers.md)
- D’autres questions ? [Essayez d’interroger la communauté Power BI](http://community.powerbi.com/)