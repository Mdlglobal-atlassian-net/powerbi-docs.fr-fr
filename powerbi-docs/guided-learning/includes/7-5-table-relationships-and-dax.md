Power BI vous permet de créer des relations entre plusieurs tables, notamment des tables provenant de sources de données complètement différentes. Vous pouvez voir ces relations pour n’importe quel modèle de données dans la vue **Relations** de Power BI Desktop.

![](media/7-5-table-relationships-and-dax/dax-relationships_1.png)

## <a name="dax-relational-functions"></a>Fonctions relationnelles de DAX
DAX dispose de **fonctions relationnelles** qui vous permettent d’interagir avec les tables qui ont des relations établies.

Vous pouvez retourner la valeur d’une colonne ou toutes les lignes dans une relation à l’aide des fonctions DAX.

Par exemple, la fonction **TABLE** suit les relations et retourne la valeur d’une colonne, tandis que **RELATEDTABLE** suit les relations et retourne une table complète filtrée pour inclure uniquement les lignes associées.

![](media/7-5-table-relationships-and-dax/dax-relationships_2.png)

La fonction **RELATED** fonctionne sur les relations *plusieurs-à-un*, tandis que **RELATEDTABLE** s’applique aux relations *un-à-plusieurs*.

Vous pouvez utiliser des fonctions relationnelles pour créer des expressions incluant des valeurs de plusieurs tables. DAX retourne un résultat avec ces fonctions, quelle que soit la longueur de la chaîne de la relation.

> Contenu vidéo fourni par [Alberto Ferrari, SQLBI](http://www.sqlbi.com/learning-dax/?utm_source=powerbi&utm_medium=marketing&utm_campaign=after-summit)
> 
> 
