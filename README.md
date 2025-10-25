## Overview

This project is a solution to the Social Links Profile challenge from Frontend Mentor. The goal was to build a centered profile card containing social media links and ensure it is fully responsive across different screen sizes.

-----

### The challenge

Users should be able to:

  * View the optimal layout for the component based on their device's screen size.
  * See hover and focus states for all interactive elements (buttons).

### Screenshot

<img width="711" height="820" alt="image" src="https://github.com/user-attachments/assets/853b2c2e-027e-44ba-9c0a-a059854f762c" />

-----

## My process

### Built with

  * **Semantic HTML5** markup
  * **CSS3** (for styling)
  * **CSS Custom Properties** (Variables)
  * **Flexbox** (for centering and button layout)
  * **CSS Media Queries** (for responsiveness)

### What I learned

The main learning curve and challenge in this project revolved around **CSS specificity** and implementing **responsive design** using media queries.

1.  **Specificity and Hover States:** I initially struggled to apply the hover effect on the buttons because the general background style (`.button .btn`) was **overriding** the hover style. I learned that the hover selector needed to be equally or more specific (e.g., `.button .btn:hover`) to successfully change the background color.
2.  **Media Queries for Layout Transition:** I learned how to use the `@media` rule to completely **re-flow the layout** for mobile devices. The key was switching the parent `.container` from a fixed `height: 100vh;` and `display: flex;` centering block, to a simple `display: block;` with `height: auto;` to allow the card to sit naturally within the mobile viewport.

<!-- end list -->

```css
/* Specificity fix for hover */
.button .btn:hover {
  background-color: var(--green);
}

/* Mobile layout transition */
@media only screen and (max-width: 600px) {
  .container {
    height: auto;
    display: block; /* Remove centering on mobile */
  }
  .card {
    width: 90%; /* Use percentage for mobile width */
    margin: 40px auto;
  }
}
```

### Continued development

I plan to continue focusing on more advanced **CSS transitions and animations** to make the hover state even smoother. I also want to practice implementing full **ARIA accessibility attributes** to make the interactive elements more robust for screen readers.

### Useful resources

  * [Frontend Mentor](https://www.frontendmentor.io/) - For the challenge and assets.
  * [MDN Web Docs](https://developer.mozilla.org/en-US/) - Invaluable resource for checking CSS syntax and specificity rules.

-----

## Author

  * **Frontend Mentor:** [@Khaisar-tech](https://www.frontendmentor.io/profile/Khaisar-tech))
 
-----

## Acknowledgments

Thanks to the Frontend Mentor community for providing clear guidelines and the design challenge.
