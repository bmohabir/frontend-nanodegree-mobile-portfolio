## Website Performance Optimization portfolio project

To view the website, download the repository and run the webserver of your choice (ie. Python SimpleHTTPServer) in the root directory. Then simply access `index.html` or `views/pizza.html` at the server address using the web browser of your choice.

### Pizza Optimizations
#### main.js
 * cache document node lists in function scope variables (`pizzaContainers`)
 * simplify pizza size determination and remove unnecessary calculations (such as `deterineDx()`)
 * move one-time code outside of `for` loop in `changePizzaSizes()` and use loop only for batch setting pre-calculated style
 * move calculations that are unaffected by iterator outside of `for` loop and into variables in `updatePositions()`
 * trigger `requestAnimationFrame()` using scroll events to call `updatePositions()` to reduce frame timing negatively affecting scroll performance
 * use separate PNG graphics for background pizzas to reduce resize overhead
 * see comments in `main.js` for more info
#### pizza.html
 * remove inline style attributes and add them to `styles.css`
 * remove unused styles in `bootstrap-grid-lite.css` to reduce selector overhead