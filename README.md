# SASS

`sass scss/style.scss style.css` => compile scss to css
`sass scss/style.scss style.css -w` => compile scss to css and watch for changes
`sass scss:assets/css -w` => compile all scss files in scss folder to css and watch for changes

## Variables

```$primary-color: red;

h1 {
  color: $primary-color;
  font-size: 100px;
}
```

## Nesting

```nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li {
    display: inline-block;
  }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

## Parent Selector

```nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li {
    display: inline-block;
    a {
      display: block;
      padding: 6px 12px;
      text-decoration: none;
    }
    &:hover {
      background-color: #eee;
    }
  }
}
```

## @Extend

## @Mixin

## @if @else

## Partial

- using @import to import partials
- @use to import partials // recommended

## 7-1 Pattern
