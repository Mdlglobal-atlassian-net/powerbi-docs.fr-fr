---
title: Dispositions personnalisées avec le contenu incorporé Power BI
description: En savoir plus sur les dispositions personnalisées lors de l’incorporation de contenu Power BI dans votre application.
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: reference
ms.date: 12/19/2017
ms.openlocfilehash: e114c208093c9f3401c43e9ea44502e65d6d84fd
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "79493201"
---
# <a name="custom-layouts"></a>Dispositions personnalisées

Les dispositions personnalisées permettent d’incorporer un rapport avec une disposition différente de celle du rapport d’origine. La définition d’une nouvelle disposition varie entre la définition de la taille de page uniquement, le contrôle de la taille des visuels ou la position et la visibilité.

Pour définir une disposition personnalisée, définissez un objet disposition personnalisée et transmettez-le à l’objet paramètres dans la configuration d’incorporation. De plus, définissez LayoutType sur Personnalisé. Pour plus d’informations, consultez [Incorporer des informations détaillées sur la configuration](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details).

```javascript
var embedConfig = {
    ...
    settings: {
            layoutType: models.LayoutType.Custom,
            customLayout: {...}
    }
};
```

## <a name="object-definition"></a>Définition d’objet

```javascript
interface ICustomLayout {
  pageSize?: IPageSize;
  displayOption?: DisplayOption;
  pagesLayout?: PagesLayout;
}

enum PageSizeType {
  Widescreen,
  Standard,
  Letter,
  Custom
}
interface IPageSize {
  type: PageSizeType;
}
interface ICustomPageSize extends IPageSize {
  width?: number;
  height?: number;
}

enum DisplayOption {
  FitToPage,
  FitToWidth,
  ActualSize
}
```

- `pageSize` : utilisez la taille de page pour contrôler la taille du canevas (par exemple, zone blanche du rapport).
- `displayOptions` : les valeurs possibles sont FitToWidth, FitToPage ou ActualSize. Cette option contrôle la mise à l’échelle du canevas pour l’ajuster au Iframe.
- `pagesLayout` : contrôle la disposition de chaque visuel. Pour plus d’informations, contactez la rubrique sur la disposition des pages.

## <a name="pages-layout"></a>Disposition des pages

La définition d’un objet disposition de page consiste fondamentalement à définir une disposition pour chaque page, et pour chaque page, vous définissez une disposition pour chaque visuel.
La disposition des pages est facultative. Si vous ne définissez pas de disposition pour une page, la disposition par défaut (qui est enregistrée dans le rapport) est appliquée.

pagesLayout est un mappage entre le nom de la page et l’objet PageLayout. Définition :

```javascript
type PagesLayout = { [key: string]: IPageLayout; };
```

PageLayout contient un mappage de disposition visuelle, qui mappe chaque nom de visuel à un objet de disposition visuelle :

```javascript
interface IPageLayout {
  visualsLayout: { [key: string]: IVisualLayout; };
}
```

## <a name="visual-layout"></a>Disposition visuelle

Pour définir une disposition visuelle, transmettez de nouvelles options d’emplacement, de taille et un nouvel état de visibilité.

```javascript
interface IVisualLayout {
  x?: number;
  y?: number;
  z?: number;
  width?: number;
  height?: number;
  displayState?: IVisualContainerDisplayState;
}

interface IVisualContainerDisplayState {
  mode: VisualContainerDisplayMode;
}

enum VisualContainerDisplayMode {
  Visible,
  Hidden
}
```

- `x,y,z` : définit la nouvelle position du visuel.
- `width`, hauteur : définit la nouvelle taille du visuel.
- `displayState` : définit la visibilité du visuel.

## <a name="update-layout"></a>Mettre à jour la disposition

Vous pouvez utiliser la méthode updateSettings pour mettre à jour la disposition du rapport à tout moment pendant le chargement de celui-ci. Consultez [Mettre à jour les paramètres](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Update-Settings).

## <a name="code-example"></a>Exemple de code

```javascript
// Get models. models contains enums that can be used.
var models = window['powerbi-client'].models;

var embedConfiguration = {
    type: 'report',
    id: '5dac7a4a-4452-46b3-99f6-a25915e0fe55',
    embedUrl: 'https://app.powerbi.com/reportEmbed',
    tokenType: models.TokenType.Embed,
    accessToken: 'H4...rf',
    settings: {
            layoutType: models.LayoutType.Custom,
            customLayout: {
                pageSize: {
                    type: models.PageSizeType.Custom,
                    width: 1600,
                    height: 1200
                }
            },
            displayOption: models.DisplayOption.ActualSize,
            pagesLayout: {
                "ReportSection1" : {
                    visualsLayout: {
                        "VisualContainer1": {
                            x: 1,
                            y: 1,
                            z: 1,
                            width: 400,
                            height: 300,
                            displayState: {
                                mode: models.VisualContainerDisplayMode.Visible
                            }
                        },
                        "VisualContainer2": {
                            displayState: {
                                mode: models.VisualContainerDisplayMode.Hidden
                            }
                        },
                    }
                }
            }
        }
    }
};

// Get a reference to the embedded report HTML element
var embedContainer = document.getElementById('embedContainer');

// Embed the report and display it within the div container.
var report = powerbi.embed(embedContainer, embedConfiguration);
```

## <a name="see-also"></a>Voir aussi

[Incorporer vos tableaux de bord, rapports et vignettes Power BI](embed-sample-for-customers.md)   
[Poser des questions à la communauté Power BI](https://community.powerbi.com/)
