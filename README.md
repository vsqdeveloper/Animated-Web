# Animated-Web

What is Web Animations?
-----------------------

A new JavaScript API for driving animated content on the web. By unifying
the animation features of SVG and CSS, Web Animations unlocks features
previously only usable declaratively, and exposes powerful, high-performance
animation capabilities to developers.

What is in this repository?
---------------------------

A JavaScript implementation of the Web Animations API that provides Web
Animation features in browsers that do not support it natively. The polyfill
falls back to the native implementation when one is available.

Quick start
-----------

Here's a simple example of an animation that fades and scales a `<div>`.  
[Try it as a live demo.](http://jsbin.com/yageyezabo/edit?html,js,output)

```html
<!-- Include the polyfill -->
<script src="web-animations.min.js"></script>

<!-- Set up a target to animate -->
<div class="pulse" style="width: 150px;">Hello world!</div>

<!-- Animate! -->
<script>
    var elem = document.querySelector('.pulse');
    var animation = elem.animate({
        opacity: [0.5, 1],
        transform: ['scale(0.5)', 'scale(1)'],
    }, {
        direction: 'alternate',
        duration: 500,
        iterations: Infinity,
    });
</script>
```
