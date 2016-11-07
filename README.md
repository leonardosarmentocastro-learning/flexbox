# Flebox tutorial

### Lesson 2
<!-- 1. Todo `<div>` quando nasce, nasce com `display: block;`. -->
<!-- 2.   -->

### Lesson 3
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

### Lesson 4
1. The main behavior of flexbox is to try to fit all the 'flexbox-item' into the container using the provided height/width.
If they can't do it, we need to tell him how to behave.
That is where the `flexbox-wrap` takes on.

The `flexbox-wrap` property by default, sets a `nowrap` value, which means that it will not try to wrap the elements inside a container to fit their content.
Which means that:
- In the actual scenario, we have a flexbox container within 10 `flexbox-item`(<div> elements).
- If we give a width of a 300px for all my `flexbox-item` inside a flex container(using the `.box` css class), by default, it will try to fit their children inside the container, but it will not be successful, and the result will be 10 `flexbox-item` with a *random* width to fit the container width, because the default value of `flexbox-wrap` is `nowrap`.
- Then, if we set the `flexbox-wrap` to `wrap`, it will put all the elements that it can on the current container(respecting the width of 300px), and the ones that can't be on the current line, will be placed on the next line.
E.g.: We have 10 `flexbox-item`, 300px each.
The `.container` is a `display: flex` of 1000px width.
With `flexbox-wrap; wrap`, it will put 3 `flexbox-item` in one line(divs 1, 2 and 3), break into another line, put more 3 on the next line(divs 4, 5 and 6), break into another line, put more 3 on the next line(7, 8 and 9), and finally break into another line and put the div 10.

The available values for `flex-wrap` are:
```css
.container {
  /* Default value is 'nowrap' */
  flex-wrap: nowrap;
  flex-wrap: wrap;
  flex-wrap: wrap-reverse;
}
```

2. If we sets the `flexbox-wrap` to `wrap-reverse`, it will change the `cross-axis` direction from top to bottom, to bottom to top, and all the `flexbox-item`(divs) will be reversed inside the `.container`.

3. Notice that every `.box` is a common box, so if you have some blank spaces at the edges of your boxes, you can set your `width` to `33.333333%` and see that is perfectly responsive and filling all the spaces on its edges.
