# Awesome CSS Tips ![Awesome][awesome-badge]

#### Contents

- [Cursors](#cursors)
- [Smooth Scrolling](#smooth-scroll)
- [Truncate text](#truncate-text)

## Cursors

Did you know that you can use your own image, or even emoji as a cursor? 

```css
div {
    cursor: url('path-to-image.png'), url('path-to-fallback-image.png'), auto;
}
```

[Link to Codepen](https://codepen.io/denic/pen/bGVpOPj)

## Smooth Scroll

Smooth scrolling without #javascript, with just one line of CSS.

```css
html {
    scroll-behavior: smooth;
}
```

[Link to Codepen](https://codepen.io/denic/pen/bGVeYqN)

## Truncate text

Did you know that you can truncate text with plain CSS?

```css
.overflow-truncate {
    text-overflow: ellipsis;
}
```

[Link to Codepen](https://codepen.io/denic/pen/LYpZKMg)

[awesome-badge]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg

