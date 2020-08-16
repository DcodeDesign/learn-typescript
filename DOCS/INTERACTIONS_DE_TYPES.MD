# INTERACTION DE TYPES

L'interaction de types, qu'est-ce que c'est ? C'est l'idée que, des fois, on va avoir besoin de déclarer des variables par exemple, qui auront soit un type soit un autre, ou alors qui même mixeront deux types.

Croisement de types :
    - UNION : |
    - croisement : &

Exemple : 

```
let a = (value: string | Array<any> | number) => console.log(value.lenght);

interface Int1 {
    prop1: any;
    prop1: any;
}

interface Int2 {
    prop3: any;
}

let a: Int1 & Int2 = {
    prop1: 1,
    prop2: 2,
    prop3: 3
}

let a: Int1 | Int2 = {
    prop1: 1,
    prop3: 3
}
```

 
