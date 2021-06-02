# Breakpoints

Helper library for easily using breakpoints in SASS

## Example Usage

```scss
@use "@at-rules/breakpoints/src/index";

.body {
  @include breakpoints.breakpoint(mobile only) {
    color: red;
  }
}
```
### Output
```css
@media screen and (max-width: 576px) {
  .body {
    color: red;
  }
}
```
