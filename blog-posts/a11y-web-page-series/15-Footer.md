# Setting Up an Accessible Web Page: The Footer (A UX Accessibility Blog Post)
##### This post was never published, but originally written on February 13, 2017 and intended for FNC's developer blog, [Software Unwound](https://softwareunwound.com).

##### This UX Accessibility Blog Series, “Setting Up An Accessible Web Page,” will walk you through the basic elements of an accessible web page in hopes that you can take what you’ve learned an apply it to more complex pages. This blog series is loosely based on Heydon Pickering’s book “Inclusive Design Patterns: Coding Accessibility Into Web Design.”

<p>Page footers give the user additional information, usually about the company, such as copyright information, privacy statements, and terms of use. The footer of the page is denoted in <code>&lt;footer&gt;</code> tags in HTML5. According to the HTML5 specification, <footer> carries the implicit role of contentinfo as long as it isn’t a descendednt of an <code>&lt;article&gt;</code> or <code>&lt;section&gt;</code> element. However, it is important to explicitly add the role=”contentinfo” attribute because Internet Explorer does not fully support it. This may seem redundant, but it is the best practice to do this until all browsers fully support HTML5 and its accessibility features.</p>

<pre><code>&lt;div class="footer" role="contentinfo"&gt; //or &lt;footer class=”footer” role=”contentinfo”&gt;
   &lt;div class="container"&gt;
      &lt;div class="row"&gt;
         &lt;div class="col-md-10 col-sm-10 col-xs-10"&gt;
            &lt;ul class="list-inline legal-links"&gt;
               &lt;li&gt;Copyright © FNC, Inc. All rights reserved.&lt;/li&gt;
               &lt;li&gt;&lt;a href="Javascript:void(0)" onclick="window.open('http://www.fncinc.com/legal.aspx', 'FNCLegal', 'status=no,toolbar=no,location=no,menu=no,scrollbars=yes,screenX=0,screenY=0,width=792,height=567');">Privacy Statement&lt;/a&gt;&lt;/li&gt;
               &lt;li&gt;&lt;a href="Javascript:void(0)" onclick=""&gt;User Agreement&lt;/a&gt;&lt;/li&gt;
               &lt;li&gt;&lt;a href="Javascript:void(0)" onclick=""&gt;Rules &amp; Regulations&lt;/a&gt;&lt;/li&gt;
            &lt;/ul&gt;
         &lt;/div&gt;
         &lt;div class="col-md-2 col-sm-2 col-xs-2"&gt;
            &lt;a href="http://www.fncinc.com" target="_blank" class="img-fnc-logo" title="FNC, Inc homepage"&gt;&lt;/a&gt;
         &lt;/div&gt;
      &lt;/div&gt;
   &lt;/div&gt;
&lt;/div&gt; //or &lt;/footer&gt;</code></pre>

<p>The WAI-ARIA documentation describes the contentinfo role as “a large perceivable region that contains information about the parent document.” It goes on to say that any element with the <code>role="contentinfo"</code> should be treated as a navigational landmark and <code>contentinfo</code> should not appear more than one time on each page. </p>

<p>According to Bruce Lawson in his article “Why does HTML footer take role=”contentinfo”?”, contentinfo is a better semantic name for the information area that we call the "footer”. This could be why those who wrote the ARIA standards used <code>contentinfo</code> rather than <code>footer</code>. Web developers, however, have been using the class <code>.footer</code> for years in their mark-up. Therefore, the HTML5 specification accommodated for those who have been writing this way. </p>
<p>As previously mentioned in the “Accessible Images” blog post, make sure the logo in your footer has the correct alt text. The footer logo is typically an image link, so the <code>alt</code> text needs to tell the user where the link points to. In this case, the logo’s <code>alt</code> text should say something like “FNC, Inc Homepage”.</p>
