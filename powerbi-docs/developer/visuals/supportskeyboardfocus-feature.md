---
title: La fonctionnalité supportsKeyboardFocus
description: Cet article explique comment utiliser la fonctionnalité supportsKeyboardFocus dans les visuels Power BI, et ses exigences.
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 04/30/2020
ms.openlocfilehash: c8cf0f4e896b8a44764d1c363c597182f55d30b3
ms.sourcegitcommit: 0e9e211082eca7fd939803e0cd9c6b114af2f90a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83276510"
---
# <a name="use-the-supportskeyboardfocus-feature"></a>Utiliser la fonctionnalité supportsKeyboardFocus

Cet article décrit comment utiliser la fonctionnalité `supportsKeyboardFocus` dans les visuels Power BI.
La fonctionnalité `supportsKeyboardFocus` permet de parcourir les points de données de l’élément visuel à l’aide du clavier uniquement.

Pour en savoir plus sur la navigation au clavier pour les visuels, consultez [Navigation au clavier](../../create-reports/desktop-accessibility-consuming-tools.md#keyboard-navigation).

## <a name="example"></a>Exemple

Ouvrez un visuel qui utilise la fonctionnalité `supportsKeyboardFocus`. Sélectionnez un point de données dans le visuel, puis sélectionnez la touche Tab. Le focus se déplace vers le point de données suivant chaque fois que vous sélectionnez la touche Tab. Sélectionnez Entrée pour sélectionner le point de données en surbrillance.

![Prend en charge l’exemple de focus clavier](./media/supportskeyboardfocus-feature/supports-keyboard-focus-example.png)

## <a name="requirements"></a>Configuration requise

Cette fonctionnalité requiert l’API v2.1.0 ou une version ultérieure.

Cette fonctionnalité peut être appliquée à tous les visuels, à l’exception des visuels d’image.

## <a name="usage"></a>Utilisation

Pour utiliser la fonctionnalité `supportsKeyboardFocus`, ajoutez le code suivant au fichier *capabilities.json* de votre visuel.
Cette fonctionnalité permet au visuel de recevoir le focus via la navigation au clavier.

```json
    {   
            ...
        "supportsKeyboardFocus": true
            ...
    }

```

## <a name="next-steps"></a>Étapes suivantes

Pour en savoir plus sur les fonctionnalités d’accessibilité, consultez [Conception des rapports Power BI pour l’accessibilité](../../create-reports/desktop-accessibility-creating-reports.md).

Pour essayer le développement Power BI, consultez [Développement d’un visuel Power BI](custom-visual-develop-tutorial.md).
