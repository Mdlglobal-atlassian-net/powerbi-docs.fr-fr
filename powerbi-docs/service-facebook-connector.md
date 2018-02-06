---
title: "Service tiers : connecteur Facebook pour Power BI Desktop"
description: "Service tiers : connecteur Facebook pour Power BI Desktop"
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
ms.openlocfilehash: 4e8600aac79683a53b7c2075b3d81e91b3354901
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2017
---
# <a name="facebook-connector-for-power-bi-desktop"></a>Connecteur Facebook pour Power BI Desktop
Le connecteur Facebook de **Power BI Desktop** s’appuie sur l’API Graph de Facebook. Par conséquent, les fonctionnalités et la disponibilité peuvent varier au fil du temps.

Vous pouvez consulter un [didacticiel sur le connecteur Facebook pour Power BI Desktop](desktop-tutorial-facebook-analytics.md).

La version v1.0 de l’API Graph de Facebook a expiré le 30 <sup>avril</sup> 2015. Power BI utilise l’API Graph en arrière-plan pour le connecteur Facebook, ce qui vous permet de vous connecter à vos données et de les analyser.

Les requêtes créées avant le 30 <sup>avril</sup> 2015 ne fonctionnent peut-être plus ou retournent moins de données. Depuis le 30 <sup>avril</sup> 2015, Power BI utilise la version 2.2 dans tous les appels à l’API Facebook. Si votre requête a été créée avant le 30 avril 2015 et que vous ne l’avez pas utilisée depuis, vous devrez probablement vous authentifier à nouveau afin d’approuver le nouveau jeu d’autorisations que nous vous demanderons.

Nous nous efforçons de publier des mises à jour en fonction des modifications. Toutefois, il se peut que l’API soit modifiée d’une manière qui affecte les résultats des requêtes que nous générons. Dans certains cas, certaines requêtes peuvent ne plus être prises en charge. En raison de cette dépendance, nous ne pouvons pas garantir les résultats de vos requêtes lors de l’utilisation de ce connecteur.

Pour plus d’informations sur la modification de l’API de Facebook, accédez [ici](https://developers.facebook.com/docs/apps/changelog#v2_0).
