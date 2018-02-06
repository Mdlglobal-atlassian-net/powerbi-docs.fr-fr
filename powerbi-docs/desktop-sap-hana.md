---
title: Utiliser SAP HANA dans Power BI Desktop
description: Utiliser SAP HANA dans Power BI Desktop
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
ms.openlocfilehash: 9cbeb0b2504612a9eb32fdad1d95fd90b57e07d9
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2017
---
# <a name="use-sap-hana-in-power-bi-desktop"></a>Utiliser SAP HANA dans Power BI Desktop
Avec Power BI Desktop, vous pouvez désormais accéder aux bases de données **SAP HANA** . Pour utiliser **SAP HANA**, le pilote ODBC de HANA SAP doit être installé sur l’ordinateur client local pour que la connexion de données **SAP HANA** de Power BI Desktop fonctionne correctement. Vous pouvez télécharger le pilote ODBC de SAP HANA à partir du [centre de téléchargement des logiciels SAP](https://support.sap.com/swdc). À partir de là, recherchez SAP HANA CLIENT pour les ordinateurs Windows. Étant donné que le **Centre de téléchargement de logiciels SAP** modifie sa structure fréquemment, des informations plus spécifiques sur la navigation dans ce site ne sont pas disponibles.

Pour vous connecter à une base de données **SAP HANA**, sélectionnez **Obtenir des données > Base de données > Base de données SAP HANA**, comme indiqué dans l’image suivante.

![](media/desktop-sap-hana/sap-hana-1.png)

Lorsque vous vous connectez à une base de données SAP HANA, spécifiez le nom et le port du serveur au format *serveur:port*. L’image suivante présente un exemple avec un serveur nommé *ServerXYZ* et un port *30015*.

![](media/desktop-sap-hana/sap-hana-2.png)

Dans cette version, **SAP HANA** en mode [DirectQuery](desktop-use-directquery.md) est pris en charge dans Power BI Desktop et le service Power BI, et vous pouvez publier ou charger des rapports qui utilisent **SAP HANA** en mode DirectQuery pour le service Power BI. Vous pouvez également publier et charger des rapports dans le service Power BI quand vous n’utilisez pas **SAP HANA** en mode DirectQuery.

### <a name="supported-features-for-sap-hana"></a>Fonctionnalités prises en charge pour SAP HANA
Cette version comporte de nombreuses fonctionnalités pour **SAP HANA**, comme indiqué dans la liste suivante :

* Le connecteur Power BI pour **SAP HANA** utilise le pilote ODBC de SAP pour offrir les meilleures conditions d’utilisation.
* **SAP HANA** prend en charge les options DirectQuery et Importer.
* Power BI prend en charge les modèles CIM HANA (tels que les vues d’analyse et de calcul) et il possède un mode de navigation optimisé.
* Avec **SAP HANA** , vous pouvez également utiliser la fonctionnalité SQL directe de connexion aux tables Row et Column.
* Comprend la navigation améliorée pour les modèles HANA
* Power BI prend en charge les variables et paramètres d’entrée **SAP HANA** .

### <a name="installing-the-sap-hana-odbc-driver"></a>Installation du pilote ODBC SAP HANA
### <a name="limitations-of-sap-hana"></a>Limitations de SAP HANA
Il existe également quelques limitations à l’utilisation de **SAP HANA**, indiquées ci-dessous :

* Les chaînes NVARCHAR sont tronquées à 4 000 caractères Unicode.
* SMALLDECIMAL n’est pas pris en charge.
* VARBINARY n’est pas pris en charge.
* Les dates valides sont comprises entre le 30/12/1899 et le 31/12/9999.
