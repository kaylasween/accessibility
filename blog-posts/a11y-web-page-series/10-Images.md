# Setting Up an Accessible Web Page: Making Images Accessible (A UX Accessibility Blog Post)
##### Originally posted on June 20, 2017 on [Software Unwound](https://softwareunwound.com/2017/06/20/setting-up-an-accessible-web-page-making-images-accessible-a-ux-accessibility-blog-post/). Some of these will have references to class names in Bootstrap or Ensemble, FNC's style guide, and therefore may not be applicable to your project.

##### This UX Accessibility Blog Series, “Setting Up An Accessible Web Page,” will walk you through the basic elements of an accessible web page in hopes that you can take what you’ve learned an apply it to more complex pages. This blog series is loosely based on Heydon Pickering’s book “Inclusive Design Patterns: Coding Accessibility Into Web Design.”

<p>We’ve talked about what needs to be done to make images accessible multiple times before, but since the relationship between these elements and accessibility/inclusivity is an important conversation to have, we’ll go over them (maybe in a bit more detail) again.</p>
<h2>Why?</h2>
<p>As we’ve discussed in a previous blog post, images can help users comprehend what they are reading better by giving them something visual to associate with the text. For example, if you’re looking at houses to buy on Zillow, the pictures can help you decide if you are interested in the house even more than the text description alone of the house. </p>

<p>Visually impaired users do not have this luxury. They rely on only the text descriptions of pictures to help them gain a better understanding of what the images on a page are. Text alternatives are read by screen readers to the user in place of the image. Also, in the event that your user has a slow internet connection (out in the field, internet outage, etc.), the images on your page may not load at all, causing the alt text to be displayed in place of the images themselves. Adding alt text to your images also satisfies the first principle of web accessibility, perceivable. For these reasons, it is imperative that clear, descriptive alternative text be added to every image.</p>

<p>Every image should have an alt attribute.</p>

<h2>Links</h2>

<p>If your image also happens to be a link, make sure the alt text describes the link destination and not necessarily the image itself. For example, you have the FNC, Inc. logo on your page that links to fncinc.com, such as in your footer. </p>
[fnc logo]

<p>In this case, using “FNC, Inc. Logo” may not be very helpful. You’ll need to make sure the alt text says something like, “FNC, Inc Home Page”. According to Penn State’s accessibility article, “Image ALT Tag Tips for HTML,” providing a full description (saying “FNC, Inc. Logo. Directs to FNC home page”) is unnecessarily redundant. </p>
<h2>Purely Decorative Images</h2>
<p>Images that are used for purely decorative purposes, such as a horizontal line that separates two sections, don’t necessarily need a description. Penn State’s article uses a rainbow toolbar image as an example. </p>
 
<code>&lt;img src="examples/spectrumtooltip.gif" alt="A Rainbow line used as toolbar" /&gt;</code>
<p>Screen reader says "Rainbow line as a toolbar." If you have eighteen rainbow toolbars, the screen reader would repeat this eighteen times. This text is irrelevant to a screen reader user and increases reading time.</p>
<p>In this case, adding the description in the alt attribute could just annoy the user. However, every image must have an alt attribute, so we can add the alt attribute, but leave it equal to an empty string (<code>&lt;img alt="" /&gt;</code>). This satisfies the HTML requirement of having an alt attribute but also keeps screen readers from just announcing “image” when encountering an <code>&lt;img /&gt;</code> tag that doesn’t have an alt attribute.</p>
<p>Again, every image must have an alt attribute.</p>
