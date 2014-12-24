This is an optimized version of the "mobile portfolio" for Udacity's Frontend Web Developer Nanodegree.The master branch contains human-intelligible code, while the gh-pages branch has minified CSS and Javascript.Since most of the actual functionality was provided by the stock pages, actual changes to code may be sparser than you'd initially expect.

The live version of these webpages is available at http://gabekagan.github.io/frontend-nanodegree-mobile-portfolio; they use the minified gh-pages branch of the code.

There are several optimizations that should show up in every single page here:
- Images were optimized for size and compression, so that they would not be any larger than the maximum display size for the page. When I needed further optimizations, I fed them to kraken.io, which implements better compression techniques than my in-house image editing software.
- The included Google analytics scripts were made asynchronous, since they are not critical to rendering the page.
- Critical CSS was placed inline on the page, although I kept it inside style tags in the headers. Determining what CSS is "critical" is still sort of a stumbling point.
- Other CSS resources were loaded with an in-line Javascript function cribbed from Google's pagespeed tutorials; see the HTML pages for further information. A "scoped" style was used for webfonts; this is apparently on its way to being acceptable practice in HTML5.
- Any CSS and Javascript that wasn't inlined has been minified with Microsoft's Ajax Minifier. I considered setting up Grunt or Gulp scripts for this, but I decided to wait since I thought it would take more time than actually minifying.

Cam's Pizzeria was a task unto itself to optimize, and I have some concerns about the way this is to be graded according to the project rubric - see my thread at https://piazza.com/class/i0sf6tsmg0r7do?cid=968 for more details. I was able to optimize several points in the code to perform better (according to the included performance analytics), and as far as I can tell the behavior of the page is exactly the same as it was when I recieved it.

On a system with the following specs, the pizzeria page renders at a consistent 60 FPS even when scrolling or resizing.
Windows 8.1 + Google Chrome Canary 41.0.2258.2
Intel Core i5-3330 (Ivy Bridge) @3.0 Ghz
AMD Radeon R9 270X
6 GB (3x2) DDR3-1600 RAM
I do not know what sort of hardware the graders will benchmark my optimized page upon. I also have a decrepit laptop from 2009 or so that struggles with even the optimized pizza page, but its various problems significantly degrade performance. 

All pages score above 90 in the speed category for both desktop and mobile browsers in Google Pagespeed Insights. The pizzeria page has some user experience issues (and in fact I was NEVER able to get it to work in Firefox), but as far as I can tell, I am not required to optimize that.