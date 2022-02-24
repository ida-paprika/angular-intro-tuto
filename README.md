
*** POINTS CLEFS ***
--------------------

`PARTIE 1`
    - *component* : composé de 3 fichiers (.html, .css et .ts)

    - *AppModule.ts* : module root regroupant les composants du projet

    - <app-root> : composant-mère de tous les autres

    - *ngFor : directive structurelle intégrée, appliquée sur un élément de composant et permettant de le répéter => for(a in aa)

    - *ngIf : directive structurelle conditionnelle => if(true)

    - {{ interpolation.syntaxe }} : permet d'accéder aux propriétés d'un composant

    - [property]="binding" : permet de contrôler dynamiquement la valeur des propriété de composants

    - (event)="binding()" : permet d'associer un évenement à une méthode, directement sur un composant => addEventListener()

    - *ng generate component nom-composant* : commande de génération de composant (créé un dossier contenant les 3 fichiers)

    - *import {...} from '@angular/core'* : permet d'implémenter des interfaces depuis la bibliothèque d'Angular

    - *@Componant()* : décorateur permettant d'identifier une classe comme étant un composant Angular, et d'en définir ses caractéristiques

    - *@Input()* : décorateur permettant de passer des données d'un composant parent à son enfant

    - *@Output()* : décorateur permettant à un composant de transmettre des données à son parent
        -> *EventEmitter* 
        -> *(event)="property.emit()"* 
        -> *ParentComponent { onProperty() }*
        -> *<child-component (property)="onProperty()">*
        : permet de définir l'action à déclencher lors de l'évenement

----------
`PARTIE 2`
    - *class Router* / *interface Route* : service gérant la navigation parmi les vues et les URL / interface permettant de définir une route
        -> *app.module.ts* 
            *{ path: 'items/:item', component: ItemComponent }*
        -> *<a [routerLink]="'/items/', item">*
            : ajout d'une route, définition des segments fixes et variables de l'URL

    - *import { ActivatedRoute } from '@angular/router'* : permet d'implémenter les interfaces du service "router" d'Angular
        -> *ActivatedRoute* permet d'accéder aux informations d'une route
        -> *route.snapshot* permet d'accéder aux paramètres contenus dans la route
    
    - *Pipes* : permet de transformer des données (string, integer, date...) => {{ data | formatter }}

----------
`PARTIE 2`
    - *DI (dependency Injection* : permet d'injecter à une classe des sources externes plutôt que de les créer dedans. On défini un service comme injectable grace au décorateur *@Injectable*

    - *HttpClientModule* : module mettant à disposition des classes permettant de manipuler des requêtes et réponses HTTP

    - *HttpClient* : dépendance permettant d'envoyer des requêtes à des API externes

    - *stream* : canal de communication entre notre application et l'API externe

    - *| async* : permet d'utiliser directement des promesses ou observables sans stockage intermédiaire
