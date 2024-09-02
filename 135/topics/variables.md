<h2>Variables</h2>
<p>Variables are the computer science tool we use when we want to save values in our program. Usually these values change over time or we don't know what they'll be while we're writing the code (kind of like the unknowns in an algebra equation).</p>
<ul>
    <li><a href="#syntax">Syntax</a>
    <li><a href="#behavior">Behavior</a>
    <li><a href="#metaphor">Metaphors</a>
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
            <td><strong>Values</strong></td>
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
            <td>an initial, a punctuation character</td>
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
<p>While there's no visible behavior associated with a variable declaration while the programm is running, we still need to understand what's happening to the computer.<br>

Remember that Operating System? You know! The one thing that's responsbile for managing interactions between software (our programs) and hardware (the keyboard, the RAM, etc.). When variable declaration statements in our code run on the computer, our program is basically asking the operating system for a memory address in RAM. Since the way that different kinds of values are saved in memory differ, the data type is important to this process (regardless of the language). The operating system grabs a good address from a "pool" of memory and "binds" the variable name to it. Every time the variable name is used in our code, it actually refers to that memory address[<a href="#important">1</a>].<br>

<h4>Junk</h4>
<p>It's very important to remember that the only thing a declaration statement does is reserve a memory address and tie it to the variable name. That's all. If you want more to happen, then you need to write more code!<br>

Usually, programmers do want more to happen which is where assignment and initialization statements come in. But before any of those, what would the value stored in the variable after declaration be?</p> 

<p>Well, when the operating system grabs a memory address from the pool, it does not "clear" it first. When the memory address is released back into the pool, it does not get "cleared"[<a href="#clearing">2</a>]. So there's no way of knowing what the value is and we will always assume that it's JUNK (some value that is nonsensical and not useful). Better safe than sorry!</p>

<h3><a name="metaphor">Metaphors</a></h3>
<p><strong>Why different data types?</strong><br>
Would you put soup on a plate? Would you put a slice of pizza in a shot glass? Probably not. Different data types take up different space in memory, much like pizza and soup.<br><br>
Other languages (like Python) still have data types, they just hide them from the programmer. While this makes learning to code faster, it doesn't help as much with learning <i>computer science</i>.</p>

<p><strong>Why care about memory addresses in RAM?</strong><br>
Cuz pointers (which we will learn about later).<br><br>
But also because humans are better at abstraction and we do this all the time. Would you tell your mom you're going to 1235 Oak Street? Or would you tell her you're going to your friend Kaycee's house? Do you want to remember what hexidecimal memory address a value is stored in? (If "yes", then you'll love CPE 301). Or would you rather remember the name of that variable?</p>

<p><strong>Why junk?</strong><br>
Ever been to a buffet? With those squishy plate stack things? When you grab one off the top so you have somewhere to put your food, you expect it to be clean, right?<br><br> 
Unfortunately, computers don't have dishwashers. The operating hands out "plates" (memory addresses) from the top without checking they're clean. When it gets a "plate" (memory address) back, it puts it right on top again, without checking that it's clean. Therefore, it's the programmers job to assume the plate will be dirty (that the variable will have a junk value).</p>


<a name="important">1</a>. IMPORTANT! This memory address is only for the one time the program runs. The next time the program runs, the same variable could get a different memory address.<br>
<a name="clearing">2</a>. In fact, the concept of "clearing" memory is kind of nonsensical. What should the default value be? Many folks want to say some version of 0, but 0 is often a valid value for certain problems. Also, that would take soooooo much of the computer's time and she busy.<br></p>
