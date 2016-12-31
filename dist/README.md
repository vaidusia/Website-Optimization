## Website Performance Optimization portfolio project

My challenge is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).


### Getting started


There are two directories: source and distribution
Source (src) is optimized code, in a readable format, distribution (dist)- optimized and minified code.

1. Download this repository to your local computer
2. o inspect the site on your phone, you can run a local server

```bash
$> cd /path/to/your-project-folder
$> python -m SimpleHTTPServer 8080
```
3. Open a browser and visit localhost:8080
4. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

``` bash
$> cd /path/to/your-project-folder
$> ngrok http 8080
```

5. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)


####Part 1: Optimize PageSpeed Insights score for index.html
What has been done

* Identified and performed optimizations to achieve a PageSpeed score over 90
* Resized and compressed images to reduce bandwidth
* Inlined above-the-fold CSS 
* Compressed HTML file

####Part 2: Optimize Frames per Second in pizza.html
What has been done

* Added "@media all" to views/css/style.css
* Set .mover to "will-change: transform;" to reduce repainting time to views/css/style.css:
* Changed maximum amount of pizzas in addEventListener
* Changed all uses of querySelectorAll to getElementsByClassName
* Moved variables: "items" and "pizzasDiv", out of the function updatePositions() and out of loop, accordingly
* Changed function changePizzaSizes(size) to reduce time of resizing pizzas in views/pizza.html to < 5ms


