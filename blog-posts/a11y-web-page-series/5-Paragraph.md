# Setting Up an Accessible Web Page: The Paragraphs (A UX Accessibility Blog Post)
##### Originally posted on March 7, 2017 on [Software Unwound](https://softwareunwound.com/2017/03/07/setting-up-an-accessible-web-page-the-paragraph-a-ux-accessibility-blog-post/). Some of these will have references to class names in Bootstrap or Ensemble, FNC's style guide, and therefore may not be applicable to your project.

##### This UX Accessibility Blog Series, “Setting Up An Accessible Web Page,” will walk you through the basic elements of an accessible web page in hopes that you can take what you’ve learned an apply it to more complex pages. This blog series is loosely based on Heydon Pickering’s book “Inclusive Design Patterns: Coding Accessibility Into Web Design.”

<h2>Readability is Important</h2>
<p>It’s important for all of your content to be easy to read and concise. While there aren’t a lot of guidelines that say whether your paragraphs are accessible or not, there are a few things to keep in mind when writing content for a website:</p>
<h3>Keep it short</h3>
<p>If you can say something in 5 words instead of 20, say it in 5. People typically don’t like to read. They especially won’t read something if they think it’s too long. </p>
<h3>Passive Voice</h3>
<p>Don’t use passive voice unless absolutely necessary. Using the direct alternative tends to be easier to understand and shorter than its passive counterpart. </p>
<h3>Redundancy</h3>
<p>Saying the same thing twice in different ways is usually just a waste of effort. Users rarely will benefit from having the same thing said to them twice. (See what I did there?)</p>
<h3>Variety</h3>
<p>If your content is long, try to vary the length of sentences within your paragraphs and even the paragraph lengths themselves. Varying the length and sentence structure helps encourage your users to focus.</p>

<p>Readability also includes typefaces, spacing, type setting, line height, etc. For the sake of keeping this blog post under 50 pages and rehashing too many things that are already taken care of in Bootstrap and Ensemble, we’ll stick to some basic ways to help make your paragraphs more readable. </p>

<h2>Justification</h2>
<p>It may be tempting to use text-align: justify; on your paragraphs so that they’re all even on both sides. Though this works in print form, it doesn’t carry over to web as easily and is actually considered bad practice for web content. While it may make your paragraphs appear a little neater, the readability of your content suffers. Since justifying content tries to make all of the lines in your paragraphs equal, the spacing between words and breaking up words can be distracting for your user. Hyphenating words across lines isn’t even supported by some major browsers, and even if it is, the Javascript used to do it is extremely large because it needs to be able to reference every English word to find the best way to hyphenate them. </p>
<p>Your users will only care that your content is left justified. Jagged lines on the right side of your page should be the least of your worries when it comes to usability and readability.  </p>

<h2>Contrast</h2>
<p>Make sure your main content (excluding buttons, panel headings, callouts, and alerts found in Ensemble) has sufficient contrast. If you’re not sure if your content has sufficient contrast, check the background color and font color with WebAIM’s Color Contrast Checker. The contrast between the text on your page and the background is very important when ensuring your content is readable. 4.5:1 for large text (18+ point font, typically) and 7:1 for normal text (14+ point font, typically) or higher contrast is helpful for everyone.</p>
