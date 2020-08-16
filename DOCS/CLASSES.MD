# LES CLASSES

 une classe, c'est une fonctionnalité propre à ES6, donc à la version 6 de JavaScript. JavaScript n'a pas de type. Donc sa finalité première n'est pas de créer un nouveau type, mais c'est de créer de nouvelles instances à partir d'une fonction déguisée, entre guillemets, sous le keyword class. Donc ça pour dire que la finalité première d’une classe n'est absolument pas de créer un nouveau type. Si l'objectif de votre code est simplement de créer un type sans création d'objets, d'instance par la suite, il vaut mieux utiliser l'interface. En revanche, si vous souhaitez déclarer une classe qui vous permettra ensuite d'instancier des objets à partir de cette classe, bien évidemment, il faut utiliser la classe et du même coup, nous aurons un type qui lui sera associé. 

* exemple JS (ES6): 
```
class FooBar {
    constructor() {}
    foo = 'blah';
    bar = 21;
}
// instanciation
let bar = new FooBar();
console.log(bar.bar); // 21
```

Les classes JS sont des sucres syntaxiques (ou raccourci d'écriture), le code ci-dessus revient à faire le code ci-dessous :

```
function _classcallCheck(instance, Constructor) {
    // appelle le constructeur
}

var FooBar = function FooBar() {
    _classcallCheck(this, FooBar);
    this.foo = 'Blah';
    this.bar = 21;
}

let bar = new FooBar();
console.log(bar.bar); // 21
```
# Une classe peut implémenter une interface

```
interface IFooBar {
    foo: string;
    bar: string;
}

class FooBar implements IFooBar {
    foo: string;
    bar: string;
    constructor(arg1, arg2) {
        this.foo = arg1;
        this.bar = arg2
    }
}