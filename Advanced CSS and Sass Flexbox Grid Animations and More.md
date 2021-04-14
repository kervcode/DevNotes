# Three Pillars to Write Good CSS And Build Good Websites


|Responsive Design|Maintainable and Scalable Code|Web performace|
|---|---|---|
|Fluid Layout|clean|Less HTTP|
|Media Queries|Easy to understand|Less code|
|Responsive images|Growth|Compress Code|
|Correct units|Reusable|Use a CSS proprocessor|
|Desktop-first vs mobile-first|How to Organize files|Less images|
|   |how to name classes|Compress images|
|   |How to structure HTML|


# How CSS Works Behind the Scenes
  ### How CSS is Parsed 
    - The Cascade and Specificity
    
    CASCADE : 
    DEF : Process of combining different stylesheets and resolving conflicts between different CSS rules
    and declarations, when more than rule applies to a certain element.
    
    IMPORTANCE  >  SPECIFICITY  > SOURCE ORDER
    
    |IMPORTANCE                       |
    | :---: |
    | 1. User !important declarations |
    
    
## What is Sass and How does it Work

Sass is a CSS preprocessor, an extension of CSS that adds power and elengace to the basic language.

## Main SASS Features

- Variables: for reusable values such as colors, font-sizes, spacing, etc
- Nesting: to nest selectors inside of one another, allowing us to write less code;
- Operators: for mathematical operations right inside of CSS;
- Partials and imports: to write CSS in different files and importing them all into one single file;
- Mixins: to write reusable peice of CSS code;
- Functions: similar to mixins, with the difference that they produce a value that can than be used
- Extends: to make different selectors inherit declarations that are common to all of them;
- Control directives: for writing complex code using conditionals and loops (not to covered in this course.)

### Mixins

- Declare mixing

```scss
@mixing mixinName {
    &::after {
        content: "";
        clear: both;
        display: table;
        }
      }
```

- Use mixing

```scss
   nav {
      margin: 30px;
      background-color: $color-primary;
      
      @include mixinName;
      }
```

- mixing with variables

```scss
@mixin style-link-text($color) {
    text-decoration: none;
    text-transform: uppercase;
    color: $color;
    }
```

        
