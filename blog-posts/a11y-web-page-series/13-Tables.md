# Setting Up an Accessible Web Page: Making Tables Accessible (A UX Accessibility Blog Post)
##### Originally posted on June 27, 2017 on [Software Unwound](https://softwareunwound.com/2017/06/27/setting-up-an-accessible-web-page-making-tables-accessible-a-ux-accessibility-blog-post/). Some of these will have references to class names in Bootstrap or Ensemble, FNC's style guide, and therefore may not be applicable to your project.

##### This UX Accessibility Blog Series, “Setting Up An Accessible Web Page,” will walk you through the basic elements of an accessible web page in hopes that you can take what you’ve learned an apply it to more complex pages. This blog series is loosely based on Heydon Pickering’s book “Inclusive Design Patterns: Coding Accessibility Into Web Design.”

<p>Tables that have specified rows or columns with header information about that particular row or column is considered a data table. Without a header, a table can be considered a formatting table. Personally, I don’t like to use tables to format content, but it’s not technically wrong. In this blog post, I’ll be focusing on making data tables accessible.</p>

<h2>General</h2>
<p>The simpler the table, the better. Simple tables are more easily understood than ones that are more complex (i.e. have multiple table headers or sections). Simpler is always better, but necessity will dictate how simple your data tables can be. However, it is recommended that you do your best to simplify your data tables as much as possible to be understood by a broader audience. </p>

<h2><code>th</code> and the <code>scope</code> attribute</h2>
<p>Sighted users have the luxury of being able to read data tables in any orientation the data may be displayed in. Screen reader users can only hear one cell at a time from left to right, top to bottom. This can easily cause confusion, especially if the table is complex or doesn’t use the right attributes in the markup to make it accessible. </p>

<p>Table headings allow sighted users to designate certain table cells as headers for the column or row it belongs to. 
The scope attribute is used to clarify the scope of a header cell and aid comprehension for those who use screen readers. It identifies whether the cell is a header for a row, column, group of columns, or group of rows. The scope attribute can also be used on <code>&lt;td&gt;</code> tags to denote the content of the cell is the header for a row. For example: </p>
<pre><code>&lt;table class="table table-bordered col-2-bloat"&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th scope="col"&gt;#&lt;/th&gt;
      &lt;th scope="col"&gt;Address&lt;/th&gt;
      &lt;th scope="col"&gt;GLA&lt;/th&gt;
      &lt;th scope="col"&gt;Sales Price&lt;/th&gt;
      &lt;th scope="col"&gt;MLS Number&lt;/th&gt;
      &lt;th scope="col"&gt;Service&lt;/th&gt;
  &lt;/tr&gt;
&lt;/thead&gt;
&lt;tbody&gt;
  &lt;tr&gt;
      &lt;td&gt;1&lt;/td&gt;
      &lt;td scope="row"&gt;380 Agate St&lt;/td&gt;
      &lt;td&gt;1250&lt;/td&gt;
      &lt;td&gt;$1,000,000&lt;/td&gt;
      &lt;td&gt;s709276&lt;/td&gt;
      &lt;td&gt;Desktop Appraisal&lt;/td&gt;
		&lt;/tr&gt;
		&lt;tr&gt;
      &lt;td&gt;2&lt;/td&gt;
      &lt;td scope="row"&gt;2160 S Coast Hwy&lt;/td&gt;
      &lt;td&gt;3205&lt;/td&gt;
      &lt;td&gt;$470,000&lt;/td&gt;
      &lt;td&gt;l40212&lt;/td&gt;
      &lt;td&gt;Desktop Appraisal&lt;/td&gt;
		&lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;</code></pre>

<p>Sometimes the scope may not need to be on the first element of the row. As in the example above, it would aid comprehension for the screen reader to read out the street address before every value rather than the number row it is.
Penn State’s Accessibility article titled “Tables for Data in HTML” has a great example for how table headings can aid comprehension of a visually impaired user. </p>
[picture]
<p>Assuming the markup is correct and uses scope as we showed in the code example above, the screen reader should read out the following:</p>
<blockquote>
“black, Spanish: Negro<br/>
black, French: noir<br/>
black, Irish: dubh<br/>
black, Welsh: du…”
</blockquote>

<p>This way, by the time the screen reader reads the last element of the row, the user is still able to remember what English term is being translated.</p>
