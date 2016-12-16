# stylus-code-style
My code style for stylus

### Brackets
Never use brackets when declaring selectors.

:heavy_check_mark: Good
```stylus
.good
  display block
  padding 10em
```

:x: Bad
```stylus
.bad {
  display block
  padding 10em
}
```

### Colons
Never use colons.

:heavy_check_mark: Good
```stylus
.good
  display block
  padding 10em
```

:x: Bad
```stylus
.bad
  display: block
  padding: 10em
```

### Colors
Always use colors inside variables.

:heavy_check_mark: Good
```stylus
$primary-color = #000

.good
  color $primary-color
  display block
```

:x: Bad
```stylus
.bad
  color #000
  display block
```

### Comment Space
Always put a space after line comments.

:heavy_check_mark: Good
```stylus
// Good comment
```

:x: Bad
```stylus
//Bad comment
```

### Depth Limit
Never indent selectors more than 3 times. Pseudo selectors like &:first-child or &:hover won't count towards the limit.

:heavy_check_mark: Good
```stylus
.list
  // some properties

  &__item
    // some properties

    &--highlighted
      // some properties
```

:x: Bad
```stylus
.list
  // some properties

  &__item
    // some properties

    &__media
      // some properties

      &--highlighted
        // some properties
```

### Extends
Always extend a placeholder using `@extends` instead of ``@extend`.

:heavy_check_mark: Good
```stylus
.good
  @extends $some-placeholder
```

:x: Bad
```stylus
.bad
  @extend $some-placeholder
```

### Indentation

:heavy_check_mark: Good
```stylus
.good
  display block
  padding 10em
```

:x: Bad
```stylus
.good
    display block
    padding 10em
```

### Leading Zero
Never use unnecessary leading zeroes on decimal points.

:heavy_check_mark: Good
```stylus
$primary-color = rgba(0,0,0,.87)
```

:x: Bad
```stylus
$primary-color = rgba(0,0,0,0.87)
```

### None Value
Always use `0` instead of `none`.

:heavy_check_mark: Good
```stylus
.good
  border 0
```

:x: Bad
```stylus
.bad
  border none
```

### Paren Space
Never use extra spaces inside parens.

:heavy_check_mark: Good
```stylus
my-mixin($my-param)
```

:x: Bad
```stylus
my-mixin( $my-param )
```

### Placeholders
Always extend placeholders vars.

:heavy_check_mark: Good
```stylus
.good
  @extends $placeholder
```

:x: Bad
```stylus
.bad
  @extends .some-class
```

### Quotes
Always use single quotes.

:heavy_check_mark: Good
```stylus
.good
  font-family 'Roboto', sans-serif
```

:x: Bad
```stylus
.bad
  font-family "Roboto", sans-serif
```

### Semicolons
Never use semicolons.

:heavy_check_mark: Good
```stylus
.good
  display block
  padding 10em
```

:x: Bad
```stylus
.bad
  display block;
  padding 10em;
```

### Property Order
Sort properties in alphabetical order.

:heavy_check_mark: Good
```stylus
.good
  display block
  left 0
  position relative
  text-align center
  top 0
```

:x: Bad
```stylus
.bad
  position relative
  top 0
  left 0
  text-align center
  display block
```

### Stacked Properties
Always put properties on new lines.

:heavy_check_mark: Good
```stylus
.good
  display block
```

:x: Bad
```stylus
.bad {display: block}
```

### Variables
Always name a variable with the lowercase-dash convention and prefix it with
a dollar.

:heavy_check_mark: Good
```stylus
$gutter-width = 10em
$cols-number = 12
```

:x: Bad
```stylus
$gutterWidth = 10em
cols-number = 12
```

### Zero Units
Never use units after `0` values.

:heavy_check_mark: Good
```stylus
.good
  margin 0
```

:x: Bad
```stylus
.bad
  margin 0px
```
