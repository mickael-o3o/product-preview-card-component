# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [https://github.com/mickael-o3o/product-preview-card-component.git](https://github.com/mickael-o3o/product-preview-card-component.git)
- Live Site URL: [Add live site URL here](https://mickael-o3o.github.io/product-preview-card-component)

## My process

### Built with

- [Vue](https://vuejs.org)
- [Sass](https://sass-lang.com)
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

Using html picture element to create reposive image.

```html
<picture>
  <source media="(min-width: 27rem)" srcset="/images/image-product-desktop.jpg" />
  <source srcset="/images/image-product-mobile.jpg" />
  <img class="c-card__image" src="/images/image-product-mobile.jpg" alt="" />
</picture>
```

## Author

- Frontend Mentor - [@mickael-o3o](https://www.frontendmentor.io/profile/mickael-o3o)
