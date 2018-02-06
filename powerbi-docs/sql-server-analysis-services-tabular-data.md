---
title: "Données actives SQL Server Analysis Services dans Power BI"
description: "Données actives SQL Server Analysis Services dans Power BI. Cela s’effectue grâce à une source de données configurée pour une passerelle d’entreprise."
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 08/10/2017
ms.author: maghan
ms.openlocfilehash: a2a0b2ae9f663f5bd2ba1c599f4f55232c0d1973
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2018
---
# <a name="sql-server-analysis-services-live-data-in-power-bi"></a>Données actives SQL Server Analysis Services dans Power BI
Dans Power BI, vous disposez de deux méthodes pour vous connecter à des données actives provenant d’un serveur SQL Server Analysis Services. Dans **Obtenir des données**, vous pouvez vous connecter à un serveur SQL Server Analysis Services ou vous connecter à un [fichier Power BI Desktop](service-desktop-files.md) ou à un [classeur Excel](service-excel-workbook-files.md) qui est déjà connecté à un serveur Analysis Services.

 >[!IMPORTANT]
 >* Pour que vous puissiez vous connecter à un serveur Analysis Services en ligne, une passerelle de données locale doit être installée et configurée par un administrateur. Pour plus d’informations, consultez [Passerelle de données locale](service-gateway-onprem.md).
 >* Quand vous utilisez la passerelle, vos données restent locales.  Les rapports que vous créez à partir de ces données sont enregistrés dans le service Power BI. 
 >* [Les requêtes en langage naturel dans Q&R](service-q-and-a-direct-query.md) sont actuellement en version préliminaire pour les connexions actives Analysis Services.

## <a name="to-connect-to-a-model-from-get-data"></a>Pour se connecter à un modèle via Obtenir des données
1. Dans **Mon espace de travail**, sélectionnez **Obtenir des données**. Vous pouvez également sélectionner un espace de travail de groupe, s’il y en a de disponible.
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdatabutton.png)
2. Sélectionnez **Bases de données et plus**.
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_1.png)
3. Sélectionnez **SQL Server Analysis Services** > **Se connecter**. 
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_2.png)
4. Sélectionnez un serveur. Si vous ne voyez aucun des serveurs répertoriés ici, cela signifie qu’une passerelle ou une source de données n’a pas été configurée, ou que votre compte n’est pas répertorié sous l’onglet **Utilisateurs** de la source de données, dans la passerelle. Consultez votre administrateur.
5. Sélectionnez le modèle auquel vous voulez vous connecter. Il peut être tabulaire ou multidimensionnel.

Une fois que vous êtes connectez au modèle, il apparaît dans votre site Power BI, dans **Mon espace de travail/Jeux de données**. Si vous êtes passé à un espace de travail de groupe, le jeu de données s’affiche dans le groupe.

![](media/sql-server-analysis-services-tabular-data/connecttoas_dataset_5.png)

## <a name="dashboard-tiles"></a>Vignettes d’un tableau de bord
Si vous épinglez des éléments visuels d’un rapport dans le tableau de bord, les vignettes épinglées sont automatiquement actualisées toutes les 10 minutes. Si les données de votre serveur local Analysis Services sont mises à jour, les vignettes sont mises à jour automatiquement après 10 minutes.

## <a name="next-steps"></a>Étapes suivantes
[Passerelle de données locale](service-gateway-onprem.md)  
[Gérer les sources de données Analysis Services](service-gateway-enterprise-manage-ssas.md)  
[Résolution des problèmes de passerelle de données locale](service-gateway-onprem-tshoot.md)  
D’autres questions ? [Posez vos questions à la communauté Power BI](http://community.powerbi.com/)
