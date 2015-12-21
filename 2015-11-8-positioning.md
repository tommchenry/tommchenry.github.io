---
layout: post
title: Static, Fixed, Absolute Have New, Worse Meanings
---

#CSS Concepts

##Static, Fixed, Absolute Have New, Worse Meanings

####November 8, 2015

For me, one of the most difficult concepts to grasp in CSS is positioning. In general, the concept isn't difficult: positioning just refers to how parts of your HTML page should be displayed on the page. Position has four other properties associated with it: top, right, left and bottom. Adding values to these will adjust the positioning of the element. Just how it adjusts the position and what it positions them relative to depends on what value the position property has.

In theory, you can use positioning to make any part of your HTML fall anywhere you need it to on the page. In practice, this is only possible if you know exactly what you're doing with the different possible values for the position property, and keeping them separate is where things get confusing. For one thing, "absolute," "fixed," and "static" are usually mean the same thing, but here mean three completely different things.

**Static Positioning

Static positioning is the easiest to understand because it's the most basic. HTML elements position as static by default, so if you haven't ever set position values before, you've been working with static positioned elements. An element with static positioning isn't affected by top, right, left and bottom. Think of static as locking the element in place.

**Relative Positioning

Relative positioning is the first position value to be affected by top, right, left and bottom. If you set position to relative, any values for top, right, left and bottom will nudge the HTML element that much from where it would otherwise appear if it still had static positioning. You're moving the HTML element relative to where it should appear.

**Fixed Positioning

Fixed positioning doesn't take an element's original position into account at all. Instead, fixed position fixes the element in place on the browser window, even if the page is scrolled. The values of top, right, left and bottom now are used to glue the element that much from the top, left, right, and bottom of the window itself. So a position:fixed; element with a top value of 0 will be glued to the top of the browser window and stay there, even if the user scrolls down the page.

**Absolute Positioning

Absolute positioning is the final position value and probably the most difficult to understand. Absolute positioning is the only position value to work off of the position values of other HTML elements on the page. For the first time, you have to think about the HTML elements that are wrapping the HTML element whose position you're adjusting. This means talking about how elements have parents.

Every HTML element on a page has a parent element, and the easiest way to think about this concept is that an element's parent is the element that's wrapping it. On a simple page with only a `<main>` element, that `<main>` element's parent is the `<body>` tag, which wraps the whole page's content.

Now, if an element's parent has a position value that is anything except static (remember: static just means the default position value), setting position:absolute; will adjust that element's position relative to the parent element.

Remember how in fixed positioning, you were positioning the element relative to the browser window? Absolute positioning works as though the parent element is the browser window. So if you had a `<main>` element with a fixed position at the top of the screen, and inside it you had an `<article>` element with a position:absolute and bottom:0, the `<article>` element is going to stick to the bottom of the `<main>` element. If you set right to 0, the `<article>` element would stick to the right side of the `<main>` element.

Absolute positioning is like trapping an element inside its parent like an element-based prison cell. Where relative and fixed positioning can move your elements anywhere you want them to go, absolute positioning makes sure they're only ever moving around inside their parent element.