---
title: Distribuer du contenu à des utilisateurs invités externes avec Azure AD B2B
description: Power BI permet de partager du contenu avec des utilisateurs invités externes par le biais d’Azure Active Directory Business to Business (Azure AD B2B).
author: kfollis
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: conceptual
ms.date: 09/09/2019
ms.author: kfollis
LocalizationGroup: Administration
ms.openlocfilehash: 09b2f8afd78eda244a6862459a85558efa0fa1c2
ms.sourcegitcommit: bfc2baf862aade6873501566f13c744efdd146f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83129337"
---
# <a name="distribute-power-bi-content-to-external-guest-users-with-azure-ad-b2b"></a>Distribuer du contenu Power BI à des utilisateurs invités externes avec Azure AD B2B

Power BI permet de partager du contenu avec des utilisateurs invités externes par le biais d’Azure Active Directory Business to Business (Azure AD B2B).
En utilisant Azure AD B2B, votre organisation active et régit le partage avec des utilisateurs externes à un emplacement central. Par défaut, les invités externes disposent d’une expérience de consommation uniquement. De plus, vous pouvez autoriser les utilisateurs invités extérieurs à votre organisation à modifier et à gérer du contenu au sein de votre organisation.

Cet article offre une introduction générale à Azure AD B2B dans Power BI. Pour plus d’informations, consultez [Distribuer du contenu Power BI à des utilisateurs invités externes avec Azure AD B2B](../guidance/whitepaper-azure-b2b-power-bi.md).

## <a name="enable-access"></a>Activer l’accès

Veillez à activer la fonctionnalité [Partager du contenu avec des utilisateurs externes](service-admin-portal.md#export-and-sharing-settings) dans le portail d’administration de Power BI avant de convier des utilisateurs invités. Même si cette option est activée, l’utilisateur doit disposer dans Azure Active Directory de l’autorisation d’inviter des utilisateurs, qui est accordée par le biais du rôle Inviteur d’invités. 

L’option [Autoriser les utilisateurs invités externes à modifier et à gérer le contenu de l’organisation](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization) vous permet d’accorder aux utilisateurs invités la possibilité de voir et créer du contenu dans les espaces de travail, notamment la navigation dans le contenu Power BI de votre organisation.

> [!NOTE]
> Le paramètre [Partager du contenu avec des utilisateurs externes](service-admin-portal.md#export-and-sharing-settings) détermine si Power BI permet d’inviter des utilisateurs externes dans votre organisation. Une fois qu’un utilisateur externe a accepté l’invitation, il devient un utilisateur invité Azure AD B2B de l’organisation. Il apparaît dans les sélecteurs de personnes dans l’ensemble de l’expérience Power BI. Lorsque le paramètre est désactivé, les utilisateurs déjà invités dans votre organisation conservent leurs accès d’origine et restent listés dans les expériences des sélecteurs de personnes. Par ailleurs, les invités ajoutés par le biais de l’approche des [invitations planifiées](#planned-invites) apparaîtront également dans les sélecteurs de personnes. Pour empêcher les utilisateurs invités d’accéder à Power BI, utilisez une stratégie d’accès conditionnel Azure AD.

## <a name="who-can-you-invite"></a>Qui pouvez-vous inviter ?

Il est possible d’inviter dans votre organisation quasiment tous les utilisateurs qui ont une adresse e-mail, notamment des comptes personnels comme gmail.com, outlook.com et hotmail.com. Azure AD B2B appelle ces adresses des *identités sociales*.

Vous ne pouvez pas inviter des utilisateurs associés à un cloud gouvernemental, comme [Power BI pour le gouvernement américain](service-govus-overview.md).

## <a name="invite-guest-users"></a>Inviter des utilisateurs

Les utilisateurs invités nécessitent des invitations seulement la première fois que vous les invitez dans votre organisation. Pour inviter des utilisateurs, utilisez des invitations planifiées ou ad hoc.

Pour utiliser des invitations ad hoc, servez-vous des fonctionnalités suivantes :
* Partage de rapports et de tableaux de bord
* Liste d’accès à l’application

Les invitations ad hoc ne sont pas prises en charge dans la liste d’accès à l’espace de travail. Utilisez l’[approche des invitations planifiées](#planned-invites) pour ajouter ces utilisateurs à votre organisation. Une fois que l’utilisateur externe est un invité dans votre organisation, ajoutez-le à la liste d’accès à l’espace de travail.

### <a name="planned-invites"></a>Invitations planifiées

Utilisez une invitation planifiée si vous savez quels utilisateurs inviter. Le portail Azure ou PowerShell vous permet d’envoyer les invitations. Vous devez être un administrateur de locataire pour inviter des personnes.

Procédez comme suit pour envoyer une invitation dans le portail Azure.

1. Dans le [portail Azure](https://portal.azure.com), sélectionnez **Azure Active Directory**.

1. Sous **Gérer**, sélectionnez **Utilisateurs** > **Tous les utilisateurs** > **Nouvel utilisateur invité**.

    ![Capture d’écran du portail Azure avec l’option Nouvel utilisateur invité affichée.](media/service-admin-azure-ad-b2b/azure-ad-portal-new-guest-user.png)

1. Entrez une **adresse e-mail** et un **message personnel**.

    ![Capture d’écran de la boîte de dialogue Nouvel utilisateur invité du portail Azure AD.](media/service-admin-azure-ad-b2b/azure-ad-portal-invite-message.png)

1. Sélectionnez **Inviter**.

Pour inviter plus d’un utilisateur, utilisez PowerShell. Pour plus d’informations, consultez [Code Azure AD B2B Collaboration et exemples PowerShell](/azure/active-directory/b2b/code-samples/).

L’utilisateur invité doit sélectionner **Mise en route** dans l’e-mail d’invitation qu’il reçoit. L’utilisateur invité est ensuite ajouté au client.

![Capture d’écran de l’invitation par e-mail d’un utilisateur invité.](media/service-admin-azure-ad-b2b/guest-user-invite-email.png)

### <a name="ad-hoc-invites"></a>Invitations ad hoc

Pour inviter à tout moment un utilisateur externe, ajoutez-le à votre tableau de bord ou à votre rapport à l’aide de l’interface utilisateur de partage, ou à votre application via la page d’accès. L’exemple suivant montre comment inviter un utilisateur externe à utiliser une application.

![Capture d’écran d’un utilisateur externe ajouté à la liste d’accès d’une application dans Power BI.](media/service-admin-azure-ad-b2b/power-bi-app-access.png)

L’utilisateur invité reçoit un e-mail indiquant que vous avez partagé l’application avec lui.

![Capture d’écran de l’e-mail indiquant qu’une application est partagée avec un utilisateur invité](media/service-admin-azure-ad-b2b/guest-user-invite-email-2.png)

L’utilisateur invité doit se connecter en utilisant l’adresse e-mail de son organisation. Il recevra une demande d’acceptation de l’invitation une fois connecté. Après la connexion, l’application s’ouvre pour l’utilisateur invité. Pour revenir à l’application, il doit marquer le lien à l’aide d’un signet ou enregistrer l’e-mail.


## <a name="licensing"></a>Licences

L’utilisateur invité doit disposer de la licence appropriée pour voir le contenu que vous avez partagé. Il existe trois façons de vérifier que l’utilisateur dispose d’une licence appropriée : utiliser Power BI Premium, attribuer une licence Power BI Pro ou utiliser la licence Power BI Pro de l’invité.

Les [utilisateurs invités qui peuvent modifier et gérer le contenu de l’organisation](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization) ont besoin d’une licence Power BI Pro pour contribuer au contenu des espaces de travail ou partager du contenu avec d’autres utilisateurs.

### <a name="use-power-bi-premium"></a>Utiliser Power BI Premium

L’affectation de l’espace de travail à la [capacité Power BI Premium](service-premium-what-is.md) permet à l’utilisateur invité d’utiliser l’application sans disposer d’une licence Power BI Pro. Power BI Premium permet également à des applications de tirer parti d’autres capacités, comme des fréquences de rafraîchissement accrues, une capacité dédiée et des modèles de grande taille.

![Diagramme de l’expérience d’un utilisateur invité avec Power BI Premium.](media/service-admin-azure-ad-b2b/license-approach-1.png)

### <a name="assign-a-power-bi-pro-license-to-guest-user"></a>Affecter une licence Power BI Pro à un utilisateur invité

L’attribution d’une licence Power BI Pro à un utilisateur invité au sein de votre locataire permet à cet utilisateur de voir du contenu dans le locataire. Pour plus d’informations sur l’attribution de licences, consultez [Attribution de licences à des utilisateurs via la page Licences](/office365/admin/manage/assign-licenses-to-users#assign-licenses-to-users-on-the-licenses-page). Avant d’attribuer des licences Pro à des utilisateurs invités, vérifiez auprès de votre responsable de compte Microsoft que vous remplissez les conditions de votre contrat avec Microsoft.

![Diagramme de l’expérience d’un utilisateur invité avec une licence Pro provenant de votre locataire.](media/service-admin-azure-ad-b2b/license-approach-2.png)

### <a name="guest-user-brings-their-own-power-bi-pro-license"></a>Utilisateur invité apportant sa propre licence Power BI Pro

L’utilisateur invité dispose déjà d’une licence Power BI Pro assignée à l’intérieur de son client.

![Diagramme de l’expérience d’un utilisateur invité quand ils apportent leur propre licence.](media/service-admin-azure-ad-b2b/license-approach-3.png)

## <a name="guest-users-who-can-edit-and-manage-content"></a>Utilisateurs invités pouvant modifier et gérer du contenu

Quand vous utilisez la fonctionnalité [Autoriser les utilisateurs invités externes à modifier et à gérer le contenu de l’organisation](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization), les utilisateurs invités spécifiés bénéficient d’un accès supplémentaire au système Power BI de votre organisation. Les invités autorisés peuvent voir tout contenu pour lequel ils disposent d’une autorisation, accéder à l’accueil, parcourir des espaces de travail, installer des applications, voir où ils figurent dans la liste d’accès et contribuer au contenu des espaces de travail. Ils peuvent créer ou être des administrateurs d’espaces de travail qui utilisent la nouvelle expérience d’espace de travail. Certaines limitations s’appliquent. La section Considérations et limitations liste ces restrictions.
 
Pour aider les invités autorisés à se connecter à Power BI, fournissez-leur l’URL du locataire. Pour trouver l’URL de locataire, effectuez les étapes suivantes.

1. Dans le service Power BI, menu supérieur, sélectionnez l’aide ( **?** ), puis **À propos de Power BI**.

2. Recherchez la valeur en regard de **URL de locataire**. Partagez l’URL du locataire avec les utilisateurs invités autorisés.

    ![Capture d’écran de la boîte de dialogue À propos de Power BI avec l’URL du locataire affichée pour l’utilisateur invité.](media/service-admin-azure-ad-b2b/power-bi-about-dialog.png)

## <a name="considerations-and-limitations"></a>Considérations et limitations

* Par défaut, Azure AD B2B limite les invités externes à la seule consommation du contenu. Les invités Azure AD B2B externes peuvent consulter les applications, les tableaux de bord et les rapports, exporter des données, et créer des abonnements par courrier pour les tableaux de bord et les rapports. Ils ne peuvent pas accéder aux espaces de travail ou publier leur propre contenu. Pour supprimer ces restrictions, vous pouvez utiliser la fonctionnalité [Autoriser les utilisateurs invités externes à modifier et à gérer le contenu de l’organisation](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization).

* Pour inviter des utilisateurs, une licence Power BI Pro est nécessaire. Les utilisateurs de la version Pro d’essai ne peuvent pas inviter d’utilisateurs dans Power BI.

* Certaines expériences ne sont pas disponibles pour les [utilisateurs invités qui peuvent modifier et gérer le contenu de l’organisation](service-admin-portal.md#allow-external-guest-users-to-edit-and-manage-content-in-the-organization). Pour mettre à jour ou publier des rapports, ils doivent utiliser l’interface utilisateur web du service Power BI, notamment l’option Obtenir les données pour charger des fichiers Power BI Desktop.  Les expériences suivantes ne sont pas prises en charge :
    * Diriger la publication de Power BI Desktop vers le service Power BI
    * Les utilisateurs invités ne peuvent pas utiliser Power BI Desktop pour se connecter à des jeux de données du service dans le service Power BI
    * Espaces de travail classiques liés à des groupes Office 365 :
        * Un utilisateur invité ne peut pas créer ou être un administrateur de ces espaces de travail
        * Les utilisateurs invités peuvent être membres
    * L’envoi d’invitations ad hoc n’est pas pris en charge pour les listes d’accès aux espaces de travail
    * Power BI Publisher pour Excel n’est pas pris en charge pour les utilisateurs invités
    * Les utilisateurs invités ne peuvent pas installer une passerelle Power BI Gateway et la connecter à votre organisation
    * Les utilisateurs invités ne peuvent pas installer d’applications à publier dans toute l’organisation
    * Les utilisateurs invités ne peuvent pas utiliser, créer, mettre à jour ou installer des packs de contenu d’organisation
    * Les utilisateurs invités ne peuvent pas utiliser la fonctionnalité Analyser dans Excel
    * Les utilisateurs invités ne peuvent pas être @mentioned dans les commentaires
    * Les utilisateurs invités ne peuvent pas utiliser des abonnements
    * Les utilisateurs invités qui utilisent cette fonctionnalité doivent disposer d’un compte professionnel ou scolaire. 
    
* Les utilisateurs invités utilisant des comptes personnels seront confrontés à plus de limitations en raison de restrictions de connexion.
    * Ils peuvent utiliser les expériences de consommation dans le service Power BI par le biais d’un navigateur web.
    * Ils ne peuvent pas utiliser d’applications Power BI Mobile.
    * Ils ne peuvent pas se connecter et spécifier des informations d’identification quand un compte professionnel ou scolaire est nécessaire.

* Pour l’instant, cette fonctionnalité n’est pas disponible avec le composant WebPart de rapport Power BI SharePoint Online.

* Des paramètres Active Directory peuvent limiter ce que les utilisateurs invités externes peuvent faire dans l’ensemble de votre organisation. Ceci s’applique également à votre environnement Power BI. La documentation suivante décrit les paramètres :
    * [Gérer les paramètres de collaboration externes](/azure/active-directory/b2b/delegate-invitations#configure-b2b-external-collaboration-settings)
    * [Autoriser ou bloquer les invitations aux utilisateurs B2B provenant d’organisations spécifiques ](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list)
    * [Autoriser les utilisateurs invités à accéder au service Power BI ou les en empêcher](/azure/active-directory/conditional-access/overview)
    
* Le partage en dehors de l’organisation n’est pas pris en charge par les clouds nationaux. Créez des comptes d’utilisateur dans votre organisation qui permettront aux utilisateurs externes d’accéder au contenu. 

* Si vous partagez du contenu directement avec un utilisateur invité, Power BI lui envoie un e-mail avec le lien. Pour éviter l’envoi d’un e-mail, ajoutez l’utilisateur invité à un groupe de sécurité et partagez le contenu avec le groupe de sécurité.  

## <a name="next-steps"></a>Étapes suivantes

Pour plus d’informations, notamment sur la façon dont fonctionne la sécurité au niveau des lignes, consultez le livre blanc : [Distribuer du contenu Power BI à des utilisateurs invités externes à l’aide d’Azure AD B2B](https://aka.ms/powerbi-b2b-whitepaper).

Pour plus d’informations sur Azure AD B2B, consultez [Qu’est-ce qu’Azure AD B2B Collaboration ?](/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b/).
