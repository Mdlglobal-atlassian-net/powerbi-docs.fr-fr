---
title: "Se connecter à Microsoft Azure Consumption Insights avec Power BI"
description: Microsoft Azure Consumption Insights pour Power BI
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggies
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 99f6f4b9159e2ab7261ab179811154ee2ef4929e
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-microsoft-azure-consumption-insights-with-power-bi"></a>Se connecter à Microsoft Azure Consumption Insights avec Power BI
Explorez et analysez vos données de consommation de Microsoft Azure dans Power BI avec le pack de contenu de Power BI. Les données sont actualisées automatiquement une fois par jour.

Connectez-vous au [Pack de contenu d’informations sur la consommation de Microsoft Azure](https://app.powerbi.com/getdata/services/azureconsumption) pour Power BI.

## <a name="how-to-connect"></a>Comment se connecter
1. Sélectionnez **Obtenir des données** en bas du volet de navigation gauche.
   
    ![](media/service-connect-to-azure-consumption-insights/getdata.png)
2. Dans la zone **Services**, sélectionnez **Obtenir**.
   
   ![](media/service-connect-to-azure-consumption-insights/services.png)
3. Sélectionnez **Microsoft Azure Consumption Insights** (informations sur la consommation de Microsoft Azure) \> **Obtenir**. 
   
   ![](media/service-connect-to-azure-consumption-insights/mazureconsumption.png)
4. Spécifiez le nombre de mois de données à importer ainsi que votre numéro d’inscription Azure Enterprise. Consultez les détails sur la [recherche de ces paramètres](#FindingParams) ci-dessous.
   
    ![](media/service-connect-to-azure-consumption-insights/azureconsumptionparams.png)
5. Fournissez votre clé d’accès pour la connexion. La clé de votre inscription figure dans votre portail Azure EA. 
   
    ![](media/service-connect-to-azure-consumption-insights/msazureconsumptioncreds.png)
6. Le processus d’importation démarre automatiquement. Une fois terminé, de nouveaux tableau de bord, rapport et modèle apparaîtront dans le volet de navigation. Sélectionnez le tableau de bord pour afficher vos données importées.
   
   ![](media/service-connect-to-azure-consumption-insights/msazureconsumptiondashboard.png)

**Et maintenant ?**

* Essayez de [poser une question dans la zone Q&R](service-q-and-a.md) en haut du tableau de bord.
* [Modifiez les vignettes](service-dashboard-edit-tile.md) dans le tableau de bord.
* [Sélectionnez une vignette](service-dashboard-tiles.md) pour ouvrir le rapport sous-jacent.
* Même si une actualisation quotidienne de votre jeu de données est planifiée, vous pouvez modifier la planification de l’actualisation ou essayer d’actualiser le jeu de données sur demande à l’aide de l’option **Actualiser maintenant**.

## <a name="whats-included"></a>Ce qui est inclus
Le Pack de contenu d’informations sur la consommation de Microsoft Azure contient des données de rapports mensuelles correspondant à la plage de mois indiquée pendant le flux de connexion. La plage est dynamique, ce qui signifie que les dates incluses sont mises à jour quand le jeu de données est actualisé.

## <a name="system-requirements"></a>Configuration requise
Le pack de contenu exige l’accès aux fonctionnalités d’entreprise dans le portail Azure. 

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Recherche de paramètres
Les rapports Power BI sont disponibles pour les clients directs, les partenaires et les clients indirects d’EA qui sont en mesure d’afficher des informations de facturation. Pour plus d’informations sur la recherche de chacune des valeurs qu’attend le flux de connexion, lisez ci-dessous.

**Nombre de mois**

* Il doit s’agir d’un nombre compris entre 1 et 36, correspondant au nombre de mois de données (à partir d’aujourd’hui) que vous souhaitez importer.

**Numéro d’inscription**

* Il s’agit du numéro d’inscription à Azure Enterprise qui se trouve sur l’écran d’accueil d’[Azure Enterprise Portal](https://ea.azure.com/) sous les détails de l’inscription.
  
    ![](media/service-connect-to-azure-consumption-insights/params2.png)

**Clé d’accès**

* Votre clé est disponible sur le portail Azure Enterprise, sous « Télécharger l’utilisation » > « Clé d’accès API »
  
    ![](media/service-connect-to-azure-consumption-insights/creds2.png)

**Aide supplémentaire**

* Pour obtenir de l’aide supplémentaire sur la configuration du pack de contenu Azure Enterprise pour Power BI, connectez-vous à Azure Enterprise Portal pour afficher le fichier d’aide de l’API sous Aide. Vous trouverez des instructions supplémentaires sous Rapports -> Télécharger l’utilisation -> Clé d’accès API. 

## <a name="next-steps"></a>Étapes suivantes
[Prise en main de Power BI](service-get-started.md)

[Obtenir des données dans Power BI](service-get-data.md)
