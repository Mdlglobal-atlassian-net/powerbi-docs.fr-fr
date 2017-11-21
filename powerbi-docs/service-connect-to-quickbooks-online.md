---
title: "Se connecter à QuickBooks Online avec Power BI"
description: QuickBooks Online pour Power BI
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
ms.openlocfilehash: def174cb86b701f628e4637d3a9933a42c5a5740
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-quickbooks-online-with-power-bi"></a>Se connecter à QuickBooks Online avec Power BI
Quand vous vous connectez à vos données QuickBooks Online à partir de Power BI, vous obtenez immédiatement un tableau de bord et des rapports Power BI contenant des informations sur le flux de trésorerie de votre entreprise, sa rentabilité, ses clients et bien plus encore. Vous pouvez utiliser le tableau de bord et les rapports tels quels ou bien les personnaliser pour mettre en avant les informations qui vous intéressent le plus. Les données sont actualisées automatiquement une fois par jour.

Connectez-vous au [pack de contenu QuickBooks Online](https://dxt.powerbi.com/getdata/services/quickbooks-online) pour Power BI.

>[!NOTE]
>Pour importer vos données QuickBooks Online dans Power BI, vous devez être administrateur de votre compte QuickBooks Online et vous connecter à l’aide de vos informations d’identification d’administrateur.

## <a name="how-to-connect"></a>Comment se connecter
1. Sélectionnez **Obtenir des données** en bas du volet de navigation gauche.
   
   ![](media/service-connect-to-quickbooks-online/pbi_getdata.png) 
2. Dans la zone **Services** , sélectionnez **Obtenir**.
   
   ![](media/service-connect-to-quickbooks-online/pbi_getservices.png) 
3. Sélectionnez **QuickBooks Online**, puis **Obtenir**.
   
   ![](media/service-connect-to-quickbooks-online/qbo.png)
4. Sélectionnez **oAuth2** pour la méthode d’authentification, puis **Se connecter**. 
5. Quand vous y êtes invité, entrez vos informations d’identification QuickBooks Online et suivez le processus d’authentification QuickBooks Online. Si vous êtes déjà connecté à QuickBooks Online dans votre navigateur, vous ne serez peut-être pas invité à entrer vos informations d’identification.
   >[!NOTE]
   >Le compte QuickBooks Online nécessite des informations d’identification d’administrateur.
6. Dans l’écran suivant, sélectionnez l’entreprise que vous voulez connecter à Power BI.
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_almost.png)
7. Sélectionnez **Autoriser** dans l’écran suivant pour commencer le processus d’importation. Ce dernier peut prendre quelques minutes selon la taille des données de votre entreprise. 
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_authorizesm.png)
   
   Une fois les données importées dans Power BI, vous verrez un nouveau tableau de bord, un nouveau rapport et un nouveau jeu de données dans le volet de navigation gauche. Les nouveaux éléments sont signalés par un astérisque jaune \*.
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_leftnavnew.png)
8. Sélectionnez le tableau de bord QuickBooks Online. Il s’agit du tableau de bord créé automatiquement par Power BI pour afficher vos données importées. Vous pouvez modifier ce tableau de bord pour afficher vos données comme vous le souhaitez. 
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_dash.png)

**Et maintenant ?**

* Essayez de [poser une question dans la zone Q&R](service-q-and-a.md) en haut du tableau de bord.
* [Modifiez les vignettes](service-dashboard-edit-tile.md) dans le tableau de bord.
* [Sélectionnez une vignette](service-dashboard-tiles.md) pour ouvrir le rapport sous-jacent.
* Même si une actualisation quotidienne de votre jeu de données est planifiée, vous pouvez modifier la planification de l’actualisation ou essayer d’actualiser le jeu de données sur demande à l’aide de l’option **Actualiser maintenant**.

## <a name="troubleshooting"></a>Résolution des problèmes
**« Désolé. Une erreur s’est produite. »**

Si vous obtenez ce message après avoir sélectionné **Autoriser**:

« Désolé. Une erreur s’est produite. Fermez cette fenêtre, puis réessayez.

Un autre utilisateur de l’entreprise s’est déjà abonné à l’application. Contactez [e-mail de l’administrateur] pour apporter des modifications à cet abonnement. »

![](media/service-connect-to-quickbooks-online/pbi_qbo_oopssm.png)

... cela signifie qu’un autre administrateur de votre entreprise a déjà connecté vos données d’entreprise à Power BI. Demandez à l’administrateur en question de partager le tableau de bord avec vous. Actuellement, un seul administrateur peut connecter un jeu de données d’entreprise QuickBooks Online à Power BI. Une fois le tableau de bord créé par Power BI, l’administrateur peut le partager avec plusieurs collègues appartenant aux mêmes clients Power BI.

**« Cette application n’est pas configurée pour autoriser les connexions depuis votre pays »**

Actuellement, Power BI prend uniquement en charge les éditions américaines de QuickBooks Online. 

![](media/service-connect-to-quickbooks-online/pbi_qbo_countrynotsupported.png)

## <a name="next-steps"></a>Étapes suivantes
[Prise en main de Power BI](service-get-started.md)

[Power BI – Concepts de base](service-basic-concepts.md)
