<h2>Variables</h2>
<p>Variables are the computer science tool we use when we want to save values in our program. Usually these values change over time or we don't know what they'll be while we're writing the code (kind of like the unknowns in an algebra equation).</p>
<ul>
    <li><a href="#syntax">Syntax</a>
    <li><a href="#behavior">Behavior</a>
    <li><a href="#metaphor">Metaphor</a>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<p>If we want to include a variable in our program, we must "declare" it. The C <span title="coding rules for a programming language">syntax</span> for a variable declaration statement must include a <a href="#data_type">data type</a>, an identifier (or name), and end with a semicolon.
<br><br>For example, if we need to save a user's age in our program we must declare a variable:<br><br>
<code>int userAge;</code></p>

<p>The C programming language does not allow spaces in <span title="names">identifiers</span>, so we can use "camel case" to smoosh them together by starting each new word with a capital letter. There are a few more <a href="https://learn.microsoft.com/en-us/cpp/c-language/c-identifiers?view=msvc-170">rules</a> about identifiers.</p>

<h4><a name="data_types"></a>Data Types</h4>
<p>Turns out programmers tend to see the same kinds of values in their programs, such as whole numbers, numbers with decimal points, and letters or punctuation. Every language has a type system for managing these data types although some languages, like C, are more strict about keeping track of them.</p>

<p>Although there are <a href="https://en.wikipedia.org/wiki/C_data_types#Main_types">many more data types</a>, we'll usually be using the following:</p>
<table>
    <tbody>
        <tr>
            <td><strong>Type</strong></td>
            <td><strong>Definition</strong></td>
            <td><strong>Example Uses</strong></td>
            <td><strong>Example Declaration</strong></td>
        </tr>
        <tr>
            <td><code>int</code></td>
            <td>whole numbers</td>
            <td>age, count, amount</td>
            <td><code>int userAge;</code></td>
        </tr>
        <tr>
            <td><code>double</code></td>
            <td>numbers with decimals</td>
            <td>money, measurement</td>
            <td><code>double shoePrice;</code></td>
        </tr>
        <tr>
            <td><code>char</code></td>
            <td>single character</td>
            <td>an initial, one letter, punctuation character</td>
            <td><code>char lastInitial;</code></td>
        </tr>
    </tbody>
</table>

<p>If you need multiple variables of the same type in your program, you can declare them on the same line:<br><br>
<code>int userAge, numDays;</code><br><br>
We can see the data type specified once, multiple identifiers, and one semicolon at the end. Each identifier is separated by a comma and will be the name of a new variable.</p>

<p>Generally, when we have variables of different types, they are declared on different lines:<br>
<pre><code>int numShoes;
double shoePrice, totalCost;
</code></pre></p>

<h3><a name="behavior">Behavior</a></h3>
<h3><a name="metaphor">Metaphor</a></h3>
