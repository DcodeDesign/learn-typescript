# LES INTERFACES

Les interfaces sont des metadatas qui décrivent la structure d'un objet. 

L'objectif d'une interface, c’est simplement de créer un type et d'appliquer un contrat sur les éléments implémentant cette interface. Donc si j'ai une variable de type défini par une interface, cette variable devra avoir la forme définie par une interface.

Une interface a une double valeur. C'est-à-dire qu'elle a à la fois une valeur de type, ce qui signifie que lorsque l'on déclare une interface, on déclare un nouveau type que l'on va pouvoir réutiliser et assigner à plusieurs variables différentes. Elle a aussi, une valeur de contrat, donc ça, cela signifie que les variables qui sont associées aux types définis par notre interface vont devoir respecter la structure qui est imposée par l'interface. 

Les interfaces sont propre au TYPESCRIPT, une fois compilé en JAVASCRIPT les interfaces disparaissent.

* exemple :

```
interface IFooBar {
    foo: string;
    bar: number;
}

let bar: IFooBar = {foo: 'Foo', bar: 2}

let wrongBar: IFooBar = {foo: 1, bar: 2}
```