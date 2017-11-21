---
title: "Configuration des paramètres de proxy pour la passerelle de données locale"
description: "Informations sur la configuration des paramètres de proxy pour la passerelle de données locale."
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 6fb6250f8cd82c7057abe3f9cf9792dc733ea4b6
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2017
---
# <a name="configuring-proxy-settings-for-the-on-premises-data-gateway"></a>Configuration des paramètres de proxy pour la passerelle de données locale
Votre environnement de travail peut nécessiter que vous passiez par un proxy pour accéder à Internet. Cela pourrait empêcher la passerelle de données locale de Power BI de se connecter au service.

## <a name="does-your-network-use-a-proxy"></a>Votre réseau utilise-t-il un proxy ?
Le billet suivant sur superuser.com explique comment vous pouvez essayer de déterminer si vous disposez d’un proxy sur votre réseau.

[Comment savoir quel serveur proxy j’utilise ? (SuperUser.com)](https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using)

## <a name="configuration-file-location-and-default-configuration"></a>Emplacement du fichier de configuration et configuration par défaut
Les informations de proxy sont configurées dans un fichier de configuration .NET. L’emplacement et les noms de fichiers seront différents selon la passerelle utilisée.

### <a name="on-premises-data-gateway"></a>Passerelle de données locale
Il existe deux principaux fichiers de configuration impliqués dans la passerelle de données locale.

**Configuration**

Le premier concerne les écrans de configuration qui configurent en fait la passerelle. Si vous rencontrez des problèmes lors de la configuration de la passerelle, c’est le fichier que vous devez consulter.

    C:\Program Files\On-premises data gateway\enterprisegatewayconfigurator.exe.config

**Service Windows**

La deuxième concerne le service Windows à proprement parler, qui interagit avec le service Power BI et gère les requêtes.

    C:\Program Files\On-premises data gateway\Microsoft.PowerBI.EnterpriseGateway.exe.config

### <a name="power-bi-gateway---personal"></a>Power BI Gateway - Personal
> [!NOTE]
> Une nouvelle version de la passerelle de données locale, appelée **Passerelle de données locale (mode personnel)** est disponible pour Power BI. Cette section de l’article décrit la précédente version de la passerelle personnelle, appelée **Power BI Gateway - Personal**, qui sera supprimée et cessera de fonctionner après le 31 juillet 2017. Pour plus d’informations sur la nouvelle version de la passerelle personnelle, notamment sur son installation, consultez l’article [**Passerelle de données locale (mode personnel)**](service-gateway-personal-mode.md).
> 
> 

La passerelle personnelle peut être installée de deux façons. En tant que service Windows (admin) ou en tant qu’application en mode utilisateur. Cela est déterminé lors de l’installation. Par conséquent, vos fichiers de configuration peuvent être dans l’un des deux emplacements en fonction de la façon dont la passerelle a été installée. Vous devez vérifier les deux emplacements.

**Configuration**

Le premier concerne les écrans de configuration qui configurent en fait la passerelle. Si vous rencontrez des problèmes lors de la configuration de la passerelle, c’est le fichier que vous devez consulter.

Pour le *service Windows*, ce sera le suivant.

    C:\Program Files\Power BI Personal Gateway\1.0\Configurator\GWConfig.exe.config
    C:\Program Files\Power BI Personal Gateway\1.0\Configurator\PowerBIGatewayAgentCmdLine.exe.config

Pour l’*application en mode utilisateur*, ce sera le suivant.

    C:\Users\<user>\AppData\Local\Power BI Gateway - Personal \1.0\Configurator\GWConfig.exe.config
    C:\Users\<user>\AppData\Local\Power BI Gateway - Personal \1.0\Configurator\PowerBIGatewayAgentCmdLine.exe.config

**Service Windows**

La deuxième concerne le service Windows à proprement parler, qui interagit avec le service Power BI et gère les requêtes.

Pour le *service Windows*, ce sera le suivant.

    C:\Program Files\Power BI Personal Gateway\1.0\Gateway\diawp.exe.config

Pour l’*application en mode utilisateur*, ce sera le suivant.

    C:\Users\<user>\AppData\Local\Power BI Gateway - Personal \1.0\Gateway\diawp.exe.config

## <a name="configuring-proxy-settings"></a>Configuration des paramètres de proxy
La configuration de proxy par défaut est la suivante.

    <system.net>
        <defaultProxy useDefaultCredentials="true" />
    </system.net>

La configuration par défaut fonctionne avec l’authentification Windows. Si votre proxy utilise une autre forme d’authentification, vous devez modifier les paramètres. En cas de doute, vous devez contacter votre administrateur réseau.

Pour en savoir plus sur la configuration des éléments de proxy pour les fichiers de configuration .NET, consultez [defaultProxy, élément (paramètres réseau)](https://msdn.microsoft.com/library/kd3cf2ex.aspx).

## <a name="changing-the-gateway-service-account-to-a-domain-user"></a>Remplacement du compte de service de passerelle par un utilisateur de domaine
Lorsque vous configurez les paramètres de proxy pour utiliser les informations d’identification par défaut, comme expliqué ci-dessus, vous pouvez rencontrer des problèmes d’authentification avec votre proxy. Cela est dû au fait que le compte de service par défaut est le SID de service et non un utilisateur de domaine authentifié. Vous pouvez modifier le compte de service de la passerelle pour autoriser une authentification appropriée auprès de votre proxy.

> [!NOTE]
> Nous vous recommandons d’utiliser un compte de service administré pour éviter d’avoir à réinitialiser les mots de passe. Découvrez comment créer un [compte de service administré](https://technet.microsoft.com/library/dd548356.aspx) dans Active Directory.
> 
> 

### <a name="change-the-on-premises-data-gateway-service-account"></a>Modifier le compte de service de la passerelle de données locale
1. Modifiez le compte de service Windows du **service de passerelle de données locale**.
   
    Le compte par défaut de ce service est *NT SERVICE\PBIEgwService*. Vous pouvez le remplacer par un compte utilisateur de domaine au sein de votre domaine Active Directory. Vous pouvez également utiliser un compte de service administré pour éviter d’avoir à réinitialiser le mot de passe.
   
    Vous pouvez modifier le compte sous l’onglet **Connexion** des propriétés du service Windows.
2. Redémarrez le **service de passerelle de données locale**.
   
    Dans une invite de commandes d’administration, exécutez les commandes suivantes.
   
        net stop PBIEgwService
   
        net start PBIEgwService
3. Démarrez l’**outil de configuration de la passerelle de données locale**. Vous pouvez sélectionner le bouton Démarrer de Windows et rechercher *Passerelle de données locale*.
4. Connectez-vous à Power BI.
5. Restaurez la passerelle à l’aide de votre clé de récupération.
   
    Ainsi, le nouveau compte de service est en mesure de déchiffrer les informations d’identification stockées pour les sources de données.

## <a name="next-steps"></a>Étapes suivantes
[Passerelle de données locale (mode personnel)](service-gateway-personal-mode.md)
[Informations sur le pare-feu](service-gateway-onprem-tshoot.md#firewall-or-proxy)  
D’autres questions ? [Posez vos questions à la communauté Power BI](http://community.powerbi.com/)
