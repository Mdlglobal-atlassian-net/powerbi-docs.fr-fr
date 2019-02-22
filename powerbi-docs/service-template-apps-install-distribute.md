---
title: Distribuer des applications modèles dans votre organisation - Power BI (préversion)
description: Découvrez comment installer, personnaliser et distribuer des applications modèles dans votre organisation à l’aide de Power BI.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 02/07/2019
ms.author: maggies
ms.openlocfilehash: cd3a1f94aa4c965327ea3e5bcb7271326aa3514d
ms.sourcegitcommit: 8207c9269363f0945d8d0332b81f1e78dc2414b0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56249673"
---
# <a name="install-and-distribute-template-apps-in-your-organization---power-bi-preview"></a>Installer et distribuer des applications modèles dans votre organisation - Power BI (préversion)

Les nouvelles *applications modèles* Power BI permettent aux partenaires Power BI de créer des applications Power BI avec peu ou pas de codage et de les déployer ensuite vers n’importe quel client Power BI. Cet article est destiné aux analystes Power BI. Il explique comment installer, personnaliser et distribuer une application modèle qui a été créée par un partenaire Power BI. Si vous êtes intéressé par la création d’applications modèles à distribuer vous-même, consultez [Créer une application modèle dans Power BI](service-template-apps-create.md).

![Applications Power BI installées](media/service-template-apps-install-distribute/power-bi-get-apps.png)

Quand vous installez une application modèle qui a été créée par un partenaire Power BI, vous pouvez modifier l’application selon les besoins de votre organisation, puis la distribuer à vos collègues sous forme d’application.  

## <a name="prerequisites"></a>Prérequis  

Les prérequis pour installer, personnaliser et distribuer une application modèle sont les suivants :  

- Une [licence Power BI Pro](service-self-service-signup-for-power-bi.md)
- Une bonne connaissance des [concepts de base de Power BI ](service-basic-concepts.md)
- Un lien d’installation valide fourni par le créateur de l’application modèle ou AppSource. 
- Les autorisations d’installation d’applications modèles. 

## <a name="install-a-template-app"></a>Installer une application modèle

Vous avez peut-être reçu un lien vers une application modèle. À défaut, vous pouvez rechercher une application qui vous intéresse dans AppSource. Dans les deux cas, après avoir installé l’application, vous pouvez la modifier et la distribuer au sein de votre organisation.

### <a name="search-appsource-from-a-browser"></a>Rechercher dans AppSource à partir d’un navigateur

Dans un navigateur, sélectionnez ce lien pour ouvrir AppSource filtré sur les applications Power BI :

- https://appsource.microsoft.com/marketplace/apps?product=power-bi

### <a name="search-appsource-from-the-power-bi-service"></a>Rechercher dans AppSource à partir du service Power BI

1. Dans le volet de navigation de gauche du service Power BI, sélectionnez **Applications** > **Obtenir des applications**.

    ![Obtenir des applications](media/service-template-apps-install-distribute/power-bi-get-apps-arrow.png)

2. Dans AppSource, sélectionnez **Applications**.

    ![Rechercher dans AppSource](media/service-template-apps-install-distribute/power-bi-appsource.png)

3. Parcourez les applications ou recherchez l’application souhaitée, puis sélectionnez **Obtenir maintenant**.

2. Dans la boîte de dialogue, sélectionnez **Installer**.

    Si vous avez une licence Power BI Pro, l’application est installée avec l’espace de travail d’application associé. Vous personnalisez l’application dans cet espace de travail.

    Au terme de l’installation, vous voyez une notification indiquant que la nouvelle application est prête. 

3. Sélectionnez **Accéder à l’application**.
4. Dans **Bien démarrer avec votre nouvelle application**, sélectionnez l’une des trois options ci-dessous :

    ![Bien démarrer avec votre nouvelle application](media/service-template-apps-create/power-bi-template-app-get-started.png)

    - **Explorer l’application** : cette option permet une exploration rapide avec un exemple de données. Choisissez d’abord cette option pour voir l’apparence générale de l’application. 
    - **Connecter des données** : changez la source de données de l’exemple de données par votre propre source de données. Vous pouvez redéfinir les paramètres du jeu de données et les informations d’identification de la source de données. Consultez la section [Limitations connues](service-template-apps-tips.md#known-limitations) dans l’article « Conseils pour créer des applications modèles ». 
    - **Accéder à l’espace de travail** (option la plus avancée) : vous pouvez apporter toute modification autorisée par le concepteur de l’application.

    Ignorez cette boîte de dialogue si vous souhaitez accéder à l’espace de travail associé directement par le biais de l’onglet **Espaces de travail** dans le volet de navigation de gauche.   
 
5. Avant de partager l’application avec vos collègues, vous voudrez peut-être vous connecter à vos propres données. Vous pouvez également avoir besoin de modifier le rapport ou le tableau de bord en fonction des besoins de votre organisation. Vous pouvez aussi ajouter d’autres rapports ou tableaux de bord à ce stade.

## <a name="update-and-distribute-the-app"></a>Mettre à jour et distribuer l’application

Une fois que vous avez mis à jour l’application pour votre organisation, vous êtes prêt à la publier. Suivez les mêmes étapes de publication que pour une application standard. 

1. Lorsque vous avez fini le travail de personnalisation, dans la vue Liste de l’espace de travail, sélectionnez **Mettre à jour l’application** dans le coin supérieur droit.  

    ![Démarrer l’installation de l’application](media/service-template-apps-install-distribute/power-bi-start-install-app.png)

2. Dans **Détails**, vous pouvez modifier la description et changer la couleur d’arrière-plan.

   ![Définir la description et la couleur de l’application](media/service-template-apps-install-distribute/power-bi-install-app-details.png)

3. Dans **Contenu**, vous pouvez sélectionner une page d’accueil (le tableau de bord ou le rapport).

   ![Définir la page d’accueil de l’application](media/service-template-apps-install-distribute/power-bi-install-app-content.png)

4. Dans **Accès**, vous pouvez accorder l’accès uniquement aux utilisateurs sélectionnés ou à toute votre organisation.  

   ![Définir l’accès à l’application](media/service-template-apps-install-distribute/power-bi-install-access.png)

5. Sélectionnez **Mettre à jour l’application**. 

6. Une fois que l’application a été publiée avec succès, vous pouvez copier le lien associé et le partager avec les utilisateurs à qui vous avez accordé l’accès. Si vous avez partagé le lien avec ces utilisateurs, ces derniers le voient également dans l’onglet **Mon organisation** dans AppSource.

## <a name="next-steps"></a>Étapes suivantes 

[Créer des espaces de travail avec vos collègues dans Power BI](service-create-workspaces.md)





  

 