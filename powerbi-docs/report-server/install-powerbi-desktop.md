---
title: "Installer Power BI Desktop optimisé pour Power BI Report Server"
description: "Découvrez comment installer Power BI Desktop optimisé pour Power BI Report Server"
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
ms.date: 12/15/2017
ms.author: maggies
ms.openlocfilehash: c1c38d9d98c92963534081049cdcc6a557313639
ms.sourcegitcommit: ea247cb3cfc1cac076d4b076c1ad8e2fc37e15a1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2017
---
# <a name="install-power-bi-desktop-optimized-for-power-bi-report-server"></a>Installer Power BI Desktop optimisé pour Power BI Report Server
Découvrez comment installer Power BI Desktop optimisé pour Power BI Report Server.

Afin de créer des rapports Power BI pour Power BI Report Server, vous devez télécharger et installer Power BI Desktop optimisé pour Power BI Report Server. Il s’agit d’une version différente de Power BI Desktop utilisée avec le service Power BI. Par exemple, la version de Power BI Desktop pour le service Power BI inclut des fonctionnalités en préversion qui ne sont pas disponibles dans la version Power BI Report Server une fois publiées. Elle est nécessaire pour s’assurer que le serveur de rapports peut interagir avec une version connue des rapports et du modèle. 

> [!NOTE]
> Vous pouvez installer Power BI Desktop et Power BI Desktop optimisé pour Power BI Report Server côte à côte sur le même ordinateur.

## <a name="download-and-install-power-bi-desktop"></a>Télécharger et installer Power BI Desktop

Le moyen le plus simple d’avoir la version la plus récente de Power BI Desktop optimisée pour Power BI Report Server est de démarrer à partir du portail web de votre serveur de rapports.

1. Dans le portail web de votre serveur de rapports, sélectionnez la flèche **Télécharger** > **Power BI Desktop**.

    ![Télécharger Power BI Desktop à partir du portail web](media/install-powerbi-desktop/report-server-download-web-portal.png)

    Ou vous pouvez accéder directement à [Microsoft Power BI Desktop](https://go.microsoft.com/fwlink/?linkid=861076) (optimisé pour Power BI Report Server - octobre 2017) dans le Centre de téléchargement Microsoft.

2. Dans la page du Centre de téléchargement, sélectionnez **Télécharger**.

3. En fonction de votre ordinateur, sélectionnez : 

    - **PBIDesktopRS.msi** (version 32 bits) ou

    - **PBIDesktopRS_x64.msi** (version 64 bits).

1. Après avoir téléchargé le programme d’installation, exécutez l’Assistant Installation de Power BI Desktop (octobre 2017).
2. À l’issue de l’installation, cochez **Démarrer Power BI Desktop maintenant**.
   
    Power BI Desktop démarre et vous pouvez l’utiliser.

## <a name="verify-you-are-using-the-correct-version"></a>Vérifier que vous utilisez la version correcte
Vous pouvez vérifier que vous utilisez la version appropriée de Power BI Desktop en regardant l’écran de lancement ou la barre de titre dans Power BI Desktop. La barre de titre indique le mois et l’année de publication.

![Barre de titre pour Power BI Desktop optimisé pour Power BI Report Server](media/quickstart-create-powerbi-report/report-server-desktop-october-2017-version.png)

La barre de titre de la version Power BI Desktop du service Power BI n’affiche pas le mois et l’année.

## <a name="file-extension-association"></a>Association d’extension de fichier
Si vous avez installé Power BI Desktop et Power BI Desktop optimisé pour Power BI Report Server sur le même ordinateur, la dernière installation de Power BI Desktop a l’association de fichiers avec .pbix. Cela signifie que, lorsque vous double-cliquez sur un fichier pbix, cela a pour effet de lancer le dernier Power BI Desktop installé.

Si vous aviez Power BI Desktop, puis avez installé Power BI Desktop optimisé pour Power BI Report Server, tous les fichiers pbix s’ouvrent dans Power BI Desktop optimisé pour Power BI Report Server par défaut. Si préférez que Power BI Desktop soit l’application par défaut à lancer lors de l’ouverture d’un fichier pbix, réinstallez Power BI Desktop à partir du service Power BI.

Vous pouvez toujours commencer par ouvrir la version de Power BI Desktop que vous souhaitez utiliser, puis ouvrir le fichier à partir de Power BI Desktop.

La modification d’un rapport Power BI à partir de Power BI Report Server, ou la création d’un rapport Power BI à partir du portail web ont toujours pour effet d’ouvrir la version appropriée de Power BI Destop.

## <a name="considerations-and-limitations"></a>Considérations et limitations
Les rapports dans Power BI Report Server et dans le service Power BI (http://powerbi.com) fonctionnent pratiquement de la même manière, mais certaines fonctionnalités diffèrent.

### <a name="in-a-browser"></a>Dans un navigateur
Les rapports Power BI Report Server prennent en charge toutes les visualisations, à savoir :

* Éléments visuels personnalisés

Les rapports Power BI Report Server ne prennent pas en charge les fonctionnalités suivantes :

* Visuels R
* ArcGIS Maps
* Fil d’Ariane
* Fonctionnalités en préversion Power BI Desktop

### <a name="in-the-power-bi-mobile-apps"></a>Dans les applications mobiles Power BI
Les rapports Power BI Report Server prennent en charge toutes les fonctionnalités de base des [applications mobiles Power BI](../mobile-apps-for-mobile-devices.md), à savoir :

* [Disposition des rapports pour téléphone](../desktop-create-phone-report.md) : vous pouvez optimiser un rapport pour les applications mobiles Power BI. Sur votre téléphone mobile, les rapports optimisés ont une icône ![icône de disposition de rapport sur téléphone](media/quickstart-create-powerbi-report/power-bi-rs-mobile-optimized-icon.png) et une disposition spéciales.
  
    ![Rapports optimisés pour les téléphones](media/quickstart-create-powerbi-report/power-bi-rs-mobile-optimized-report.png)

Les rapports Power BI Report Server ne prennent pas en charge les fonctionnalités suivantes dans les applications mobiles Power BI :

* Visuels R
* ArcGIS Maps
* Éléments visuels personnalisés
* Fil d’Ariane
* Filtrage basé sur la géolocalisation ou codes barres

## <a name="next-steps"></a>Étapes suivantes
À présent que Power BI Desktop est installé, vous pouvez commencer à créer des rapports Power BI.

[Démarrage rapide : créer un rapport Power BI pour Power BI Report Server](quickstart-create-powerbi-report.md)  
[Prise en main de Power BI Desktop](../desktop-getting-started.md)  
Formation guidée : [Prise en main de Power BI Desktop](../guided-learning/gettingdata.yml#step-2)  
[Présentation du Manuel de l’utilisateur, Power BI Report Server](user-handbook-overview.md)

D’autres questions ? [Essayez d’interroger la communauté Power BI](https://community.powerbi.com/)
