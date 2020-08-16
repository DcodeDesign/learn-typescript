# Modules et namespaces

## Modules

Un module, ça sert à mettre une partie de notre code 
dans un fichier et à le « containériser », 
c'est-à-dire de faire en sorte que on puisse importer 
ou exporter ce fichier, et utiliser certaines de ses 
fonctionnalités, du moins, les fonctionnalités qui 
sont exportées. Vous allez comprendre tout de suite 
avec la petite démonstration que l'on va faire. 
Simplement, une petite chose à retenir est le fait 
que les modules nécessitent un module 
loader comme Webpack, par exemple. 
C'est-à-dire que lorsque j'ai créé mes modules 
qui appartiennent à différents fichiers, eh bien, 
pour que mon application, mon script accède à ces 
différents fichiers, lorsqu'il va être exécuté, 
on va avoir besoin d'un module loader.

Exemple:

*exports.js
```
export function export1() {
    console.log("Export 1.");
}
```

*module.js
```
import { export1 } from "./exports";
export1();
```

## Namespaces

namespace.js
```
/// <reference path="exportNamespace.ts" />

space1.exportNamespace();
```

exportNamespace.js
```
namespace space1 {

    export const a = "foo";

    export function exportNamespace() {
        console.log('Export');
    }
}

space1.exportNamespace();
```

### compilsation avec typescript (tsc)

pour la compilation avec typescript il faudra executé le code suivant:

```
tsc --outFile nameFile.js nameFile.ts
```

