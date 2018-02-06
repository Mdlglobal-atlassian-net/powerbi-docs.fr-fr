---
title: "Optimiser vos données Excel avec Questions et réponses dans Power BI"
description: "Optimiser vos données avec Questions et réponses dans Power BI"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 01/18/2018
ms.author: mihart
ms.openlocfilehash: 92d75bc3df3a3403f77fb350b4acfe1325e707d2
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2018
---
# <a name="how-to-make-your-excel-data-work-well-with-qa-in-power-bi"></a>Optimiser vos données Excel avec Questions et réponses dans Power BI
Si vous êtes chargé de créer des modèles de données ou des classeurs Excel qui seront utilisés avec Power BI, continuez votre lecture…

Dans Power BI, Q&R peut effectuer des recherches dans des données structurées et choisir la visualisation qui convient le mieux à votre question. C’est ce qui en fait un outil incontournable.   

Le moteur Questions et réponses peut être utilisé sur n’importe quel fichier Excel chargé contenant des tableaux, des plages ou un modèle PowerPivot. Toutefois, plus vous optimisez et nettoyez vos données, meilleures sont les performances du moteur.  Si vous prévoyez de partager des rapports et tableaux de bord basés sur votre jeu de données, vous voulez que vos collègues puissent facilement poser des questions et obtenir des réponses de qualité.

### <a name="how-qa-works-with-excel"></a>Fonctionnement de Questions et réponses avec Excel
Q&R présente des capacités de compréhension de base du langage naturel qui peuvent être utilisées sur l’ensemble de vos données. Il comprend une recherche par mot clé dépendante du contexte pour les noms de tables, colonnes et champs calculés Excel. Il a également une connaissance intégrée de la manière dont les données doivent être filtrées, triées, agrégées, regroupées et affichées. 

Par exemple, si vous disposiez d’un tableau Excel nommé « Ventes » comprenant les colonnes « Produits », « Mois », « Unités vendues », « Ventes brutes » et « Bénéfices », vous pourriez poser des questions sur l’une de ces entités.  Vous pourriez demander d’afficher les ventes, le total des bénéfices par mois, les produits triés par unités vendues, et ainsi de suite. Pour plus d’informations, découvrez les [types de question que vous pouvez poser](power-bi-q-and-a.md) et les [types de visualisation que vous pouvez spécifier dans une requête Questions et réponses](power-bi-visualization-types-for-reports-and-q-and-a.md).

### <a name="prepare-an-excel-dataset-for-qa"></a>Préparer un jeu de données Excel pour Questions et réponses
Q&R s’appuie sur les noms des tables, des colonnes et des champs calculés pour répondre aux questions spécifiques aux données. Le nom que vous attribuez à vos entités est donc important.

Voici quelques conseils pour tirer le meilleur parti de Q&R.

* Assurez-vous que vos données se trouvent dans un tableau Excel. Voici [comment créer un tableau Excel](https://support.office.com/article/Create-an-Excel-table-in-a-worksheet-e81aa349-b006-4f8a-9806-5af9df0ac664?ui=en-US&rs=en-US&ad=US).
* Assurez-vous que les noms des tables, des colonnes et des champs calculés sont explicites.
  
  Par exemple, si vous disposez d’une table qui contient des données de ventes, nommez-la « Ventes ». Les noms de colonnes tels que « Année », « Produit », « Commercial » et « Montant » vous permettront d’obtenir d’excellents résultats avec Q&R.

* si votre classeur contient un modèle de données Power Pivot, vous pouvez procéder à davantage d’optimisations. Pour plus d’informations, consultez cet article de notre équipe d’experts internes en langage naturel intitulé [Demystifying Power BI Q&A part 2 (Q&R : démystification de Power BI, partie 2)](http://blogs.msdn.com/b/powerbi/archive/2014/02/27/demystifying-power-bi-q-amp-a-part-2.aspx).

* Ouvrez le jeu de données dans Power BI Desktop et créez des colonnes, créez des mesures calculées, concaténez des champs pour créer des valeurs uniques, classez les données par type (par exemple, dates, chaînes, données géographiques, images, URL) et bien plus encore.

## <a name="next-steps"></a>Étapes suivantes
Revenir à [Q&R dans Power BI](power-bi-q-and-a.md)  
[Préparer des jeux de données locaux pour Questions et réponses](service-q-and-a-direct-query.md)   
[Démarrage rapide Questions et réponses](power-bi-visualization-introduction-to-q-and-a.md)  
[Obtenir des données (pour Power BI)](service-get-data.md)  

D’autres questions ? [Posez vos questions à la communauté Power BI](http://community.powerbi.com/)
