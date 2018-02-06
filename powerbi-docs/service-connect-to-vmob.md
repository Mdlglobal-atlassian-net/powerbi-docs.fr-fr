---
title: "Se connecter à VMob avec Power BI"
description: VMob pour Power BI
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
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
ms.openlocfilehash: 09bd84fc320b550ccdaa0771f747a19bc1003150
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-vmob-with-power-bi"></a>Se connecter à VMob avec Power BI
Le suivi et l’exploration de vos données VMob sont faciles avec Power BI et le pack de contenu VMob. Power BI récupère les données suivantes : statistiques utilisateur pour toutes les périodes au cours des 30 derniers jours, indicateurs de performance clés de vente au détail pour les 30 derniers jours et performances de campagne pour les 30 derniers jours.

Connectez-vous au [pack de contenu VMob](https://app.powerbi.com/getdata/services/vmob) pour Power BI.

## <a name="how-to-connect"></a>Comment se connecter
1. Sélectionnez **Obtenir des données** en bas du volet de navigation gauche.
   
    ![](media/service-connect-to-vmob/getdata.png)
2. Dans la zone **Services** , sélectionnez **Obtenir**.
   
   ![](media/service-connect-to-vmob/services.png)
3. Sélectionnez **VMob** \> **Obtenir**.
   
   ![](media/service-connect-to-vmob/vmob.png)
4. Quand vous y êtes invité, entrez votre URL VMob et cliquez sur le bouton Suivant. Cette URL est fournie par VMob séparément.
   
    ![](media/service-connect-to-vmob/params.png)
5. Choisissez l’option **De base** dans la liste déroulante de la méthode d’authentification, entrez votre nom d’utilisateur VMob et votre mot de passe et cliquez sur le bouton **Se connecter** .
   
    ![](media/service-connect-to-vmob/creds.png)
6. Le processus d’importation commence automatiquement et Power BI récupère vos données VMob pour créer un tableau de bord prêt à l’emploi et un rapport pour vous.
   
   ![](media/service-connect-to-vmob/dashboard2.png)

**Et maintenant ?**

* Essayez de [poser une question dans la zone Q&R](power-bi-q-and-a.md) en haut du tableau de bord.
* [Modifiez les vignettes](service-dashboard-edit-tile.md) dans le tableau de bord.
* [Sélectionnez une vignette](service-dashboard-tiles.md) pour ouvrir le rapport sous-jacent.
* Même si une actualisation quotidienne de votre jeu de données est planifiée, vous pouvez modifier la planification de l’actualisation ou essayer d’actualiser le jeu de données sur demande à l’aide de l’option **Actualiser maintenant**.

## <a name="next-steps"></a>Étapes suivantes
[Prise en main de Power BI](service-get-started.md)

[Obtenir des données dans Power BI](service-get-data.md)
