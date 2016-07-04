# Website Performance Optimization portfolio project

## To run

Open portfolio site on [GitHub Pages](https://jnpj1.github.io/performance-optimization).  The pizza.html site can be accessed through clicking on the pizza site image in the portfolio.

### Optimizations to achieve Google PageSpeed Insight scores of 95/100 for mobile and 96/100 for desktop:

1. Remove link to googlefonts in index.html and replace font with alternate in CSS.
2. Added media attribute with print value in link print.css.
3. Optimized images.
4. Minified and inlined style.css.
5. Moved scripts from beginning to end of body.
6. Added async attribute to perfmatters.js and google analytics script tags.


### Optimizations to achieve 60fps when scrolling in pizza.html:

1. Generation of 'items' object moved to DOMContentLoaded event listener so as to occur just once.
2. Created a variable to store the relative scroll position outside of the for loop in updatePositions.
3. Separated functionality of for loop within updatePositions into two for loops.  Phase values are calculated in the first and stored in an array.  Positions are updated in the second.
4. Optimized loop for generation of moving pizzas in the DOMContentLoaded event listener.  The number of pizzas is dynamically calculated and generated based upon browser window height.


### Optimizations to reduce pizza resize time to less than 5ms in pizza.html:

1. Create variable pizzaImageList within changePizzaSizes function to store object of pizza containers.
2. Move dx and and newWidth variables outside of the for loop within changePizzaSizes.
3. Perform resize calculations just once based upon dimensions of first pizza, since all pizzas are always the same size as one another.