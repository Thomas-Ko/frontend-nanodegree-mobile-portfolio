Optimizations
- Compress all images
- Create very small pizzeria image for index.html
- Minify css files
- Minify javascript files
- Add media="print" to print styles
- Remove webfonts
- Add async to google analytics script

** main.js pizza fixes **
- The changePizzaSizes function should not have been going through the dom that many times. It's better that I went through the dom once and set that to one variable, so in the for-loop, we don't need to query the dom all those times.
- I removed the determineDx function (what a bloated mess!). It did a whole lot of stuff that could've been simplified with less code. I changed to using a percent width instead of using pixels because there was too much going on with the pixels. Keep it simple!
- In the changeSliderLabel function, I set a variable called pizzaSize and set it to document.querySelector("#pizzaSize").innerHTML so I wouldn't need to traverse the DOM each time I moved the slider.