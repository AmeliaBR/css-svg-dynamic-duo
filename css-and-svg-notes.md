CSS and SVG — The Dynamic Duo!
==============================

Notes for a presentation by  
Amelia Bellamy-Royds  
at  
CSS Day 2016 (17 June)


## The Origin Story

In the beginning, there was HTML.

HTML, on its trusty steed, HTTP, set off across the infinite plains of the Internet, connecting the people through the magic of hyperlinks into a World Wide Web.

And the people loved HTML.  They loved HTML so much that their web browsers gave HTML great new powers to wield.

They gave it the `<font>` tag. And the `<center>` tag. And the `<big>` tag and the `<small>` tag. And the `<marquee>` tag, and the `<blink>` tag.

And HTML suffered, under the weight of all this presentational markup.

So HTML got a sidekick.  HTML got CSS.  Like a helpful squire, CSS took care of all the styling details so HTML could focus on the content.

But CSS, in this era, was still just a sidekick.  It only focused on helping HTML.  HTML was all about text, so CSS was all about styling text.  Sure, CSS showed up briefly in a dead-end story line involving XML on the web, but it really didn't involve any character development for CSS.  CSS was still all about styling text documents. 


## Enter SVG

SVG was a new kind of hero for the web.
A graphics language for the web.

It's skills were refined in a secret location under the instruction of SVGeesus, code-name Chris Lilley.  It was given powers never before seen on the web, like scalable gradients, transformable coordinate systems, and partial transparency.

And from the beginning, SVG had CSS.  SVG didn't _need_ CSS: SVG had the power to control all its styles from XML attributes if it needed to.  But CSS was always there as an extra option.  HTML's sidekick became SVG's sidekick, too.  

(HTML's other sidekick, JavaScript, also came along. But that's a whole other talk. This talk's about SVG and CSS.)

CSS did what it had always done, controlling text styling.  But it adapted, too.  Instead of laying out text blocks, CSS assigned fill colors and stroke-dashing patterns, and kept track of all the cross references between SVG's shapes and SVG's graphical effects.

SVG entered a world (wide web) not yet ready for it.  No one was quite sure where it fit.  Web browsers tried to contain with plug-ins and embedded objects, like Flash or Java Applets.  Some graphics software and XML document formats accepted basic SVG, but excluded CSS.

For a time, it wasn't clear if SVG would have a place on the web.

SVG was hanging around with a lot of XML languages, languages like XSLT and XFTO, and they just didn't seem to be going anywhere at all.  Except maybe print publishing.

SVG had also invested a lot of time adapting to tiny mobile devices, only to have them made obsolete by smartphones.

But CSS, CSS was still on the web.  CSS still had its old pal HTML.  The web isn't the web without HTML.  But HTML and the web, they needed a new look and some new moves to compete against smartphone apps.  And CSS had discovered all sorts of new styles from SVG.


## CSS does Graphics

So CSS and HTML moved forward without SVG.  CSS introduced its own gradients.  CSS introduced its own partial transparency.  It did this its own way, with new syntax, different from how SVG had created the same effects.

For SVG, it could have been the end. Left behind, out of date, another forgotten victim of the XML/HTML wars.

But HTML reached out a helping hand, allowing SVG code to be nested in an HTML 5 document without any need for those despised XML namespaces.

And CSS?  CSS came back to SVG.  But this time, not as a sidekick.  On the modern web, SVG and CSS are partners.

CSS Transforms, CSS Filters, CSS Masks and Clip-paths?  They're not replacements for SVG — they're extensions of it.  SVG effects that can be added to any element that CSS can style.  Simple effects can be defined solely in CSS syntax, but for fancier effects, SVG can be the sidekick to snazz up your CSS.

And with CSS stronger than ever, it can now do more to support SVG.  Now we've got CSS transitions and animations.  Now we've got CSS media queries and `@supports` rules.  Now we've got CSS web fonts and font features.  All of these new skills can now back up SVG in its own feature role.

It has not been easy.  Harmonizing SVG and CSS effects has resulted in a lot of bugs and confusion.  Specifications were written and browser code implemented without carefully considering all the edge cases.  CSS graphical effects need to work with both HTML and SVG, and that hasn't always been easy.

But it's happening.  The bugs are getting squashed.  The gaps are getting filled.  SVG and CSS are moving forward, together.  The Dynamic Duo, bringing easier interactive graphics to the web.


## What Can the Dynamic Duo Do For You?

Enough story time.  You're here to learn.  What you want to know, is: What can the dynamic duo do for _you_?

Each half of the team bring their own special skills.


What can SVG do that CSS can't do alone?

- Shapes.  Real shapes, with complex curves and multiple points.  It can draw shapes with a single element, no hacking about with borders and overflow and transforms and pseudo-elements.  This is SVG's specialty, it does it so much better than CSS can alone.

- Patterns.  Simple geometric patterns, or not-so-simple, without hacking around with gradients or extra image files.

- Dashed and dotted lines.  Full control over line dashing, including the famous "line that draws itself" effect.

- Text on a path.  Because straight lines are boring.

- Stroked and filled text.  Gradients, images, and patterns inside accessible, edit-able, and selectable text, or neat outlines without dozens of drop-shadows.

- Scale-to-fit graphics and text.  The famous SVG viewBox, which defines the amount extent of your graphic, so that the browser can adjust the scale to fit the available space.


What can CSS do that SVG can't do alone?

- Classes.  Classes are so much a part of CSS you don't even think about them anymore, but they save an awful lot of typing compared to styling elements individually.  Especially if you want to change styles later.

- Pseudo-classes.  Because even typing class names can be too much typing sometimes.

- Interactive pseudo-classes.  Our friends `:hover` and `:focus` and `:active` and `:target`.  Top-of-the-class classes.  Oh, the things they can do to create simple interactive graphical effects.  Especially when you add in…

- Transitions.  Smoothly change to a new state, regardless of where you started from.  Keyframe CSS animations are pretty cool too, but you can mostly do the same things with SMIL animation elements.  But transitions?  Trust me, transitions are amazing.  Trying to code simple reversible transitions with SMIL animation elements is not pretty.  Transitions even work with…

- Media queries.  Media queries are _awesome_.  They aren't quite as awesome in practice with SVG as they could be if you could control more of SVG layout from CSS but it will get better and I'll get to that in a bit.  (breathe)  But media queries in SVG are still pretty cool.

- `calc` functions.  Just a little bit of math can make responsive design so much easier when you're mixing percentages, absolute units, and font-relative or viewport units.  Calc functions will make SVG designs so much more flexible, especially once you can control more of SVG layout from CSS.  Which is coming, just not quite yet.

- Variables.  Still pretty new, but definitely extra-awesome.  CSS variables are going to be extra powerful in SVG because of how style inheritance works in SVG's `<use>` elements.


And then there are tricks that SVG taught to CSS, which CSS is making even better:

- Transforms.  2D Transformations have been a fundamental part of SVG layout from the beginning.  CSS extends that syntax with some 

- Clip-paths.  CSS had the `clip` property for years, but didn't know what to do with it.  Rather than trying to fix clip's bad syntax, CSS has now borrowed SVG's `clip-path`.  CSS clip-path added in shorthand shape functions so you don't need SVG markup for simple clipping effects, but you still _can_ use SVG for fancier effects.

- Masks.  Masks fade away text, shapes, and images according to the color or opacity of another graphic.  The new CSS syntax allows you to specify a mask image or CSS gradient, but you can also reference a more complex mask defined with SVG markup.

- Filters.  Blurs, drop-shadows, color manipulation: SVG filters are all kinds of fun.  CSS adds in shorthand notation for the most common effects but (are you seeing a pattern here?) you can still use SVG markup for fancier effects.

- Blend modes.  SVG Filters defined a way of setting blend modes to composite content into the background.  But graphics editors over-used the attribute that turned on background compositing, and web browsers responded by refusing to implement it because of performance reasons.  Which was very disappointing for a while, but now we're getting much easier to use blend modes.

Other SVG-crossover features have been proposed, but aren't in browsers yet.  That includes filled and stroked text as well as viewBox scaling.


## Do You Even SVG?

If you're only familiar with the HTML side of CSS, you'll need to keep a few things in mind when working with SVG:

- Box model, what box model?  There's only one box in an SVG graphic, and that's around the `<svg>` element that holds it all together.  Margins, padding, borders, and background don't have an effect on any other element, not even text elements.

- Position is absolute.  SVG elements are drawn exactly where you place them.  With very limited exceptions, they don't adjust to fit their container and they don't move over to make room for their siblings.   

- Units are arbitrary.  You can use CSS units in your designs, but SVG layout is built around an arbitrary, scalable "user unit".  A `viewBox` attribute tells the browser how many user units should fit in the available space, and they scale to fit.  And every other unit — px, points, inches, centimetres — scales to match. 

- Everything scales together.  Once you include that `viewBox` attribute, your SVG truly becomes a _scalable_ vector graphic — an image.  Like other images, if you change the width and height, the graphical content adjusts uniformly, including text size and stroke width.  We'll show some examples of changing this, but that's the default behavior

- `color` is just a variable.  The familiar CSS `color` property which changes the color of your HTML text, doesn't change anything in your SVG.  But that doesn't mean it's not useful.  Thanks to the `currentColor` keyword, you can use `color` as a variable to control all sorts of SVG properties, even in browsers that don't support CSS Variables yet.

- Bugs, bugs, everywhere.  This isn't a feature, it's just a fact of life.  You may say that bugs are a fact of CSS+HTML life, too, but it's worse with SVG.  Browsers and spec developers have spent less time working with SVG than with HTML, and even for brand new features they seem to put much less effort & testing in.  Welcome back to quirks mode, please test everything.

And if all that is not enough, you need to think about _how_ do you SVG?  Because there's more than one way to get an SVG into a web page, and each option changes how you can style it.


## All SVG Are Not Alike

There are three ways to SVG on the web:

- SVG as image.  A separate file, or maybe a data URI, that you use the same as you would any other image file:

  - `<img src="logo.svg" alt="SVG Logo" />`  
  - `background-image: url(logo.svg);`
  - No scripting!
  - No interaction!
  - No external stylesheets or images!
  - `<style>` works fine
  - `:target` and SVG views _should_ work
  - `@keyframes` and `<animate>` _should_ work
  - SVG text not accessible: use `alt`
  
- SVG as embedded object.  A separate file, or maybe a data URI, embedded as an independent, interactive document.

  - `<object data="chart.svg" type="image/svg+xml">fallback content</object>`
  - `<iframe src="chart.svg" >fallback content</iframe>`
  - `<embed src="chart.svg" type="image/svg+xml" />`
  - Scripting OK, _separate_ DOM
  - Interaction OK, events don't bubble out
  - Styles work, external files work, animation works
  - `:target` and SVG views work
  - SVG text _should_ be accessible
  
- Inline SVG.  SVG elements as children of your HTML elements, whether defined via markup or created via script.

  - `<figure><svg viewBox="0 0 100 100"><path ... /></svg></figure>`
  - `document.body.insertBefore( document.createElementNS(svgNS, "svg") );`
  - Scripting OK, _same_ DOM
  - Interaction OK, events bubble up
  - Styles affect entire document
  - Animation OK
  - `:target` based on main URL
  - No SVG views
  - Accessible SVG text
  
Some of the examples I'll show only work with SVG served certain ways.


## SVG and CSS in the Real World

What problems have the Dynamic Duo solved?  

- Easy Icon Color Themes

- Interactive Icons

- Graphical Form Validation

- Stateful SVG Animations

- Animated SVG Gradients & Patterns

- Hero Text Headings

- Responsive Logos

- Responsive Maps and Charts

- Fancy Filter Effects


## The Story's Not Over

There are still lots of obstacles to overcome.  There are bugs in browser implementations, there are bugs in the specs, there are browsers that haven't implemented specs yet, and there are specs that haven't been written yet.

Some new SVG+CSS adventures that should be possible in the next few years:

- Squashing the bugs in Transforms, Masks, Filters, Animations, and Transitions
- Better support for & animations of CSS Variables
- Wrapping text in SVG, using standard CSS inline layout properties
- Generated content (`::before` and `::after`) in SVG text
- SVG geometry, including path shape, in CSS
- SVG viewBox in CSS (and maybe for non-SVG elements)
- Motion path via CSS
- CSS images (including gradient functions) in SVG fill & stroke
- SVG paint servers (including new mesh gradients) in CSS background images
- SVG fill & stroke on any text
- Simple SVG images generated directly in CSS files

I can't promise which will come first, but all are being discussed or worked on now.  If something really excites you, please let browser developers & spec editors know!

## About Me

Amelia Bellamy-Royds

- Author & Web Standards Editor
- W3C Invited Expert, SVG and ARIA working groups
- [Books on SVG from O'Reilly Media](http://www.oreilly.com/pub/au/6190)
- [@AmeliasBrain](https://twitter.com/settings/account)
- <amelia.bellamy.royds@gmail.com>