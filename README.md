# SassyBeam (draft)

## Another “BEM-like” notation

Beam (ou SassyBeam) permet d'utiliser une notation de type [BEM](http://bem.info/method/definitions/).

Il s'inspire des [réflexions de Nicolas Gallagher](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/) et des [adaptations de Harry Roberts](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) tout en y apportant ma petite touche personnelle…

### Objectifs de Beam

1. Appliquer une méthode “BEM-like” de type `.block__element--modifier`.
2. Garder un code HTML light :
    ```
    <div class="block block--mod1 block--mod2">
    ```
    devient :
    ```
    <div class="block--mod1--mod2">
    ```
3. Gestion des “états” via pseudo-classes, classes ou attribut data-state
4. Permettre l'imbrication des blocks et des éléments … ou pas !
5. Maintenir l'intégrité des noms de classes (et donc, éviter la concaténation dynamique du genre `#{$block}__element`)

## Usage

### via Bower

```
$ bower install SassyBeam
```

## Exemples

## Credits

- @necolas
- @wizardry

---

**N'hésitez pas à adapter, commenter, partager…**
