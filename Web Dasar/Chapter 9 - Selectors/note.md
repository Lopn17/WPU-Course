#Combinators

These slides explain CSS Combinators, which define the relationship between two or more elements in HTML so you can style specific elements based on where they live in the document tree.

Here is a simple breakdown of all 4 combinators shown in the slides, along with code examples:

1. Descendant Selector (Space)
Syntax: A B

How it works: Selects all B elements inside A, no matter how deeply nested they are (children, grandchildren, great-grandchildren).   
PNG

Example CSS:

CSS
div p {
  color: red;
}
HTML Impact:

HTML
<div>
  <p>Targeted (Direct Child)</p>
  section>
    <p>Targeted (Grandchild)</p>
  </section>
</div>
<p>Not Targeted (Outside div)</p>
2. Child Selector (>)
Syntax: A > B

How it works: Selects only direct children of A. Grandchildren and deeper levels are ignored.   
PNG
+ 1

Example CSS:

CSS
div > p {
  color: blue;
}
HTML Impact:

HTML
<div>
  <p>Targeted (Direct Child)</p>
  <section>
    <p>Not Targeted (Grandchild inside section)</p>
  </section>
</div>
3. Adjacent Sibling Selector (+)
Syntax: A + B

How it works: Selects exactly one B element that comes immediately after A at the exact same parent level.   
PNG

Example CSS:

CSS
h1 + p {
  font-weight: bold;
}
HTML Impact:

HTML
<h1>Heading</h1>
<p>Targeted (Immediately follows h1)</p>
<p>Not Targeted (Second paragraph)</p>
4. General Sibling Selector (~)
Syntax: A ~ B

How it works: Selects all B elements that appear anywhere after A, as long as they share the same parent level.   
PNG

Example CSS:

CSS
h1 ~ p {
  color: green;
}

HTML Impact:

HTML
<h1>Heading</h1>
<p>Targeted (Sibling after h1)</p>
<div><span>Random Div</span></div>
<p>Targeted (Another sibling after h1)</p>


Compound

This slide covers CSS Compound Selectors, which allow you to target elements by chaining multiple selectors together without spaces to make your selection much more specific.   Unlike standard combinators that target parent-child or sibling relationships across different elements, compound selectors apply to a single element that satisfies every condition at the same time.   How It Worksdiv.boxMeaning: Targets any <div> tag that also has the class box.   Key Difference:div .box (with space) = A .box element inside a <div>.div.box (no space) = A <div> that has the .box class itself..btn.primaryMeaning: Targets any element that has both the btn class AND the primary class simultaneously (class="btn primary").   Code ExampleCSS:CSS/* Compound Selector 1 */
div.box {
  border: 2px solid black;
}

/* Compound Selector 2 */
.btn.primary {
  background-color: blue;
  color: white;
}
HTML:HTML<!-- MATCHES div.box -->
<div class="box">I am a div with the box class.</div>

<!-- DOES NOT MATCH div.box (it's a section, not a div) -->
<section class="box">I have the box class, but I am a section.</section>

<!-- MATCHES .btn.primary -->
<button class="btn primary">I have BOTH classes!</button>

<!-- DOES NOT MATCH .btn.primary (missing the 'primary' class) -->
<button class="btn">I only have the btn class.</button>