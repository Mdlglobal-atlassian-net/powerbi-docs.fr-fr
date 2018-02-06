---
title: "Actualiser un jeu de données créé à partir d’un fichier Power BI Desktop - local"
description: "Actualiser un jeu de données créé à partir d’un fichier Power BI Desktop sur un lecteur local"
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
ms.openlocfilehash: f314e475d7a08ffe252144add1a887086a32a24d
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2017
---
# <a name="refresh-a-dataset-created-from-a-power-bi-desktop-file-on-a-local-drive"></a>Actualiser un jeu de données créé à partir d’un fichier Power BI Desktop sur un lecteur local
## <a name="whats-supported"></a>Qu’est-ce qui est pris en charge ?
Dans Power BI, les fonctionnalités Actualiser maintenant et Planifier l’actualisation sont prises en charge pour des jeux de données créés à partir de fichiers Power BI Desktop importés d’un lecteur local où Obtenir des données/Éditeur de requête est utilisé pour se connecter aux données des sources de données suivantes et pour les charger :

### <a name="power-bi-gateway---personal"></a>Power BI Gateway - Personal
* Toutes les sources de données en ligne affichées dans l’éditeur de requête et Obtenir des données dans Power BI Desktop.
* Toutes les sources de données locales affichées dans l’éditeur de requête et Obtenir des données dans Power BI Desktop, excepté pour HDFS (Hadoop Distributed File System) et Microsoft Exchange.

<!-- Refresh Data sources-->
[!INCLUDE [refresh-datasources](./includes/refresh-datasources.md)]

> [!NOTE]
> Une passerelle doit être installée et en cours d’exécution pour que Power BI puisse se connecter aux sources de données locales et actualiser le jeu de données.
> 
> 

Vous pouvez effectuer une actualisation manuelle unique des données directement dans Power BI Desktop en sélectionnant Actualiser dans le ruban Accueil. Lorsque vous sélectionnez Actualiser ici, les données du modèle du *fichier* sont actualisées avec les données mises à jour à partir de la source de données d’origine. Ce type d’actualisation, entièrement à partir de l’application Power BI Desktop elle-même, diffère d’une actualisation manuelle ou planifiée dans Power BI et il est important de comprendre cette différence.

![](media/refresh-desktop-file-local-drive/pbix-refresh.png)

Lorsque vous importez votre fichier Power BI Desktop à partir d’un lecteur local, les données, ainsi que d’autres informations sur le modèle sont chargées dans un jeu de données dans le service Power BI. Dans le service Power BI (pas dans Power BI Desktop), vous actualisez les données du jeu de données parce qu’il s’agit de ce sur quoi vos rapports sont basés dans le service Power BI. Étant donné que les sources de données sont externes, vous pouvez actualiser manuellement le jeu de données à l’aide de la commande **Actualiser maintenant**, ou configurer une planification de l’actualisation à l’aide de la commande **Planifier l’actualisation**.

Lorsque vous actualisez le jeu de données, Power BI ne se connecte pas au fichier sur le lecteur local pour interroger les données mises à jour. Il utilise les informations du jeu de données pour se connecter directement aux sources de données afin d’interroger les données mises à jour qu’il charge ensuite dans le jeu de données.

> [!NOTE]
> Les données actualisées dans le jeu de données ne sont pas à nouveau synchronisées dans le fichier sur le lecteur local.
> 
> 

## <a name="how-do-i-schedule-refresh"></a>Comment planifier l’actualisation ?
Lorsque vous configurez une planification de l’actualisation, Power BI se connecte directement aux sources de données en utilisant les informations de connexion et les informations d’identification du jeu de données pour interroger les données mises à jour, puis charger les données actualisées dans le jeu de données. Les visualisations des rapports et tableaux de bord basés sur ce jeu de données dans le service Power BI sont également mises à jour.

Pour plus d’informations sur la façon de planifier l’actualisation, consultez [Planifier l’actualisation](refresh-scheduled-refresh.md).

## <a name="when-things-go-wrong"></a>Quand des problèmes apparaissent
Quand des problèmes apparaissent, ceux-ci sont souvent dus au fait que Power BI ne parvient pas à se connecter aux sources de données ou, si le jeu de données se connecte à une source de données locale, que la passerelle est hors connexion. Veuillez donc vous assurer que Power BI peut se connecter aux sources de données. Si vous modifiez le mot de passe que vous utilisez pour vous connecter à une source de données ou que Power BI est déconnecté d’une source de données, essayez de vous reconnecter à vos sources de données dans Informations d’identification de la source de données.

Veillez à laisser l’option **M’envoyer une notification d’échec d’actualisation** activée. Vous voudrez en effet probablement être immédiatement informé en cas d’échec d’une actualisation planifiée.

## <a name="troubleshooting"></a>Résolution des problèmes
Parfois, l’actualisation des données peut ne pas fonctionner comme prévu. Cela est généralement dû à un problème avec une passerelle. Consultez les articles de résolution des problèmes de passerelle qui présentent des outils et les problèmes connus.

[Résolution des problèmes de passerelle de données locale](service-gateway-onprem-tshoot.md)

[Résolution des problèmes liés à Power BI Gateway - Personal](service-admin-troubleshooting-power-bi-personal-gateway.md)

D’autres questions ? [Essayez d’interroger la communauté Power BI](http://community.powerbi.com/)
