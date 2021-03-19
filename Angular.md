# Angular le Framework #

1990 : HTML
1998 : HTML + CSS
2000 : JS
2005 : AJAX permet les interactions avec des backends HTTP
En 2010 : première version d'Angular JS

Apparition des Frameworks :
- Rapidité : gain de temps et livraison + rapides qu'un développement à partir de 0
- Organisation : l'architecture d'un Framework favorise une bonne Organisation du code (MVC, MVVC)
-


## Framework Angular ##

Permet de créer plus facilmeent de SPA (single Page Applications). Pas de rafraichissement du navigateur, temps de chargement réduits, etc. Cela charge toute l'application mais n'affiche qu'une partie seulement sur le site en lazy loading.


**Les avantages**
- Typescript : code plus sûr, mieux organisé, plus maintenable
- Organisé en modules puis composants & services : on sépare les triatements (la view, le control ...)
- Modèle MVVM : à la fois les donnéesstockées et la façon dont elles sont affichées
- Développé et maintenu par Google
- Forte demande sur le marché Bordelais
- Framewort complet avec une architecture élégante : gestionnaire de dépendances services, injection de dépendances, routing, testing.
- Documentation très bien fournie
- Utilise prime ng à la place de Bootstrap

**Les inconvénients**
- TypeSript : lourd
- Courbe d'apprentissage difficile : JS + TS, RXJS injection de projets lourds...


## Utiliser Angular ##

**Installer Angular**
>npm install -g @angular/cli

**Créer un projet Angular**
> ng new myProjectName


**Un module** c'est une boîte dans laquelle on met des composants. La plupart du temps un seul module est suffisant.

**Un composant** c'est un très petit élément du site composé de HTML, CSS,TypeScript. Il a une fonction partiulière. Exemple un header ou une barre de menu ou une section d'un site sont des composants. Un composant a vocation a être réutilisé en changeant juste les valeurs qu'il reçoit. Il sert de "patern". Cela évite de répéter son code.

### Pour créer un nouveau composant: ###
>ng generate component nomDuComposant
ou
ng g c nomDuComposant


>Exemple: ng g c home


Angular a créé un nouveau dossier home pour notre composant home qui a été créé. Dedans il y un fichier home.component.ts qui contient la classe.

```
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-home',
  templateUrl: './home.component.html',
  styleUrls: ['./home.component.scss']
})
export class HomeComponent implements OnInit {

  constructor() { }

  ngOnInit(): void {

  }

}
```

>ngOnInit() est une fonction qui est lancée au démarrage du composant on peut mettre dedans ce qu'on veut. On peut aussi mettre des trucs dans le constructor. Le @Component c'est les metaData (le chemin vers la partie html/css/scss de ce composant).

Pour lancer l'application  :

>ng s

>ng serve --open
