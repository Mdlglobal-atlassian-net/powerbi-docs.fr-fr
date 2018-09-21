---
title: Scanner un code-barres depuis l’application Power BI sur un iPhone
description: Scannez des codes-barres dans le monde réel pour accéder directement à des informations décisionnelles filtrées dans l’application mobile Power BI.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-mobile
ms.topic: conceptual
ms.date: 10/13/2017
ms.author: maggies
ms.openlocfilehash: 42ba9b042209dfd717c58042834e8d7966f97ecf
ms.sourcegitcommit: 67336b077668ab332e04fa670b0e9afd0a0c6489
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44732585"
---
# <a name="scan-a-barcode-with-your-iphone-from-the-power-bi-mobile-app"></a>Scanner un code-barres depuis l’application Power BI sur votre iPhone
Scannez des codes-barres dans le monde réel pour accéder directement à des informations décisionnelles filtrées dans l’application mobile Power BI.

![](media/mobile-apps-scan-barcode-iphone/power-bi-barcode-scanner.png)

Supposons qu’un collègue ait [marqué un champ de code-barres dans un rapport Power BI Desktop](../../desktop-mobile-barcodes.md) et partagé le rapport avec vous. 

Quand vous scannez un code-barres de produit avec le scanner de l’application Power BI de votre iPhone, vous voyez le rapport (ou une liste de rapports) avec ce code-barres. Vous pouvez ouvrir ce rapport, filtré selon ce code-barres, sur votre iPhone.

## <a name="scan-a-barcode-with-the-power-bi-scanner"></a>Scanner un code-barres avec le scanner de Power BI
1. Dans l’application mobile Power BI, ouvrez le menu de navigation principal ![](media/mobile-apps-scan-barcode-iphone/pbi_iph_navmenu.png) dans le coin supérieur gauche. 
2. Recherchez le **scanner** et sélectionnez-le. 
   
    ![](media/mobile-apps-scan-barcode-iphone/power-bi-scanner.png)
3. Si votre appareil photo n’est pas activé, vous devez autoriser l’application Power BI à l’utiliser. Il s’agit d’une autorisation à usage unique. 
4. Pointez le scanner sur un code-barres de produit. 
   
    Vous pouvez voir une liste des rapports associés à ce code-barres.
5. Appuyez sur le nom du rapport pour l’ouvrir sur votre iPhone, automatiquement filtré selon ce code-barres.

## <a name="filter-by-other-barcodes-while-in-a-report"></a>Filtrer selon d’autres codes-barres dans un rapport
Lors de la consultation sur votre iPhone d’un rapport filtré selon un code-barres, vous pouvez filtrer ce rapport en fonction d’un autre code-barres.

* Si l’icône de code-barres contient un filtre ![](media/mobile-apps-scan-barcode-iphone/power-bi-barcode-filtered-icon-black.png), cela signifie que le filtre est actif et que le rapport est déjà filtré selon un code-barres. 
* Si l’icône de code-barres ne contient pas de filtre ![](media/mobile-apps-scan-barcode-iphone/power-bi-barcode-unfiltered-icon.png), cela signifie que le filtre est inactif et que le rapport n’a pas été filtré selon un code-barres. 

Dans ces deux cas, appuyez sur l’icône pour ouvrir un petit menu avec un scanner flottant.

* Dirigez le scanner sur le nouvel élément pour modifier la valeur de code-barres du filtre du rapport. 
* Sélectionnez **Effacer le filtre à code-barres** pour rétablir le rapport non filtré.
* Sélectionnez **Filtrer par codes-barres récents** pour remplacer le filtre du rapport par l’un des codes-barres que vous avez scannés durant la session active.

## <a name="issues-with-scanning-a-barcode"></a>Problèmes lors de la lecture d’un code-barres
Les messages suivants peuvent s’afficher quand vous scannez le code-barres d’un produit.

### <a name="couldnt-filter-report"></a>« Impossible de filtrer le rapport... »
Le rapport à filtrer est basé sur un modèle de données qui ne comprend pas cette valeur de code-barres. Par exemple, le produit « eau minérale » n’est pas inclus dans le rapport.  

### <a name="allsome-of-the-visuals-in-the-report-dont-contain-any-value"></a>Tous/certains éléments visuels du rapport ne contiennent aucune valeur
La valeur de code-barres que vous avez scannée existe dans votre modèle, mais tous/certains éléments visuels de votre rapport ne contiennent pas cette valeur et, par conséquent, le filtrage va renvoyer un état vide. Essayez de consulter d’autres pages du rapport ou modifiez vos rapports dans Power BI Desktop afin qu’ils contiennent cette valeur. 

### <a name="looks-like-you-dont-have-any-reports-that-can-be-filtered-by-barcodes"></a>« Apparemment, vous n’avez aucun rapport pouvant être filtré par code-barres. »
Cela signifie que vous n’avez aucun rapport prenant en charge les codes-barres. Le scanner de codes-barres peut filtrer uniquement les rapports qui possèdent une colonne marquée **Code-barres**.  

Vérifiez que vous ou le propriétaire du rapport avez marqué une colonne **Code-barres** dans Power BI Desktop. En savoir plus sur [le marquage d’un champ de code-barres dans Power BI Desktop](../../desktop-mobile-barcodes.md)

### <a name="couldnt-filter-report---looks-like-this-barcode-doesnt-exist-in-the-report-data"></a>« Impossible de filtrer le rapport - Il semble que ce code-barres n’existe pas dans les données du rapport. »
Le rapport que vous avez choisi de filtrer est basé sur un modèle de données qui ne comprend pas cette valeur de code-barres. Par exemple, le produit « eau minérale » n’est pas inclus dans le rapport. Vous pouvez scanner un autre produit, choisir un autre rapport (si plusieurs rapports sont disponibles) ou afficher le rapport sans filtrage. 

## <a name="next-steps"></a>Étapes suivantes
* [Marquer un champ de code-barres dans Power BI Desktop](../../desktop-mobile-barcodes.md)
* [Vignettes d’un tableau de bord dans Power BI](../../service-dashboard-tiles.md)
* [Tableaux de bord dans Power BI](../../service-dashboards.md)
