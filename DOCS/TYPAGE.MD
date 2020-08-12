# TYPAGE
```
    association > variable + type 
```

# TYPAGE DYNAMIQUE
```
    TYPAGE LORS DU RUNTIME
    TYPE INFERE
    MODIFICATION DU TYPE possible

    lorsque je déclare une variable, 
    je ne vais pas lui assigner de type. 
    Je vais simplement, déclarer ma variable, 
    éventuellement, lui attribuer une valeur. 
    De ce fait, lorsque mon script sera exécuté, 
    le type va être inféré, il va être deviné 
    par la machine qui va exécuter le script.
```

# TYPAGE STATIQUE
```
    TYPAGE DANS LE CODE
    TYPE DEFINIT à la DECLARATION de la VARIABLE
    PAS DE MODIFICATION POSSIBLE

```

# EXEMPLES : TYPAGE PRIMITIFS
```
    Booléen
    Null
    Undefined
    Nombre
    String
    Symbole
    Objet : 
        Array
        Function
        Promise
        Error
```

# Connaître le type d'une variable
```
    > let var = [1,2]
    < undefined
    > typeof var;
    < "object"
    > var instanceof array;
    < true
```

# TYPESCRIPT UTILISE LES OBJETS GLOBAUX
liste : 

> https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Objets_globaux

# TYPE any permet la typa dynamic d'une variable
```
    let a: any = 4;
    a = "foo";
```

# TYPER une varibale littéralement (personnalisé)
```
let a : {
    prop1: string;
    prop2: number;
}
a = { prop1: "Test"} > OK
a = { prop2: 4} > OK
a = { prop3: "2"} > NOK
```