# Documentation

## Convention BEM

* B -> Block
* E -> Element
* M -> Modifier


```html

<!--- maintList = block -->
<ul class="mainList mainList--xmas">

    <!--__list = Element -->
    <li class="mainList__item">

        <!-- __itemLink = Elemnt -->    
        <a class="mainList__itemLink mainList__itemLink--isActive" href="/home">Accueil</a>

    </li>

    <!--__list = Element -->
    <li class="mainList__item">

        <!-- __itemLink = Elemnt -->
        <a class="mainList__itemLink" href="/home">Accueil</a>

    </li>

    <!--__list = Element -->
     <li class="mainList__item">

    <!-- __itemLink = Elemnt -->
    <a class="mainList__itemLink" href="/home">Accueil</a>

    </li>

</ul>

```

```css
.mainList {
    display: flex;
    justify-content: space-between;
        &--xmax{
            background: green;
        }
        &__item {
            list-style: none;
        }
        &__itemLink {
            color:red;
            &--isActive{
                color: white;
            }
        }
    }

```

## Pseudo attributs

Les Pseudo attrbuts 'befor' et 'after' permettent de créer des noeuds HTML et CSS.
Ils sont essentiellement utilisés pour ajouter des ornements, des décorations ... On peut bien entendu faire des animations avec, les positions par rapport à leur parent (relative / absolute).
* Ils doivent obligatoirement avoir un 'content:
* fin de s'afficher.

```html
<section class="cover">
    <h1 class ="cover__mainTitle">Présentation des pseudo-attributs</h1>
</section>
```

```css
.cover{
background: #FDFDFD;
padding: 20px;
&__mainTitle {
    text-align: center;
    font-size: 24px;
    color: green;
    position: relative
    &::before,
    &::after {
        position: absolute
        content: '';
        display : block;
        width : 50px;
        height: 50px;
        background : green;
        }
        &::before{
            left: 0;
        }
        &::after{
            right: 0;
        }
    }  
}
``
#REM, EM, %, VW sizing

#EM

```css
.cover{
    font-size: 100%;
&__mainTitle
    {
    font-size: .8em;
    }
}
````

### REM
*le REM est basé sur la taille de la racine (soit la balsie html) qui, par défaut a une valeur de 16 px. Afin d'éviter tout calcul, il est nécessaire de l'écraser en donnant une base de 10px soit 62,5%. Le REM est intéressant à utiliser si les media-queries emplayées sont en rem également. Cela vous permettre de garder des proportions égales lorsqu'on va redimensionner la page. Ses proportions seront également gardées quand l'utilisateur zoomera dans votre page.*

## vw

*Unités relatives à la taille de votre écran (peu importe le device)
Attention au VH et à son contenu. 100vh === 100vh quoi qu'il arrive.
VW : trés utiles pour les interfaces fluides.*


## flexboxgrid

*Les modificateurs réactifs permettent de spécifier différentes tailles de colonnes, décalages, alignement et distribution aux largeurs de la fenêtre xs, sm, md & lg*

  ``HTML
  <div class="row">
      <div class="col-xs-12
                  col-sm-8
                  col-md-6
                  col-lg-4">
          <div class="box">Responsive</div>
      </div>
  </div>
```

```css
    voir flexboxgrid.min.css
```
