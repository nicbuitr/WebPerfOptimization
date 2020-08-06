<p align="center">
    <a href="../../"><img src="img/logo.png" ></a>
</p>

## Information:

This repo is the final project of [Udacity's Critical Rendering Path course](https://www.udacity.com/course/ud884).
It is originally cloned from [Website Performance Optimization portfolio project](https://github.com/udacity/frontend-nanodegree-mobile-portfolio)
The purpose was to optimize this online portfolio for speed. In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques learned from the course.

It is built with Html, CSS, JavaScript and used Chrome DevTools to optimize the performance.

## Changes (DD/MM/AAAA)

- 31/07/2020 Initial Upload.
- 05/08/2020 index.html optimizations and README.md updates.

## How To View:

Just click here: [WebPerfOptimization](https://nicbuitr.github.io/WebPerfOptimization/).

## How To Download:

Just download or clone the repo:

    $ git clone https://github.com/nicbuitr/WebPerfOptimization.git

## Installation

Requirements:

- [Python](https://www.python.org/downloads/) in order to setup local server.	

Once Python is installed, just run:

    $ python -m SimpleHTTPServer 8080

Once its deployed go to http://localhost:8080/

## Optimization results

### index.html improvements

- Completed the metadata
- Added the async attribute for non-critical resources
  - favicon.ico
  - perfmatters.js
  - All the images
- Added the attribute media="print" to print.css
- Downloaded and added the fonts into the style.css
- Added the attribute font-display: swap; to the fonts to avoid FOIT and ensure that the text remains visible during webfont load
- Removed the Google Analytics script as it is not being used
- Removed a couple of CSS styles that were not being used
- Added h1 header for better semantics
- Added picture tag elements to use the right image sizes according to the viewport
- Added alt descriptions to all the images
- Resized and compressed pizzeria.jpg
- Moved the locally stored images to cloud storage to be able to request different sizes as parameter
- Added discernible names to all the anchor links
- Made sure that all links used https to avoid mixed content
- Made sure that all the images were displayed with appropriate sizes on all viewports
- Made sure that no errors were logged on the console

#### Desktop - Before/After

![PageSpeedInsights-Desktop-Base image](/audits/index/PageSpeedInsights-Desktop-Base.png?raw=true) | ![PageSpeedInsights-Desktop-Result image](/audits/index/PageSpeedInsights-Desktop-Result.png?raw=true)
:---:|:---:

![Lighthouse-Desktop-Remote-Base image](/audits/index/Lighthouse-Desktop-Remote-Base.png?raw=true) | ![Lighthouse-Desktop-Remote-Result image](/audits/index/Lighthouse-Desktop-Remote-Result.png?raw=true)
:---:|:---:

#### Mobile - Before/After

![PageSpeedInsights-Mobile-Base image](/audits/index/PageSpeedInsights-Mobile-Base.png?raw=true) | ![PageSpeedInsights-Mobile-Result image](/audits/index/PageSpeedInsights-Mobile-Result.png?raw=true)
:---:|:---:

![Lighthouse-Mobile-Remote-Base image](/audits/index/Lighthouse-Mobile-Remote-Base.png?raw=true) | ![Lighthouse-Mobile-Remote-Result image](/audits/index/Lighthouse-Mobile-Remote-Result.png?raw=true)
:---:|:---:

## Built with:

[![HTML](https://github.com/nicbuitr/f/blob/master/html5.png)](https://www.w3.org/html/) | [![CSS](https://github.com/nicbuitr/f/blob/master/css3.png)](https://www.w3.org/Style/CSS/)  | [![JavaScript](https://github.com/nicbuitr/f/blob/master/javascript.png)](https://developer.mozilla.org/en-US/docs/Web/JavaScript) | [![Visual Studio Code](https://github.com/nicbuitr/f/blob/master/vscode.png)](https://code.visualstudio.com/)
:---:|:---:|:---:|:---:


## License

MIT © [Nicolás Buitrago Castaño](https://github.com/nicbuitr)

## Original Repo's README with further instructions to setup remote server with NGROK

### Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
