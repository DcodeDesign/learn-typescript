# TYPES GENERIQUES

Cela sert à caractériser un typage lorsqu’on ne connaît pas le type mais qu'on souhaiterait qu'il y ait des liens entre les différents types que l'on manipule.

Exemple : 
```
let a: <T>(v: T) => T[] = (value) => [value];

interface Int1 {
    prop1: T;
    prop2: T[]
}

let b: Int1 <number> = {
    prop1: 21,
    prop2: [21]
}

class Cl1 <T>{
    constructor (public arg1: T, public arg2: T) {}

    toArray : () => T[] = () => [this.arg1, this.arg2]
}
let c = new cl1<number>(1,2);
c.toArray // intellisence reconnaît le type number
```
<T> = type générique