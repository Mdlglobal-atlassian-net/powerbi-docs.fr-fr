---
title: Notifications d’interruption de service
description: Découvrez comment recevoir des notifications par e-mail en cas de perturbation ou de dégradation du service Power BI.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-service
ms.topic: conceptual
ms.date: 07/25/2019
ms.author: mblythe
ms.openlocfilehash: a33ace000917311cbd060c853e0122034a396ae2
ms.sourcegitcommit: 4595a6231615d253aead315cb3f85472e2f189e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68501730"
---
# <a name="service-interruption-notifications"></a>Notifications d’interruption de service

Il est essentiel d’avoir un aperçu de la disponibilité de vos applications métier stratégiques. Power BI fournit une notification d’incident pour vous permettre de recevoir éventuellement des e-mails en cas de dégradation ou de perturbation du service. Même si le contrat de niveau de service (SLA) de 99,9 % de Power BI rend ces occurrences rares, nous voulons nous assurer que vous êtes tenu informé. La capture d’écran suivante montre le type d’e-mail que vous recevrez si vous activez les notifications :

![Actualiser l’e-mail de notification](media/service-interruption-notifications/refresh-notification-email.png)

À l’heure actuelle, nous envoyons des e-mails pour les _scénarios de fiabilité_ suivants :

- Fiabilité des rapports ouverts
- Fiabilité des actualisations de modèles
- Fiabilité des actualisations de requêtes

Voici quelques exemples de ces notifications : les utilisateurs rencontrent un délai prolongé lors d’opérations telles que l’ouverture de rapports, l’actualisation du jeu de données ou l’exécution de requêtes. Après la résolution d’un incident, vous recevez un e-mail de suivi.

> [!NOTE]
> Cette fonctionnalité est actuellement disponible uniquement pour les capacités dédiées dans Power BI Premium. Elle n’est pas disponible pour la capacité partagée ou embarquée.

## <a name="enable-notifications"></a>Activer les notifications

Un administrateur de locataire Power BI active les notifications dans le portail d’administration :

1. Identifiez ou créez un groupe de sécurité prenant en charge les e-mails qui doit recevoir des notifications.

1. Dans le portail d’administration, sélectionnez **Paramètres du locataire**. Sous **Paramètres d’aide et de support**, développez **Recevoir des notifications par e-mail pour les pannes ou incidents du service**.

1. Activez les notifications, entrez un groupe de sécurité, puis sélectionnez **Appliquer**.

    ![Activer les notifications de service](media/service-interruption-notifications/enable-notifications.png)

> [!NOTE]
> Power BI envoie des notifications à partir du compte no-reply-powerbi@microsoft.com. Vérifiez que ce compte est inclus dans la liste verte afin que les notifications ne se retrouvent pas dans un dossier de spam ou de courrier indésirable.

## <a name="next-steps"></a>Étapes suivantes

[Options de support Power BI Pro et Power BI Premium](service-support-options.md)

D’autres questions ? [Posez vos questions à la communauté Power BI](http://community.powerbi.com/)