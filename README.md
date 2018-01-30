# Documentation 

## Convention BEM

* B -> Block 
* E -> ELement
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
Ils sont essentiellement utilisés pour ajouter des ornements, des décorations ... On peut bien entendu faire des animations avec, les positions par rapport à leur parent (relative / absolute). **Ils doivent obligatoirement avoir un 'content: '''**afin de s'afficher.

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
    &::before,
    &::after {
        content: '';
        }
    }  
}

## Centrer en 3 lignes 