---
title: "Gérer votre source de données - Importation/actualisation planifiée"
description: "Gestion de la passerelle de données locale et des sources de données associées. Cet article porte spécifiquement sur les sources de données qui peuvent être utilisées avec les fonctions d’importation et d’actualisation planifiée."
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
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 247d6ab4978a9e62573ba9fe2ee19d69fdd793a0
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2017
---
# <a name="manage-your-data-source---importscheduled-refresh"></a>Gérer votre source de données - Importation/actualisation planifiée
Une fois que vous avez installé la passerelle de données locale, vous devez ajouter des sources de données qui peuvent être utilisées avec la passerelle. Cet article examine comment travailler avec des passerelles et des sources de données utilisées pour l’actualisation planifiée, et non pas avec des connexions actives ou DirectQuery.

## <a name="download-and-install-the-gateway"></a>Télécharger et installer la passerelle
Vous pouvez télécharger la passerelle à partir du service Power BI. Sélectionnez **Téléchargements** > **Passerelle de données** ou accédez à la [page de téléchargement de la passerelle](https://go.microsoft.com/fwlink/?LinkId=698861).

![](media/service-gateway-enterprise-manage-scheduled-refresh/powerbi-download-data-gateway.png)

## <a name="add-a-gateway"></a>Ajouter une passerelle
Pour ajouter une passerelle, [téléchargez](https://go.microsoft.com/fwlink/?LinkId=698863) et installez la passerelle d’entreprise sur un serveur de votre environnement. Une fois la passerelle installée, elle apparaît dans les listes de passerelles sous **Gérer les passerelles**.

> [!NOTE]
> **Gérer les passerelles** n’apparaît pas si vous n’êtes pas administrateur d’au moins une passerelle. Pour cela, vous devez être ajouté en tant qu’administrateur ou installer et configurer une passerelle.
> 
> 

## <a name="remove-a-gateway"></a>Supprimez une passerelle
La suppression d’une passerelle entraîne celle de toutes les sources de données associées.  Elle entraîne également l’arrêt des éventuels tableaux de bord et rapports qui reposent sur ces sources de données.

1. Sélectionnez l’icône Engrenage ![](media/service-gateway-enterprise-manage-scheduled-refresh/pbi_gearicon.png) en haut à droite > **Gérer les passerelles**.
2. Passerelle > **Supprimer**
   
   ![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings7.png)

## <a name="add-a-data-source"></a>Ajouter une source de données
Pour ajouter une source de données, sélectionnez une passerelle, puis cliquez sur **Ajouter une source de données**, ou accédez à Passerelle > **Ajouter une source de données**.

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings1.png)

Vous pouvez ensuite sélectionner le **type de source de données** dans la liste. Toutes les sources de données répertoriées peuvent être utilisées à des fins d’actualisation planifiée avec la passerelle d’entreprise. Vous pouvez utiliser Analysis Services, SQL Server et SAP HANA pour l’actualisation planifiée ou des connexions actives/DirectQuery.

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings2.png)

Vous devez ensuite renseigner les informations relatives à la source de données, notamment les informations sur la source et les informations d’identification utilisées pour accéder à la source de données.

> [!NOTE]
> Toutes les requêtes à la source de données sont exécutées à l’aide de ces informations d’identification. Pour plus d’informations, consultez l’article sur la passerelle de données locale principale qui indique la façon dont les [informations d’identification](service-gateway-onprem.md#credentials) y sont stockées.
> 
> 

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings3-oracle.png)

Vous pouvez cliquer sur **Ajouter** après avoir renseigné toutes les informations.  Vous pouvez à présent utiliser cette source de données pour l’actualisation planifiée avec vos données locales. L’indication *Connexion réussie* apparaît une fois la connexion établie.

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings4.png)

<!-- Shared Install steps Include -->
[!INCLUDE [gateway-onprem-datasources-include](./includes/gateway-onprem-datasources-include.md)]

### <a name="advanced-settings"></a>Paramètres avancés
Vous pouvez configurer le niveau de confidentialité de votre source de données pour contrôler le mélange (« mashup ») des données. Cette option concerne uniquement l’actualisation planifiée ; [En savoir plus](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings9.png)

## <a name="remove-a-data-source"></a>Supprimez une source de données.
La suppression d’une source de données entraîne l’arrêt des éventuels tableaux de bord ou rapports qui reposent sur la source de données en question.  

Pour supprimer une source de données, accédez à Source de données > **Supprimer**.

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings6.png)

## <a name="manage-administrators"></a>Gérer les administrateurs
Sous l’onglet Administrateurs, pour la passerelle, vous pouvez ajouter et supprimer des utilisateurs qui peuvent administrer la passerelle. Vous pouvez uniquement ajouter des utilisateurs à ce stade. Vous ne pouvez pas ajouter de groupes de sécurité.

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings8.png)

## <a name="manage-users"></a>Gérer les utilisateurs
Sous l’onglet Utilisateurs, pour la source de données, vous pouvez ajouter et supprimer des utilisateurs ou des groupes de données qui peuvent utiliser cette passerelle.

> [!NOTE]
> La liste des utilisateurs contrôle uniquement les personnes autorisées à publier des rapports. Les propriétaires des rapports peuvent créer des tableaux de bord ou des packs de contenu et les partager avec d’autres utilisateurs.
> 
> 

![](media/service-gateway-enterprise-manage-scheduled-refresh/datasourcesettings5.png)

## <a name="using-the-data-source-for-scheduled-refresh"></a>Utilisation de la source de données pour une actualisation planifiée
Une fois la source de données créée, elle peut être utilisée avec des connexions DirectQuery ou via une actualisation planifiée.

> [!NOTE]
> Le nom du serveur et celui de la base de données doivent correspondre entre Power BI Desktop et la source de données dans la passerelle de données locale.
> 
> 

Le lien entre votre jeu de données et la source de données dans la passerelle est basé sur le nom de votre serveur et sur le nom de votre base de données. Ils doivent correspondre. Par exemple, si vous fournissez une adresse IP pour le nom du serveur, dans Power BI Desktop, vous devez utiliser l’adresse IP de la source de données dans la configuration de la passerelle. Si vous utilisez *SERVEUR\INSTANCE*, dans Power BI Desktop, vous devez utiliser la même valeur dans la source de données configurée pour la passerelle.

Si vous êtes répertorié sous l’onglet **Utilisateurs** de la source de données configurée dans la passerelle, et que le nom du serveur et celui de la base de données correspondent, la passerelle s’affiche comme option à utiliser avec l’actualisation planifiée.

![](media/service-gateway-enterprise-manage-scheduled-refresh/powerbi-gateway-enterprise-schedule-refresh.png)

> [!WARNING]
> Si votre jeu de données contient plusieurs sources de données, chaque source de données doit être ajoutée au sein de la passerelle. Si une ou plusieurs sources de données ne sont pas ajoutées à la passerelle, vous ne verrez pas la passerelle comme étant disponible pour l’actualisation planifiée.
> 
> 

## <a name="limitations"></a>Limites
* OAuth n’est pas un schéma d’authentification pris en charge avec la passerelle de données locale. Vous ne pouvez pas ajouter des sources de données qui nécessitent OAuth. Si votre jeu de données contient une source de données nécessitant OAuth, vous ne pourrez pas utiliser la passerelle pour une actualisation planifiée.

## <a name="next-steps"></a>Étapes suivantes
[Passerelle de données locale](service-gateway-onprem.md)  
[Informations approfondies sur la passerelle de données locale](service-gateway-onprem-indepth.md)  
[Résolution des problèmes de passerelle de données locale](service-gateway-onprem-tshoot.md)  
D’autres questions ? [Posez vos questions à la communauté Power BI](http://community.powerbi.com/)
