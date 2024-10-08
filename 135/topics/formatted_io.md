<h2>Formatted IO</h2>
<p>The acronym "IO" stands for <strong>I</strong>nput <strong>O</strong>utput. "Formatted IO" refers to either arranging the structure of text for output or preparing to receive information as input. We'll be <em>output</em>ing information from our programs to the terminal window screen and <em>input</em>ing information into our program from the keyboard.</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <li><a href="#behavior">Behavior</a>
    <ul><li><a href="#printf"><code>printf</code></a></li>
        <li><a href="#scanf"><code>scanf</code></a></li></ul>
    </li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<h4>The <code>stdio</code> Library</h4>
<p>Writing code to control information moving to and from other devices is far beyond the scope of this course. Luckily, someone else has done it for us! We can access this code through a <em>library</em> of code and <em>functions</em>. To use this library in our programs, we need to include a <em>preprocessor directive</em> above the main function:<br><br>
<code>#include &lt;stdio.h&gt;</code><br><br>
This tells the compiler to look in the library when it encounters certain functions. Forgetting it will lead to a compiler error:<br>
<img src="https://github.com/user-attachments/assets/a9b317c8-9632-43e8-90d1-a9f585b1b27b">
It might look intimidating, but I've outlined in red the helpful part of the error messages. Once the correct library is included, you can use the <code>printf</code> function for output and the <code>scanf</code> function for input.<br>
</p>
<h4>Vocabulary</h4>
<a name="format_string">format string</a>
<p>The <em>format string</em> starts with the first double quote inside the parenthesis and ends with the second one. The function uses what's inside the pair of double quotes to know how things should be input or output.</p>
<a name="conversion_specifier">conversion specifier</a>
<p>A <em>conversion specifier</em> is like a placeholder within the format string. It holds the place of whatever variable (or value) you want to replace it during runtime. Those variables are listed after the format string, separated by commas, and correspond conversion specifiers by position (first conversion specifier matches with first variable).<br><br> 
    <em><strong>The conversion specifier should match the data type of the value</strong></em>.</p>
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

<h3><a name="behavior">Behavior</a></h3>
<h4><a name="printf"><code>printf</code></a></h4>
<p>The <code>printf</code> function sends everything in the <a href="#format_string">format string</a> to be displayed on the screen. For example, running a program with the line<br>
  <code>printf("Hello World!");</code><br>
would result in<br>
  <img src="https://github.com/user-attachments/assets/d67b5f12-5a6a-4f70-afeb-3bb74d4afa78" width="200"><br>
being displayed to the screen.<br><br>
Notice how the very next thing (the terminal prompt) is displayed right next to our output! If we want it to display on the next line, we need to add some "blank space". The <strong>Enter</strong> key would do that if we were typing in a text document, but for formatted IO we need a special symbol, called the <em><strong>endline</strong></em> or <em><strong>newline</strong></em> character: <code>\n</code>.<br><br>
Adding that to the end of our format string changes the behavior of the program!<br>
  <code>printf("Hello World!<strong>\n</strong>");</code><br>
  produces<br>
    <img src="https://github.com/user-attachments/assets/7a06c887-af31-4d4d-9881-7e619a865b17" width="200">.<br>
    The <em><strong>endline</strong></em> character is one of many "escaped" characters that can be used in formatted IO: <a href="https://en.wikipedia.org/wiki/Escape_sequences_in_C#Escape_sequences">https://en.wikipedia.org/wiki/Escape_sequences_in_C#Escape_sequences</a>.</p>
<p>
  To display values, especially those stored in variables, a placeholder called a <a href="#conversion_specifier">conversion specifier</a> must be included in the <em>format string</em> and a corresponding variable (or value or expression) must be listed after the format string. In the <code>printf</code> function, the value is "read" and replaces the corresponding conversion specifier. For example:<br>
<pre><code>int age = 44;
printf("Your age is %d.\n", age);</code></pre>
would display<br>
<img src="https://github.com/user-attachments/assets/0e79f82d-7dc5-46a8-84b9-fe40fd0cbaf8" width="200"><br>
when the code is run.<br><br>
Notice that the value stored in the <code>age</code> variable is read and replaces the <code>%d</code> conversion specifier when the code is run. If you want to display more values, you must add more conversion specifiers and values:<br>
<pre><code>int age = 44;
printf("Your age is %d. You will be %d in 10 years\n", age, age + 10);</code></pre>
would display<br>
<img src="https://github.com/user-attachments/assets/1c69fc21-2a28-44f3-b8db-a136b358dac4" width="500"><br>
when the code is run. The first value <code>age</code> replaces the first conversion specifier and the second value <code>age + 10</code> replaces the second conversion specifier.</p>
<h4><a name="scanf"><code>scanf</code></a></h4>
<p>The <code>scanf</code> function also uses conversion specifiers in a format string, but <em><strong>NOTHING IN THE FORMAT STRING IS EVER DISPLAYED!</strong></em>. The conversion specifiers in the format string just prepare the program to receive information from the keyboard. That information is stored in variables listed after the format string. For example,<br>
<pre><code>int age;
scanf("%d", &amp;age);</code></pre>
would store whatever number the user types on the keyboard in the age variable.</p>
<p>A whole program should help see the difference!<br>
<img src="https://github.com/user-attachments/assets/38fc951a-657d-4f05-bc7f-32d53797375b" width="500"><br>
If we want to tell the user what to do, that text should be in a preceding <code>printf</code> statement (line 9). The <code>scanf</code> statement on line 10 will actually store the value in the <code>age</code> variable, after which point we can use that variable in the rest of our code (line 12).<br><br>
When we run our program, the first <code>printf</code> statement displays the prompt then the program stops<br>
<img src="https://github.com/user-attachments/assets/01703500-0dce-48ce-9af3-9e3ae77d5824" width="240"><br>
until the user enters a number followed by the Enter key (<strong>NOTE</strong>: for this class, we will always assume the user will enter a valid value).<br>
<img src="https://github.com/user-attachments/assets/dec9d196-0a54-4d9c-bc2d-e94b873d53a8" width="300"><br>

</p>
