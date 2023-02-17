# Frontend Mentor - Stats preview card component

**Table of Contents**

- [Frontend Mentor - Stats preview card component](#frontend-mentor---stats-preview-card-component)
  - [Welcome! 👋](#welcome-)
  - [Links](#links)
  - [Overview](#overview)
  - [The Problems and Solutions](#the-problems-and-solutions)
  - [Acknowledgments](#acknowledgments)
  - [Author](#author)

## Welcome! 👋

Welcome to my solution page. I hope you'll find some good implemantions for this project here.

![Stats preview card component](./design/desktop-preview.jpg)

## Links

- [My Live Site](https://adonmez04.github.io/FEM-3-Stats-preview-card-component-v1/)

- [My Solution Page](https://www.frontendmentor.io/solutions/fem3statspreviewcardcomponent-v11-xAYXaBsNli)

- [The Challenge Page](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62)

## Overview

Almost every project has a unique problem for improving our coding skills. Problems sound terrible but we should solve them for the our learning process. It would be better if it was the official solution page. However, we can look at other solutions and collect some good implementations. Maybe that's why there aren't any official solution pages. We should spend time to check others code thus we'll understand what is the solution.

## The Problems and Solutions

1. First, we should change the direction for mobile and desktop versions.
2. Secondly, we should add a background-color to the image.

Both of them are good problems because we'll encounter these problems a lot.

1. For first problem, I used a CSS Grid and added it to the classes. And then in the media query, I changed to the direction.

```css
/* The Grid Template - For The Mobile */
.grid {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto 1fr;
}

/* The Grid Template - For The Desktop*/
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr;
}
```

I also changed the order of flex-items in the media query.

```css
.content-box {
  /* Changing the order */
  grid-column: 1;
  grid-row: 1;
}

.img-box {
  /* Changing the order */
  grid-column: 2;
  grid-row: 1;
}
```

I didn't set the layout size so I gave width and height values to the image-area. I'm not sure if it is a best practice but I didn't set the layout without any size values. I should focus on that.

```css
.img-box {
  width: 33.75rem;
  height: 27.875rem;
}
```

2. For the second problem, I used ::after pseudo-element to add a background-color to the image.

```css
.img-box::before {
  content: "";
  display: block;
  width: 20.4375rem;
  padding-bottom: 15rem;
  background-color: rgba(170, 92, 219, 0.9);
  mix-blend-mode: multiply;
}
```

I used padding-bottom instead of height. Because padding-bottom value will be calculated as the height value. Basically, I gave width and height values to the background-color and used them before the image. It solved the problem but I'm also not sure about them if it is best practice because I had to do a static unit. I'll look into other people's code for a better solution.

3. For the bonus problem in this project, I should use `aria-label` because I manipulated the html file from the css but there aren't any semantic tags in html. Thus, I used `aria-label` for accessibility.

```html
<div
  class="img-box"
  role="img"
  aria-label="A group of women in the work."
></div>
```

I'm sure I'll change my code based on some good comments and implementations. I'm in the learning process and this is so natural. For now this is my stable solution and I'm okay with that. If I make any major changes to my code, I'll create a new repository for the new version of the solution so you can check the solutions according to the current commit.

<!-- ## My Questions -->

<!-- ## Feedbacks -->

<!-- ## Good Implementations -->

<!-- ## Useful Resources -->

<!-- - [The link title](The link) -->

## Acknowledgments

- Thanks Hassia Issah for your helpful comment. [@Hassiai](https://www.frontendmentor.io/profile/Hassiai)

## Author

- My Frontend Mentor Profile Page - [@adonmez04](https://www.frontendmentor.io/profile/adonmez04)
- For those of you reading this, have a nice day!
