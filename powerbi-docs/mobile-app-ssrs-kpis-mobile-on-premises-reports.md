---
title: "Afficher des rapports et des indicateurs de performance clés locaux dans des applications mobiles Power BI"
description: "Les applications mobiles Power BI pour iOS vous offrent un accès mobile en direct à vos informations métier locales via une interface tactile dans SQL Server Reporting Services et Power BI Report Server."
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
ms.date: 12/18/2017
ms.author: maggies
ms.openlocfilehash: 5bbd2f09187e9fac16f6cc4b9ac3ff59a888ed7f
ms.sourcegitcommit: ea247cb3cfc1cac076d4b076c1ad8e2fc37e15a1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2017
---
# <a name="view-on-premises-report-server-reports-and-kpis-in-the-power-bi-mobile-apps"></a>Afficher des indicateurs de performance clés et des rapports Report Server locaux dans des applications mobiles Power BI
S’applique à :

| ![iPhone](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/iphone-logo-50-px.png) | ![iPad](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/ipad-logo-50-px.png) | ![Téléphone Android](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-phone-logo-50-px.png) | ![Tablette Android](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/android-tablet-logo-50-px.png) |
|:--- |:--- |:--- |:--- |
| iPhone |iPad |Téléphones Android |Tablettes Android |

Les applications mobiles Power BI vous offrent un accès mobile en direct à vos informations métier locales via une interface tactile dans Power BI Report Server et SQL Server 2016 Reporting Services (SSRS). 

 ![Accueil de Report Server dans les applications mobiles](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-pbi-report-server-home.png)

## <a name="first-things-first"></a>Avant tout
**Les applications mobiles sont l’emplacement où vous affichez du contenu Power BI, pas celui où vous le créez.**

* Vous et d’autres créateurs de rapports dans votre organisation [créez des rapports Power BI avec Power BI Desktop, puis les publiez sur le portail web de Power BI Report Server](report-server/quickstart-create-powerbi-report.md). 
* Vous pouvez également créer des [indicateurs de performance clés dans le portail web](https://docs.microsoft.com/sql/reporting-services/working-with-kpis-in-reporting-services), les organiser en dossiers et marquer vos favoris afin de pouvoir les retrouver aisément. 
* [Créez des rapports mobiles Reporting Services](https://docs.microsoft.com/sql/reporting-services/mobile-reports/create-mobile-reports-with-sql-server-mobile-report-publisher) avec l’éditeur de rapports mobiles SQL Server 2016 Enterprise Edition et publiez-les sur le [portail web Reporting Services](https://docs.microsoft.com/sql/reporting-services/web-portal-ssrs-native-mode).  

Ensuite, dans les applications mobiles Power BI, connectez-vous à jusqu’à jusqu’à cinq serveurs de rapports pour afficher les rapports et indicateurs de performance clés Power BI organisés dans des dossiers ou regroupés en favoris. 

## <a name="explore-samples-in-the-mobile-apps-without-a-server-connection"></a>Explorer des exemples dans les applications mobiles sans connexion au serveur
Même si vous n’avez pas accès à un portail web Reporting Services, vous pouvez toujours explorer les fonctionnalités des rapports mobiles et des indicateurs de performances clés de Reporting Services. 

1. Appuyez sur le bouton de navigation globale ![Bouton de navigation globale](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-global-nav-button.png) dans l’angle supérieur gauche, puis cliquez sur l’icône d’engrenage dans l’angle supérieur droit ![Icône d’engrenage](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ios-settings-icon.png).
2. Appuyez sur **Exemples Reporting Services**, puis naviguez pour interagir avec les exemples d’indicateurs de performance clés et de rapports mobiles.
   
   ![Exemples Reporting Services](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-ssrs-samples.png)

## <a name="connect-to-an-on-premises-server"></a>Se connecter à un serveur local
Vous pouvez afficher des rapports Power BI locaux, des rapports mobiles Reporting Services et des indicateurs de performance clés dans les applications mobiles Power BI. 

1. Sur votre appareil mobile, ouvrez l’application Power BI.
2. Si vous n’êtes pas encore connecté à Power BI, appuyez sur **Report Server**.
   
   ![Se connecter à un serveur de rapports](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-connect-to-rs-login.png)
   
   Si vous êtes déjà connecté à l’application Power BI, appuyez sur le bouton de navigation globale ![Bouton de navigation globale](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-global-nav-button.png), puis sur l’icône d’engrenage ![Icône d’engrenage](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ios-settings-icon.png) dans l’angle supérieur droit.
3. Appuyez sur **Se connecter au serveur**.
   
    ![Se connecter au serveur](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-android-server-sign-in.png)

     L’application mobile doit accéder au serveur d’une certaine façon. Plusieurs solutions s’offrent à vous :

    - Rester sur le même réseau/utiliser un VPN est le moyen le plus simple.
    - Il est possible d’utiliser un proxy d’application web pour se connecter depuis l’extérieur de l’organisation. Pour plus d’informations, consultez [Utilisation d’OAuth pour la connexion à Reporting Services](mobile-oauth-ssrs.md). 
    - Ouvrez une connexion (port) dans le pare-feu.

1. Renseignez l’adresse du serveur, ainsi que votre nom d’utilisateur et votre mot de passe. Utilisez ce format pour l’adresse du serveur :
   
     `http://<servername>/reports`
   
     OR
   
     `https://<servername>/reports`
   
   Ajoutez **http** ou **https** devant la chaîne de connexion.
   
    ![Boîte de dialogue Se connecter au serveur](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ios-connect-to-server-dialog.png)
5. (Facultatif) Sous **Options avancées**, vous pouvez affecter un nom convivial au serveur, si vous le souhaitez.
6. À présent, le serveur est visible dans la barre de navigation à gauche. Dans cet exemple, il est nommé « Power BI Report Server ».
   
   ![Serveur de rapports dans le volet de navigation gauche](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-left-nav-report-server.png)

## <a name="view-power-bi-reports-and-kpis-in-the-power-bi-app"></a>Afficher les rapports Power BI et les indicateurs de performance clés dans l’application Power BI
Les rapports Power BI, les rapports mobiles Reporting Services et les indicateurs de performance clés sont affichés dans les mêmes dossiers que sur le portail web Reporting Services. 

* Appuyer sur un rapport Power BI ![Icône de rapport Power BI](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-report-icon.png). Celui-ci s’ouvre en mode paysage et vous pouvez interagir avec lui dans l’application Power BI.
  
    ![Rapport Power BI](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-iphone-report-server-report.png)
* Dans Power BI Desktop, les propriétaires de rapports peuvent [optimiser un rapport](desktop-create-phone-report.md) pour les applications mobiles Power BI. Sur votre téléphone mobile, les rapports optimisés ont une icône ![icône de rapport Power BI optimisé](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-optimized-icon.png) et une disposition spéciales.
  
    ![Rapport Power BI optimisé pour les mobiles](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-rs-mobile-optimized-report.png)
* Appuyez sur un indicateur de performance clé pour l’afficher en mode Focus.
  
    ![Indicateur de performance clé en mode Focus](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/pbi_ipad_ssmrp_tile.png)

## <a name="view-your-favorite-kpis-and-reports"></a>Afficher vos rapports et indicateurs de performance clés favoris
Vous pouvez marquer des indicateurs de performance clés et des rapports en tant que favoris sur le portail web, et les afficher ainsi que vos tableaux de bord Power BI favoris dans un seul dossier sur votre appareil.

* Appuyez sur **Favoris**.
  
   ![Favoris dans le volet de navigation gauche](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-faves-pbi-report-server-update.png)
  
   Vos indicateurs de performance clés et rapports favoris du portail web figurent tous sur cette page, ainsi que les tableaux de bord Power BI du service Power BI :
  
   ![Rapports et tableau de bord Power BI dans la page Favoris](media/mobile-app-ssrs-kpis-mobile-on-premises-reports/power-bi-ipad-favorites.png)

## <a name="remove-a-connection-to-a-report-server"></a>Supprimez une connexion à un serveur de rapports
1. Appuyez sur **Paramètres**en bas de la barre de navigation de gauche.
2. Appuyez sur le nom du serveur duquel vous souhaitez vous déconnecter.
3. Appuyez sur **Supprimer le serveur**.

## <a name="next-steps"></a>Étapes suivantes
* [Prise en main de Power BI](service-get-started.md)  
* Vous avez des questions ? [Essayez d’interroger la communauté Power BI](http://community.powerbi.com/)
