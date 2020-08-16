# LES DECORATEURS

 Les décorateurs sont des métadonnées qui sont adressées au compilateur TypeScript. Il faut savoir que les décorateurs sont purement une fonctionnalité TypeScript actuellement. Ils sont néanmoins en proposition pour les prochaines versions de JavaScript. Il n'est pas impossible que la prochaine ou une des prochaines versions de JavaScript contienne des décorateurs de façon native.

 Exemples : 
 ```
let d1 = (conctructor) => console.log('Décorateur appelé.')

@d1
class Cl1<T> {
     constructor (public arg1: T, public arg2: T) {}
}

let a = new Cl1(1,2);
```

pour éviter que le compilateur ne compile pas
executer la commande suivante :
tsc --experimentalDecorators [nomFichier.ts]


il en existe cinq types différents. Une remarque préliminaire : tous les éléments susceptibles d'être décorés sont liés à la notion de classe, c'est-à-dire qu’on peut décorer soit la classe elle-même avec le décorateur classe, soit des éléments appartenant à cette classe, comme par exemple des méthodes ou des propriétés. Le premier type de décorateurs est un décorateur de classe. Les autres types de décorateurs, décorateur de méthodes, d'accesseur, de propriété, de paramètres, tous ces décorateurs vont être fonctionnels lorsque ces éléments sont à l'intérieur d'une classe. 

Exemples:
```
let accesseurs = {
    get prop1() {
        console.log('prop1')
    },
    set prop2(value) {
        console.log('prop2')
    }
}
let a = accesseurs.prop1;
accesseurs.prop2 = "foo";

// autres exemple

let d1 = (conctructor) => console.log('Décorateur appelé.')

let d2: PropertyDecorator = (prototype, name) => {
    console.log(prototype);
    console.log(name);
}

@d1
class Cl1 <T>{
    constructor (public arg1: T, public arg2: T) {}

    @d2
    prop1: string = "foo";
}
let c = new cl1<number>(1,2);
```
