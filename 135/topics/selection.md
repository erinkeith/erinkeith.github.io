<h2>Selection</h2>
<p><strong>Selection</strong> allows us to include choices in our program. Is it going to rain? Let's grab an umbrella!</p>
<ul>
    <li><a href="#syntax">Syntax</a>
    <ul><li><a href="#expressions">Expressions</a></li>
        <li><a href="#if_else"><code>if</code> and <code>else</code></a></li>
        <li><a href="#switch"><code>switch</code></a></li></ul>
    </li>
    <li><a href="#behavior">Behavior</a>
    <ul><li><a href="#expression_behavior">Expressions</a></li>
        <li><a href="#truth">Truth Tables</a></li></ul>
    </li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<h4><a name="expressions">Relational and Logical Expressions</a></h4>
<p>for relational and logical operator precedence and associativity, please see <a href="https://erinkeith.github.io/135/quick_guides/operators">Operator Precedence and Associativity</a></p>
<p>Most choices depend on comparing conditions or whether or not certain conditions are true. These relationships and conditions can be <em>evaluated</em> through relational and logical expressions.<br>
For example, if the temperature outside is below a certain threshold we would want to grab a jacket. The relationship between too cold and the current temperature could be determined with the following expression:<br>
<code>currentTemp < tooCold</code><br><br>
Relational and logical expressions always evaluate to <em>true</em> or <em>false</em> (although the C programming language uses <code>1</code> and <code>0</code> instead) and because they have lower precedence than arithmetic operators, the expressions can get quite complex:<br>
<code>currentTemp - 10 < tooCold</code><br><br>
Logical operators have even lower precedence than relational operators!<br>
<code>currentTemp < tooCold && currentTemp > 32</code><br><br>
also checks that the current temperature is above freezing.
</p>
<h4><a name="if_else"><code>if</code> and <code>else</code></a></h4>
<p>These expressions can be used in <code>if/else</code> statements to determine which blocks (parts) of code to execute, resulting in our programs <em>behaving</em> in different ways! These start with the <code>if</code> keyword, are followed by the expression to evaluate in the parenthesis, and should include curly braces surrounding the block of code you want executed:<br>
<pre><code>if(currentTemp < tooCold){
    printf("Don't forget a jacket!\n");
}</code></pre>

<br>When there's an alternative path to the true condition which must be taken, use the <code>else</code> keyword and curly braces for that block of code. <strong>Note!</strong> There is no expression to evaluate after the <code>else</code>!<br>
<pre><code>if(currentTemp < tooCold){
    printf("Don't forget a jacket!\n");
}
else{
    printf("So fresh and so clean!\n");
}</code></pre>

<br>When there's multiple alternative pathes, use a "cascading" <code>if/else</code> format:<br>
<pre><code>if(currentTemp < 32){
    printf("Oof, too cold! Stay home.\n");
}
else if(currentTemp < tooCold){
    printf("Don't forget a jacket!\n");
}
else{
    printf("So fresh and so clean!\n");
}</code></pre>
</p>
<p>There are a ton of different ways to use them, depending on the problem and how you approach it. <code>if</code> statements can even be used on their own. As long as the expression between the parenthesis evaluates to <code>1</code> (<em>true</em>), the code between the parenthesis executes:
<pre><code>if(raining == 'y' || raining == 'Y'){
    umbrella = 1;
}</code></pre>
If there's no action to take when it's not raining, then we don't need an <code>else</code> block.<br>
</p>
<h4><a name="switch"><code>switch</code></a></h4>
<p><code>switch</code> statements provide a convenient format when decisions are made based on specific integer or character values. The block starts with the <code>switch</code> keyword and the variable whose value is going to be checked. Then there is a list of "cases" for each useful value. Here's a generic form:<br>
<pre><code>switch(expression){ //the expression must be an int or char variable
    case x:
        //code to execute
        break;
    case y:
        //different code to execute
        break;
    default:
        //code to execute if no other cases are true
}</code></pre>

<br>And a more specific example:<br>
<pre><code>switch(currentTemp){
    case 32:
        printf("It's freezing!\n");
        break;
    case 451:
        printf("The temperature at which books burn.\n");
        break;
    case 212:
        printf("I'm boiling!\n");
        break;
    default:
        printf("Nothing interesting about this temperature.\n");
}</code></pre>

<br>Since there aren't any curly braces after the <code>case</code> value, the <code>break</code> statement is what keeps the code from continuing to execute. Sometimes it's useful to take advantage of that feature and omit the <code>break</code> statements!<br>
<pre><code>switch(studentGrade){
    case 'A':
    case 'B':
    case 'C':
        printf("Have fun in 202!\n");
        break;
    case 'D':
    case 'F':
        printf("See you next semester!\n");
        break;
    default:
        printf("Invalid grade.\n");
}</code></pre>
<br>If the <code>studentGrade</code> variable stores either <code>A</code>, <code>B</code>, or <code>C</code> then <code>Have fun in 202!</code> will display to the screen. While this allows for using a <code>switch</code> for a range, I'd only recommend it if there are very few possible matches.<br>
</p>
<h3><a name="behavior">Behavior</a></h3>
<h4><a name="expression_behavior">Relational and Logical Expressions</a></h4>
<p>Relational operators should look familiar, as they mirror their mathematical counterparts, however logical operators are often a new concept.
<ul>
    <li>AND <code>&&</code> expressions evaluate to <em>true</em> or <code>1</code> when both conditions are true.</li>
    <li>OR <code>||</code> expressions evaluate to <em>false</em> or <code>0</code> when both conditions are false.</li>
</ul>
This can be illustrated through real life. For example, if I were to say that we're in CS 135 <em>AND</em> Erin is teaching, that's a true statement. However, if we used some other course, the statement would be false. If we referred to some other instructor, it would also be false. This property is often represented in something called a <strong>Truth Table</strong>. [<a href="#truth">generic forms below</a>]<br><br>
The <strong>AND</strong> truth table:
<table>
<thead>
<tr>
<th>first part</th>
<th>logic</th>
<th>second part</th>
<th>whole statement</th>
</tr>
</thead>
<tbody>
<tr><td>We're in CS 135</td><td><em>AND</em></td><td>Erin is teaching.</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td>We're in CS 135</td><td><em>AND</em></td><td>Sara is teaching.</td><td><code>0</code> (<em>false</em>)</td></tr>
<tr><td>We're in CS 202</td><td><em>AND</em></td><td>Erin is teaching.</td><td><code>0</code> (<em>false</em>)</td></tr>
<tr><td>We're in CS 202</td><td><em>AND</em></td><td>Sara is teaching.</td><td><code>0</code> (<em>false</em>)</td></tr>
</tbody>
</table>
The <strong>OR</strong> relationship is much looser. If either statement is true, the overall statement is also true.<br>
The <strong>OR</strong> truth table:
<table>
<thead>
<tr>
<th>first part</th>
<th>logic</th>
<th>second part</th>
<th>whole statement</th>
</tr>
</thead>
<tbody>
<tr><td>We're in CS 135</td><td><em>OR</em></td><td>Erin is teaching.</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td>We're in CS 135</td><td><em>OR</em></td><td>Sara is teaching.</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td>We're in CS 202</td><td><em>OR</em></td><td>Erin is teaching.</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td>We're in CS 202</td><td><em>OR</em></td><td>Sara is teaching.</td><td><code>0</code> (<em>false</em>)</td></tr>
</tbody>
</table>
</p>

<a name="truth">Generic Truth Tables</a><br>
<strong>p</strong> is the first statment or <em>clause</em> and <strong>q</strong> is the second statment or <em>clause</em><br>
<h4>AND</h4>
<table>
<thead>
<tr>
<th>p</th>
<th>q</th>
<th>p && q</th>
</tr>
</thead>
<tbody>
<tr><td><code>1</code> (<em>true</em>)</td><td><code>1</code> (<em>true</em>)</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td><code>1</code> (<em>true</em>)</td><td><code>0</code> (<em>false</em>)</td><td><code>0</code> (<em>false</em>)</td></tr>
<tr><td><code>0</code> (<em>false</em>)</td><td><code>1</code> (<em>true</em>)</td><td><code>0</code> (<em>false</em>)</td></tr>
<tr><td><code>0</code> (<em>false</em>)</td><td><code>0</code> (<em>false</em>)</td><td><code>0</code> (<em>false</em>)</td></tr>
</tbody>
</table>
<h4>OR</h4>
<table>
<thead>
<tr>
<th>p</th>
<th>q</th>
<th>p || q</th>
</tr>
</thead>
<tbody>
<tr><td><code>1</code> (<em>true</em>)</td><td><code>1</code> (<em>true</em>)</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td><code>1</code> (<em>true</em>)</td><td><code>0</code> (<em>false</em>)</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td><code>0</code> (<em>false</em>)</td><td><code>1</code> (<em>true</em>)</td><td><code>1</code> (<em>true</em>)</td></tr>
<tr><td><code>0</code> (<em>false</em>)</td><td><code>0</code> (<em>false</em>)</td><td><code>0</code> (<em>false</em>)</td></tr>
</tbody>
</table>
