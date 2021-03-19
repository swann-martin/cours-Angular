# Apprendre TypeScript #

TypeScript est un surensemble de JavaScript. TypeScript est 100% rétrocompatible avec JavaScript. On peut coder en pur JS dans un fichier .ts. Les fichier .ts sont transformés en JS grâse au transpileur d'Angular.

En TypeSript on peut faire du front avec Angular. On peut faire aussi du backEnd avec NestJs.

en TypeScript
```
function tsAdd(a: number, b: number ): number {
  return a+ b
}
```

En JS :
```
let animal = 'fish'
```
En TS :
```
let animal:  string = 'fish'
```


Les types en TS :

>string, number, array, boolean, any, void

Exemple :
>let animalArray: string[] = ['fish', 'shark', 'horse' ]

>let count :number = 5

>let condition boolean = true

> let anything: any = true

>let everything: any = 'universe'

```
function exemple(): void {
  console.log('Hello')
}

```


Compiler = c'est convertir un progamme d'un e forme compréhensible (haut niveau) vers une forme compréhensible (bas niveau).

Transpiler  = convertir un langage de haut niveau vers un autre langage de haut niveau.


Pour installer TypeScript on tape dans la console :
>npm install -g typescript

Ensuite il suffit de créer dans vs code un fichier en avec l'extension .ts comme par exemple exemple.ts

Pour faire une transpilation d'un fichier .ts et le transformer en JS il faut dans la console demander à node de le faire.
>tsc nomDeMonFichier.ts

> tsc exemple.ts


## POO et TS ##

Un model objet vise à modeliser et à traduire en code des concepts du monde réél.
expl : dans le monde réel une voiture possède un moteur , des roues, une couleur des portes. Il est possible d'effectuer des actions dessus : ouvrir des portes...


### Construire une classe et un objet ###

Un classe c'est un peu déssiner les plans pour construire quelque chose. Le constructeur équivaut à l'usine où vont être créer les objets grâce à des machines... Ensuite on pourra lancer la construction/l'itération d'un objet.

```
class Counter {
  name: string;
  value number = 0; // valeur à 0 par défaut
  max: number;

  constructor(name: string, max: number) {
    this.max = max;
    this.name = name;
  }

  getValue(): number {
    return this.value;
  }
}

```

Les valeurs que l'on passe au constructeur permettent de créer/itérer un objet en particulier en fonction des paramètres/ arguments qu'on entre.

```
const counter1 = new Counter("Counter #1", 5);
const counter2 = new Counter("Counter #2", 3);
```
**Le mot clé : this** permet à un objet (une instance de classe) de se référencer lui-même. C'est à dire qu'un objet, compteur, voiture, etc... peut accéder à ses propres valeurs.
