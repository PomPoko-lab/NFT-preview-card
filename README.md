# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it.

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid

### What I learned

- Implementing a footer with the use of flexbox.

```css
body {
  display: flex;
  flex-direction: column;
}

main {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
```

- Resizing in CSS grid.

```css
.card {
  width: 350px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-areas:
    "image image"
    "header header"
    "p p"
    "eth-num days-left"
    "footer footer";
}

.card > img {
  width: 100%;
  height: auto;
  /* grid-column: 1 / -1; */
  grid-area: image;
}
```

- More about CSS selector specificity

- Adding a color over the image was my biggest hurdle for this challenge. I ended up creating a div which allowed me to set as a relative position (I couldn't apply it to the image).

```css
.overlay:hover::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  top: -0.2em;
  left: 0;
  background-color: hsla(178, 100%, 50%, 0.6);
  border-radius: 0.5em;
  cursor: pointer;
  background-image: url("images/icon-view.svg");
  background-repeat: no-repeat;
  background-position: center;
}
```

### Continued development

One of my weaker areas is working with the pseudo-classes ::after and ::before. This allowed me to strengthen this and I hope to overcome this weakness soon.
