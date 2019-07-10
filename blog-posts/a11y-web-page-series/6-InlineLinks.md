# Setting Up an Accessible Web Page: Inline Links (A UX Accessibility Blog Post)
##### This UX Accessibility Blog Series, “Setting Up An Accessible Web Page,” will walk you through the basic elements of an accessible web page in hopes that you can take what you’ve learned an apply it to more complex pages. This blog series is loosely based on Heydon Pickering’s book “Inclusive Design Patterns: Coding Accessibility Into Web Design.”

<h2>Links Should Be Underlined</h2>
<p>Conventionally, links have always been underlined. With the rise of frameworks and CSS usage, the amount of underlined links has started to decline in favor of using text-decoration:none on anchor tags and only changing the color of the link to differentiate it from other text. This is no good. Links should continue to be underlined for the sake of all of your users. 
It is hard for most users to differentiate a link from other text if they are different in color alone (especially colorblind users), but it also makes it more difficult for the user to determine if it is a link at all. Some users may think the different color is meant to show emphasis instead of denote a link.</p>
<p>Another problem is that some users may skim paragraphs in search of links. These links stand out more when they are both underlined and a different color from normal paragraph text. </p>
<p>The only exception to this is navigation bar links. Most people understand that your navbar will take them to other places on your website, so there’s no need to underline these links.</p>

<h2>Descriptive Links</h2>
<p>I touched on this in my Accessibility workshop and in a past blog post, “Four Benefits of Designing for All Users.”
It’s important to create links that concisely describe where the link points to. For example, if I was sending you to the blog post mentioned above, instead of saying “to visit my blog post, click here” I would say “Check out my blog post on designing for all users.” When the user clicks on “my blog post on designing for all users” they know exactly what to expect when they get there – blog post about designing for all users.</p>
<p>Some users elect for their screen readers to read through the links on the page as a way of skimming the text. If all of your links are just “click here,” “more,” “here,” etc., it makes it hard for screen reader users to know where the link will take them to. Hearing all of these links out of context can also be very confusing and disorienting for the user to experience. </p>
<p>Using the word “link” in your links also is redundant if you’ve already followed my recommendation above on underlining the link and used a <code>&lt;a href=””&gt;&lt;/a&gt;</code> tag to denote your link. The user will be able to tell that it’s a link based on the underline. A user who relies on a screen reader would know that it was a link because typically screen readers tell the user when they’ve encountered a link.</p>