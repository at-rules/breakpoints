# Breakpoints

**WIP**
Helper library for easily using breakpoints in SASS

## Variables Available

Below are the default variables, as this package uses @at-rules/breakpoints those variables will also be available

```scss
$breakpoints: (
  "mobile": 320px,
  "phablet": 425px,
  "tablet": 768px,
  "desktop": 1024px,
) !default;
```

## Usage

You can use all of the above breakpoints mixed with a term (up, down and only)
this will provide you with different min - max breakpoints on compile.

### Example One

```scss
@use "@at-rules/breakpoints/src/index" as *;

.body {
  @include breakpoint(mobile only) {
    color: red;
  }
}
```

```css
@media screen and (max-width: 576px) {
  .body {
    color: red;
  }
}
```

### Example two

```scss
@use "@at-rules/breakpoints/src/index" as *;

.body {
  @include breakpoint(tablet down) {
    color: red;
  }
}
```

```css
@media screen and (max-width: 768px) {
  .body {
    color: red;
  }
}
```

### Example three

```scss
@use "@at-rules/breakpoints/src/index" as *;

.body {
  @include breakpoint(phablet only) {
    color: red;
  }
}
```

```css
@media screen and (min-width: 425px) and (max-width: 768px) {
  .body {
    color: red;
  }
}
```
