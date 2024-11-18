<br>

# <div align="center">Flex or Grid</div>

## Flex Approach

This property is used along with the display property and its value `flex`, the property flex is a shorthand of: **flex-grow, flex-shrink and flex-basis**.

When the element doesn't have a custom width and its parent have `display: flex`, this element will have a width of the maximum content of the element. If we want the elements inside parent element take the whole space we can use `flex-grow: 1` but for responsive design is better to set `flex-shrink` and `flex-basis` as well.

For this reason we can use the shorthand `flex`

```css
.parent {
  display: flex;
}

.child1 {
  flex: 1; /* flex-grow: 1; flex-shrink: 1; flex-basis: 0; */
}

.child2 {
  flex: 2; /* flex-grow:2; flex-shrink: 1; flex-basis: 0; */
}
```

## Grid Approach

We can use the display property with grid as value and then add the `grid-template-column` or `grid-template-row` property to get a similar result to `flex property`, but for images, both must add some lines of CSS more.

```css
.parent {
  display: grid;
  grid-template-columns: repeat(2, 1fr); /* 1fr 1fr */
  grid-template-rows: 100%;
}
```

<br>

#### **_Examples:_**

<details>
    <summary>For boxes</summary>

<br>

Flex Approach

```html
<section style="display: flex; height: 200px">
  <div style="flex: 1; background: red"></div>
  <div style="flex: 1; background: blue"></div>
  <div style="flex: 1; background: green"></div>
</section>
```

<br>

Grid Approach

```html
<section style="display: grid; grid-template-columns: repeat(3, 1fr); grid-template-rows: 100%; height: 200px">
  <div style="background: red"></div>
  <div style="background: blue"></div>
  <div style="background: green"></div>
</section>
```

<br>

</details>

<details>
    <summary>For images</summary>

<br>

For images, we should **_always_** add a picture tag (it's not necessary), but for a Flex Approach we must add it.

```html
<section style="display: flex; height: 200px">
  <picture style="flex: 1">
    <img src="./img1.jpg" alt="#" />
  </picture>

  <picture style="flex: 2">
    <img src="./img2.jpg" alt="#" />
  </picture>

  <picture style="flex: 3">
    <img src="./img3.jpg" alt="#" />
  </picture>
</section>

<article>Random Text below section parent container</article>
```

<br>

Grid Approach

```html
<section style="display: grid; grid-template-columns: 1fr 2fr 3fr; grid-template-rows: 100%; height: 200px">
  <picture>
    <img src="./img1.jpg" alt="#" />
  </picture>

  <picture>
    <img src="./img2.jpg" alt="#" />
  </picture>

  <picture>
    <img src="./img3.jpg" alt="#" />
  </picture>
</section>

<article>Random Text below section parent container</article>
```

<br>

</details>
