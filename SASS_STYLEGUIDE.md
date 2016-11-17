# Sass guidelines

## BEM-like naming

When creating styles for components, we use class names that follow
a convention adapted from the BEM (_Block_, _Element_, _Modifier_)
front-end methodology:

* Block: the class that will be applied to the component root.
* Element: a descendant element of the block or of another element.
* Modifier: a state or version of a block or element.

The CSS class names we use look like this:

```css
.block {}
.block__element {}
.block--modifier {}
```

* Two underscores for elements
* Two hyphens for modifiers
* One hyphen for multi-word names

## Example

```hbs
<div class="row">
  <div class="columns small-12">
    <div>
      nmbl-charts
    </div>

    <div class="nmbl-docs-page-header__title-wrapper">
      <h1 class='nmbl-docs-page-header__title'>
        <span class="nmbl-docs-page-header__title-slim">{{slimTitle}}</span>
        <span class='nmbl-docs-page-header__title-heavy'>{{title}}</span>
      </h1>
      <p class='nbml-docs-page-header__byline'>{{byline}}</p>
    </div>

    <div class="nmbl-docs-page-header__links">
      {{link-to 'Home' 'index'}}
      {{link-to 'Components' 'components'}}
    </div>
  </div>
</div>
```

```sass
.nmbl-docs-page-header {
  background-image: linear-gradient(153deg, #191919 0%, #2D6101 50%, #A0E32D 100%);
  box-shadow: 0 2px 4px 0 rgba(0,0,0,0.50);
  padding: 20px 0;
  color: rgba(255,255,255,0.9);

  &__title-wrapper {
    padding: 20px 0 40px;
  }
  
  &__title {
    font-size: 3.5em;
    margin-bottom: 0;
  }
  
  &__title-heavy {
    font-weight: bold;
    color: #6cd61a;
    text-shadow: 3px 2px 4px rgba(0, 0, 0, 0.25);
  }
  
  &__title-slim {
    font-size: 3.5em;
    margin-bottom: 0;
  }

  &__byline {
    font-size: 1.5em;
    line-height: 1;
    margin-bottom: 0;
  }
  
  &__links {
    margin-left: 0;
  }
}
```
