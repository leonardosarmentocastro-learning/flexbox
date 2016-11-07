# Flebox tutorial

### Lesson 1
1. Todo `<div>` quando nasce, nasce com `display: block;`.
2.  

### Lesson 2
1. The `flex-direction` property is responsible for setting the `main-axis`, which stands for the direction whose every flex item will be placed inside a given flexbox `container`.
The available values are:
```css
.container {
  /* ... */
  flex-direction: row;
  flex-direction: row-reverse;
  flex-direction: column;
  flex-direction: column-reverse;
}
```

`flex-direction: row;`: Is the default value for the flexbox system.
It means that the `.container` class will behave like a row to others `.container` classes.
The `main-axis` is a horizontal line, starting from the **left** to **right**.
<!-- The `cross axis` is a vertical line, starting from the top to bottom. -->

`flex-direction: row-reverse;`: The same behavior as the `flex-direction: row`, but instead, sets:
The `main-axis` is a horizontal line, starting from the **right** to **left**.
<!-- The `cross axis` remains the same, a vertical line starting from the top to bottom. -->

`flex-direction: column;`: Means that the `.container` class will behave like a column to others `.container` classes.
The `main-axis` is vertical line, starting from the **top** to **bottom**.
<!-- The `cross axis` is a horizontal line, starting from left to right. -->

`flex-direction: column-reverse;`: The same behavior as the `flex-direction: column`, but instead, sets:
The `main-axis` is vertical line, starting from the **bottom** to **top**.
<!-- The `cross axis` remains the same, a horizontal starting from the left to right. -->
