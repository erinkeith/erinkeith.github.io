<h2>Arrays</h2>
<p><strong>Arrays</strong> allow us to store multiple values of the same data type in a group.</p>
<p>Let's say we're writing an application which needs to store 3 air temperature measurements throughout the day. It might make sense to create 3 <strong>scalar</strong> (single value) variables:<br>
  <code>double sunriseTemp, noonTemp, sunsetTemp;</code><br>
  <br>But what if we need to store measurements for every hour? Or every 15 minutes? There's got to be an easier way than declaring 24 or 96 different variables! Since they are considered <strong>composite</strong> (multiple values), <strong>arrays</strong> can come to the rescue!
</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <ul><li><a href="#declaration">Declaration</a></li>
        <li><a href="#element_access">Accessing an Element</a></li>
        <li><a href="#all_elements">Accessing All Elements</a></li>
        <li><a href="#macros">Macros</a></li></ul>
    <li><a href="#behavior">Behavior</a></li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<h4><a name="declaration">Declaration</a></h4>
<p>
  Array syntax is similar to variable syntax, with one important difference: <strong>size</strong>, which tells us how many values will be in our group. 
  The C <span title="coding rules for a programming language">syntax</span> for an array declaration statement must include a <a href="https://github.com/erinkeith/erinkeith.github.io/blob/main/135/topics/variables.md)">data type</a>, an identifier (or name), a size (between square brackets), and end with a semicolon.
</p>
<p>For example, if we need to save 24 temperature measurements in our program, we can declare an array:<br>
  <code>double temperatures[24];</code>
</p>
<h4><a name="element_access">Accessing Elements</a></h4>
<p>
  There are many benefits to grouping values, but we will still need to access each value (called an <strong><em>element</em></strong>) one at a time. To do that, we'll use the square brackets again but instead of having the size inside, it will be the location (called the <strong><em>index</em></strong>). <strong><em>Index</em></strong> values can be any integer value between <code>0</code> and one less than the original size (inclusive).
</p>
<p>
  <strong>WARNING!</strong> Index values always start at <code>0</code>. They <strong><em>do not</em></strong> start at <code>1</code> (and should almost never be used that way).
</p>
<p>
  For example, we can access the first value in the temperatures array through the following expression:<br>
  <code>temperatures[0]</code><br>
  <br>Expressions in this form can be used anywhere you would use a "regular" variable.<br>
  <code>temperatures[0] = 88.2</code><br>
  or<br>
  <code>printf("%.2lf", temperatures[1]);</code><br>
  or<br>
  <code>scanf("%.2lf", &temperatures[12]);</code><br>
  or<br>
  <code>sum += temperatures[23];</code><br>
  or<br>
  <code>temperatures[3] > 75</code><br>
</p>
<h4><a name="all_elements">Accessing All Elements</a></h4>
<p>
  Because <a href="#behavior">array names</a> only refer to the beginning memory address, they cannot be used on their own to refer to all of the values at once. If you want to do something like display all of the values in an array, each element <em>must</em> be accessed individually, using indexes (there is no shortcut for this).
</p>
<p>
  Since the index of the first element starts at <code>0</code>, the last index value is one less than the original size, and each element is at the next index value, arrays and for loops are best friends! For example:
<pre><code>for(index = 0; index < 24; index++){
    printf(".2lf ", temperatures[index]);
}</code></pre>
  would display all of the values in the <code>temperatures</code> array.
</p>
<h4><a name="macros">Macros</a></h4>
<p><strong>Macros</strong> are extremely useful for managing the size of <strong>arrays</strong>!</p>
  <img src="https://github.com/user-attachments/assets/3e9ef33f-3609-406d-81bc-44c3ea0237ec"><br>
<p>Now we only have to change <code>24</code> to <code>96</code> once at the beginning of the file if we measure every fifteen minutes instead of every hour.
</p>
<h3><a name="behavior">Behavior</a></h3>
<p>Before jumping into <strong>array</strong> behavior, it may help to take a refresher in <a href="https://github.com/erinkeith/erinkeith.github.io/blob/main/135/topics/variables.md#behavior">Variable Behavior</a>.</p>
<p>
  There's also no visible program behavior associated with array declaration. Again, the operating system is reserving memory, but instead of enough bytes for a single value, it reserves <strong>array size * number of bytes</strong> space. 
</p>
<p>
  It's pretty normal to start out thinking that an array name refers to the whole group of values, but it really only refers to the starting address of the array. Remembering that can help prevent bugs, especially when using arrays with <strong>functions</strong>.</p>
<p>
  To access individual elements, the compiler does some simple arithmetic with the index and the data type size to determine the correct location of that element. <img src="https://github.com/user-attachments/assets/5eaa63a8-8f91-400f-a4e9-a5e5612ee737"></p>
<p>
  This is why indexes always starts at <code>0</code>! The result of <strong>0 * number of bytes + starting address</strong> is the starting address and first element!
</p>
