# Setting Up an Accessible Web Page: Keyboard Focus (A UX Accessibility Blog Post)
##### This UX Accessibility Blog Series, “Setting Up An Accessible Web Page,” will walk you through the basic elements of an accessible web page in hopes that you can take what you’ve learned an apply it to more complex pages. This blog series is loosely based on Heydon Pickering’s book “Inclusive Design Patterns: Coding Accessibility Into Web Design.”

<p>It’s important for your users to know where they are on your page at all times. This is especially true for your keyboard users, who often find it difficult to determine their location on a webpage. </p>

<p>Some elements, such as those that use divs, do not automatically receive keyboard focus or allow the user to navigate to them via the keyboard. Elements that are clickable but wouldn’t receive focus normally, such as infographic boxes in Ensemble, need to have the <code>tabindex=”0”</code> attribute added to them. Interactive elements should always be accessible. This way, keyboard users can navigate to them, see that they have received focus, and hit enter to navigate to the same place a mouse user would be able to navigate to. </p>

##### Note: This paragraph is in original blog post, but no longer reflects development practices that I believe are necessary and has been striked out for that reason.
<p><del>For elements that are mostly text, such as paragraphs, keyboard focus isn’t necessary, although some users may find it helpful. To make sure blocks of text receive focus, add the <code>tabindex=”0”</code> attribute to your paragraph tag. This will addition will only enhance the experience of your keyboard users without adding any unnecessary visual noise for your mouse users.</del></p> 

<p>Interactive elements that are written using semantic HTML have keyboard focus features baked in. Some examples of these would be <code>&lt;input type=”[text,email,tel,etc/checkbox/radio]”&gt;</code>, <code>&lt;button&gt;</code>, <code>&lt;select&gt;</code>, and <code>&lt;textarea&gt;</code>. Even though these elements are typically accessible, it’s important to always test your page for keyboard accessibility by tabbing through and making sure the tab order is logical.</p>
<p>Browsers typically implement their own focus styles, which are usually fuzzy blue halos or dotted lines. I like to use the browser default, but there are other ways to add focus styles to make focus more clear. It is important, however, to NEVER remove or add styles that contradict the browser’s default implementation of focus styles. These are very important and help a variety of users. </p>
<p>An example of an improved focus style would be <a href="https://www.gov.uk">gov.uk</a>’s implementation. They give the focused element a different background color from the rest of the text on the page.</p>