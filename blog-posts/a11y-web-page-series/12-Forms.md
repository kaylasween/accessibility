# Setting Up an Accessible Web Page: Making Forms Accessible (A UX Accessibility Blog Post)
##### This UX Accessibility Blog Series, “Setting Up An Accessible Web Page,” will walk you through the basic elements of an accessible web page in hopes that you can take what you’ve learned an apply it to more complex pages. This blog series is loosely based on Heydon Pickering’s book “Inclusive Design Patterns: Coding Accessibility Into Web Design.”

<p>We’ve talked about what needs to be done to make forms accessible multiple times before, but since the relationship between these elements and accessibility/inclusivity is an important conversation to have, we’ll go over them (maybe in a bit more detail) again.</p>

<h2>Labels and Inputs</h2>
<p>Labels are used to identify all types of inputs and other form controls (such as <code>&lt;select&gt;</code>s or <code>&lt;textarea&gt;</code>s). Browsers allow the labels to become part of the clickable area that can be used to allow the input to receive focus. Labels also insure that assistive technologies correctly associate the label with the corresponding input field. </p>
<p>To associate a label with an input field, just set the for attribute in the label element to the id of the input it corresponds with. For example:</p>
<pre><code>&lt;label for=”firstName”&gt;First Name:&lt;/label&gt;
&lt;input type=”text” class=”form-control” name=”textbox” id=”firstName” /&gt;
&lt;label for=”pizza”&gt;Pizza Type:&lt;/label&gt;
&lt;select id=”pizza” name=”select”&gt;
  &lt;optgroup label=”Veggie Friendly”&gt;
    &lt;option value=”1”&gt;Cheese&lt;/option&gt;
    &lt;option value=”3”&gt;Veggie&lt;/option&gt;
  &lt;/optgroup&gt;
  &lt;optgroup label=”Meaty Pizzas”&gt;
    &lt;option value=”2”&gt;Pepperoni&lt;/option&gt;
    &lt;option value=”4”&gt;Sausage&lt;/option&gt;
  &lt;/optgroup&gt;
&lt;/select&gt;</code></pre>
<p>Text inputs can have an attribute called placeholder that you can use to give your users an example of what they should type in the input field. Never use the placeholder attribute instead of a label for the field. Using the placeholder attribute as the text input label can cause the user confusion since the placeholder disappears as soon as the user starts typing or as soon as the field receives focus. </p>

<h2>Radio Buttons and Checkboxes</h2>
<p>The best way to make radio buttons and checkboxes accessible is to use the <code>&lt;fieldset&gt;</code> and <code>&lt;legend&gt;</code> tags. The fieldset tag surrounds the group of radio buttons or checkboxes to show that those are the options for this particular group. The legend tag gives the fieldset a name to show the user what they’re picking. Screen readers repeat the legend text for each option in the fieldset, so it is important to keep your legend text as concise as possible.</p>
<pre><code>&lt;fieldset&gt;
  &lt;legend&gt;Pizza Type&lt;/legend&gt;
  &lt;input id=”cheese” type=”radio” name=”pizza” value=”cheese” /&gt;&lt;label for=”cheese”&gt;Cheese&lt;/label&gt;
  &lt;input id=”veggie” type=”radio” name=”pizza” value=”veggie” /&gt;&lt;label for=”veggie”&gt;Veggie&lt;/label&gt;
  &lt;input id=”pepperoni” type=”radio” name=”pizza” value=”pepperoni” /&gt;&lt;label for=”pepperoni”&gt;Pepperoni&lt;/label&gt;
  &lt;input id=”sausage” type=”radio” name=”pizza” value=”sausage” /&gt;&lt;label for=”sausage”&gt;Sausage&lt;/label&gt;
&lt;/fieldset&gt;</code></pre>
<p>There’s no point in using a fieldset without a legend, so always make sure the checkboxes or radio button groups warrant needing a legend. Sometimes the meaning of the group can be determined by the labels of the inputs alone, for example, radio buttons that say “yes” or “no” or a single checkbox that says “I agree to these terms” or “is billable”. In this case, a fieldset and legend shouldn’t be used because the purpose is clear and addition of a legend could just confuse the user.
The American Foundation for the Blind also suggests that you could include the fieldset into the label of the first option. This may be accessible, but requires the developer to add breakpoints (<code>&lt;br/&gt;</code>) between what should be the legend and the first option’s label. <code>&lt;br/&gt;</code> tags are hard to standardize across devices and browsers and are not semantic. Therefore, this option should not be used.</p>
