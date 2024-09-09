<h2>Formatted IO</h2>
<p>The acronym "IO" stands for <strong>I</strong>nput <strong>O</strong>utput. "Formatted IO" refers to either arranging the structure of text for output or preparing to receive information as input. We'll be <em>output</em>ing information from our programs to the terminal window screen and <em>input</em>ing information into our program from the keyboard.</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <li><a href="#behavior">Behavior</a></li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<h4>The <code>stdio</code> Library</h4>
<p>Writing code to control information moving to and from other devices is far beyond the scope of this course. Luckily, someone else has done it for us! We can access this code through a <em>library</em> of code and <em>functions</em>. To use this library in our programs, we need to include a <em>preprocessor directive</em> above the main function:<br><br>
<code>#include &lt;stdio.h&gt;</code><br><br>
This tells the compiler to look in the library when it encounters certain functions. Forgetting it will lead to a compiler error:<br>
<img src="https://github.com/user-attachments/assets/a9b317c8-9632-43e8-90d1-a9f585b1b27b">
It might look intimidating, but I've outlined in red the helpful part of the error messages.<br>
</p>
<h4>Examples</h4>
<p>Once the correct library is included, you can use the <code>printf</code> function for output and the <code>scanf</code> function for input.<br><br>
The <code>printf</code> function sends everything in the <a href="#format_string">format string</a> to be displayed on the screen. For example, running a program with the line<br><br>
  <code>printf("Hello World!");</code><br><br>
would result in 
  <img src="https://github.com/user-attachments/assets/c3fd5561-f5bd-4d5c-82c4-897cfb148ca2"> 
being displayed to the screen.<br><br>
Notice how the very next thing (the terminal prompt) is displayed right next to our output! If we want it to display on the next line, we need to add some "blank space". The <strong>Enter</strong> key would do that if we were typing in a text document, but for formatted IO we need a special symbol, called the <em><strong>endline</strong></em> or <em><strong>newline</strong></em> character: <code>\n</code>. Adding that to the end of our format string changes the behavior of the program!<br><br>
  <code>printf("Hello World!<strong>\n</strong>");</code><br><br>
  produces <img src="https://github.com/user-attachments/assets/0c373b88-c4c9-4e65-934d-00a03db10928">. The <em><strong>endline</strong></em> character is one of many "escaped" characters that can be used in formatted IO: <a href="https://en.wikipedia.org/wiki/Escape_sequences_in_C#Escape_sequences">https://en.wikipedia.org/wiki/Escape_sequences_in_C#Escape_sequences</a>.</p>
<p>
  To include values, especially those stored in variables, a placeholder called a <a href="#conversion_specifier">conversion specifier</a> must be included in the <em>format string</em> and a corresponding variable (or value or expression) must be listed after of the format string.<br><br>
  In the <code>printf</code> function, the value is "read" and replaces the corresponding conversion specifier. For example:<br>
  <pre><code>int age = 44;
printf("Your age is %d.\n", age);</code></pre><br>
would display <img src=""> when the code is run.<br><br>
Notice that the value stored in the <code>age</code> variable is read and replaces the <code>%d</code> conversion specifier when the code is run. If you want to display more values, you must add more conversion specifiers and values:<br>
<pre><code>int age = 44;
printf("Your age is %d. You will be %d in 10 years\n", age, age + 10);</code></pre><br>
would display <img src=""> when the code is run. The first value <code>age</code> replaces the first conversion specifier and the second value <code>age + 10</code> replaces the second conversion specifier. <br><br>
</p>
<h4>Vocabulary</h4>
<p><a name="format_string">format string</a></p>
The <em>format string</em> starts with the first double quote inside the parenthesis and ends with the second one. The function uses what's inside the pair of double quotes to know how things should be input or output.
<p><a name="conversion_specifier">conversion specifier</a><br>
A <em>conversion specifier</em> is like a placeholder within the format string. It holds the place of whatever variable (or value) you want to replace it during runtime.
<table>
  <tr>
    <th>Data Type</th>
    <th>Conversion Specifier</th>
  </tr>
  <tr>
    <td><strong>int</strong></td>
    <td><code>%d</code></td>
  </tr>
  <tr>
    <td><strong>double</strong></td>
    <td><code>%lf</code></td>
  </tr>
  <tr>
    <td><strong>char</strong></td>
    <td><code>%c</code></td>
  </tr>
</table>
</p>
