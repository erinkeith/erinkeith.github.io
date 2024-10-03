<h2>Arrays</h2>
<p><strong>Arrays</strong> allow us to store multiple values of the same data type in a group.</p>
<p>Let's say we're writing an application which needs to store 3 air temperature measurements throughout the day. 
  It might make sense to create 3 variables:<br>
  <code>double sunriseTemp, noonTemp, sunsetTemp;</code><br>
  <br>But what if we need to store measurements for every hour? Or every 15 minutes? There's got to be an easier way than declaring 24 or 96 different variables!<br>
  <br>Enter <strong>arrays</strong> to the rescue!
</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <ul><li><a href="#declaration">Declaration</a></li>
        <li><a href="#element_access">Accessing Elements</a></li>
        <li><a href="#macros">Macros</a></li></ul>
    <li><a href="#behavior">Behavior</a>
    </li>
    <li><a href="#metaphor">Metaphors</a></li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<h4><a name="declaration">Declaration</a></h4>
<p>
  Array syntax is similar to variable syntax, with one important difference: <strong>size</strong>, which tells us how many values will be in our group. 
  The C <span title="coding rules for a programming language">syntax</span> for an array declaration statement must include 
  a <a href="https://github.com/erinkeith/erinkeith.github.io/blob/main/135/topics/variables.md)">data type</a>, an identifier (or name), a size (between square brackets), and end with a semicolon.<br>
  <br>For example, if we need to save 24 temperature measurements in our program, we can declare an array:<br><br>
  <code>double temperatures[24];</code>
</p>
<h4><a name="element_access">Accessing Elements</a></h4>
<p>
  There are many benefits to arrays, many of which our outlined below, but we're still going to have to access each value (called an <strong><em>element</em></em></strong>) one at a time. 
  To do that, we'll use the square brackets again but in a different way:<br>
  <code>temperatures</code>
</p>
<h4><a name="macros">Macros</a></h4>
<p><strong>Macros</strong> are extremely useful for managing the size of <strong>arrays</strong>!<br>
  <img src="https://github.com/user-attachments/assets/3e9ef33f-3609-406d-81bc-44c3ea0237ec"><br>
  Now we only have to change <code>24</code> to <code>96</code> once at the beginning of the file if we measure every fifteen minutes instead of every hour.
</p>
<h3><a name="behavior">Behavior</a></h3>
<p>
  Before jumping into <strong>array</strong> behavior, it may help to take a refresher in <a href="https://github.com/erinkeith/erinkeith.github.io/blob/main/135/topics/variables.md#behavior">Variable Behavior</a>.<br><br>
  
</p>
[<a href="#note">1</a>]
<h3><a name="metaphor">Metaphors</a></h3>

<a name="note">1</a>. Explanation.<br>
