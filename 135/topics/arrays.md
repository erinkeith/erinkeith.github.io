<h2>Arrays</h2>
<p><strong>Arrays</strong> allow us to store multiple values of the same data type in a group.</p>
<p>Let's say we're writing an application which needs to store 3 air temperature measurements throughout the day. It might make sense to create 3 variables:<br>
  <code>double sunriseTemp, noonTemp, sunsetTemp;</code><br>
  <br>But what if we need to store measurements for every hour? Or every 15 minutes? There's got to be an easier way than declaring 24 or 96 different variables! Enter <strong>arrays</strong> to the rescue!
</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <ul><li><a href="#declaration">Declaration</a></li>
        <ul><li><a href="#array_names">Array Names</a></li></ul>
        <li><a href="#element_access">Accessing an Element</a></li>
        <li><a href="#all_elements">Accessing All Elements</a></li>
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
  a <a href="https://github.com/erinkeith/erinkeith.github.io/blob/main/135/topics/variables.md)">data type</a>, an identifier (or name), a size (between square brackets), and end with a semicolon.
</p>
<p>For example, if we need to save 24 temperature measurements in our program, we can declare an array:<br><br>
  <code>double temperatures[24];</code>
</p>
<h4><a name="element_access">Accessing Elements</a></h4>
<p>
  There are many benefits to grouping values, but we will still need to access each value (called an <strong><em>element</em></strong>) one at a time. To do that, we'll use the square brackets again but instead of having the size inside, it will be the location (called the <strong><em>index</em></strong>).
</p>
<p>
  <strong>WARNING!</strong> Index values always start at <code>0</code>. They <strong><em>do not</em></strong> start at <code>1</code> (and should almost never be used that way).
</p>
<p>
  For example, we can access the first value in the temperatures array through the following expression:<br>
  <code>temperatures[0]</code><br>
  <br>Expressions in this form can be used anywhere you would use a "regular" variable.<br>
  <br><code>temperatures[0] = 88.2</code><br>
  or<br>
  <code>printf("%.2lf", temperatures[1]);</code><br>
  or<br>
  <code>scanf("%.2lf", &amp temperatures[12]);</code><br>
  or<br>
  <code>sum += temperatures[22];</code><br>
  or<br>
  <code>temperatures[3] > 75</code><br>
  <br>These examples use random index values, but it's important to note that any integer value between <code>0</code> and one less than the original size (inclusive) is valid.
</p>
<h4><a name="array_names">Array Names</a></h4>
<p>
  While we tend to think of an array name referring to the whole group of values, it really only refers to the starting address of the array. 
</p>

<h4><a name="all_elements">Accessing All Elements</a></h4>
<p>
  Because the array name only refers to the beginning address, it cannot be used on its own to refer to all of the values at once. If you want to do something like display all of the values in an array, each element must be accessed individually, using indexes.<br>
  <br>Since the index of the first element starts at <code>0</code>, the last index value is one less than the original size, and each element is at the next index value, arrays and for loops go hand in hand! For example: <br>
  <pre><code>for(index = 0; index < 24; index++){
      printf(".2lf ", temperatures[index]);
  }</code></pre><br>
  would display all of the values in the <code>temperatures</code> array.
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
