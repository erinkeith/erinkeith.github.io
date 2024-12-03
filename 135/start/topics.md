<style>
    table{
        width:100%;
    }
    td{
        vertical-align: top;
    }
    img{
        height: auto;
        max-width: 100%;
    }
</style>

<h2>Topics</h2>
<table>
    <tr>
        <th>Tool</th>
        <th>Use</th>
        <th style="width:40%">Explanation</th>
        <th style="width:35%"><code>C</code> Examples</th>
    </tr>
    <tr>
        <td>Program Basics</td>
        <td>start programming</td>
        <td>minimum syntax to create a program<br>(<em>or get points in this class</em>)</td>
        <td><ul>
          <li>header comments</li>
          <li>preprocessor directives</li>
          <li>main function</li>
          <li>return statement</li>
        </ul></td>
    </tr>
    <tr>
        <td>Variable</td>
        <td>save stuff</td>
        <td>store values that change<br>(<em>either during the program or between program runs</em>)</td>
        <td><ul>
          <li>declaration statements</li>
          <li>assignment statements</li>
          <li>initialization statements</li>
        </ul></td>
    </tr>
    <tr>
        <td>Expression</td>
        <td>do stuff</td>
        <td>bit of code which results in or <em>evaluates to</em> another value</td>
        <td><ul>
          <li>arithmetic: <code>+</code> <code>-</code> <code>*</code> <code>/</code> <code>%</code></li>
          <li>relational: <code>==</code> <code><</code> <code><=</code> <code>></code> <code>>=</code></li>
          <li>logical: <code>&&</code> <code>||</code></li>
          <li>function calls</li>
        </ul></td>
    </tr>
    <tr>
        <td>Formatted IO</td>
        <td>interact with user</td>
        <td>gets values from the keyboard or displays text to the screen</td>
        <td><ul>
          <li><code>printf</code> function</li>
          <li><code>scanf</code> function</li>
        </ul></td>
    </tr>
    <tr>
        <td>Selection</td>
        <td>make decisions</td>
        <td>allows program to "decide" which code blocks to execute</td>
        <td><ul>
          <li><code>if</code> blocks</li>
          <li><code>else</code> blocks</li>
          <li><code>switch</code> statements</li>
        </ul></td>
    </tr>
    <tr>
        <td>Iteration</td>
        <td>repetition</td>
        <td>allows program to continue executing certain blocks of code until a condition is met</td>
        <td><ul>
          <li><code>for</code> loops</li>
          <li><code>while</code> loops</li>
          <li><code>do while</code> loops</li>
        </ul></td>
    </tr>
    <tr>
        <td>Arrays</td>
        <td>saving a group of stuff</td>
        <td>store a collection of same-type values that change</td>
        <td><ul>
          <li>declaration (with size)</li>
          <li>access a single element through the <strong>index</strong></li>
          <li>access all elements with a <code>for</code> loop controlled by the index</li>
        </ul></td>
    </tr>
    <tr>
        <td>C-Style Strings</td>
        <td>saving words</td>
        <td>store a collection of <code>char</code>s that combine to form language</td>
        <td><ul>
          <li>declared as a 1D array of <code>char</code>s</li>
          <li>access a single element through the <strong>index</strong></li>
          <li>access all elements with a <code>for</code> loop controlled by the null character <code>\0</code></li>
        </ul></td>
    </tr>
    <tr>
        <td>Functions</td>
        <td>modularize code</td>
        <td>organize program into chunks of code specific enough to accomplish a single task, but generalizable enough to do it under different circumstances</td>
        <td><ul>
          <li>prototypes, definitions, calls</li>
          <li>returned type/value, name, parameters/arguments</li>
        </ul></td>
    </tr>
    <tr>
        <td>Pass by Address</td>
        <td>"return" multiple values</td>
        <td>since <code>C</code> can only return 1 value from a function, passing the address of a variable allows it to be modified within the function</td>
        <td><ul>
          <li>pointer parameters</li>
          <li><strong>address of</strong> operator <code>&</code></li>
          <li><strong>dereference</strong> operator <code>*</code></li>
        </ul></td>
    </tr>
    <tr>
        <td>File IO</td>
        <td>interact with a file</td>
        <td>read values from or save values to a file on the hard drive</td>
        <td><ul>
          <li><code>FILE*</code> data type</li>
          <li><code>fopen</code> and <code>fclose</code> functions</li>
          <li><code>fprintf</code> and <code>fscanf</code> functions</li>
        </ul></td>
    </tr>
    <tr>
        <td>2D Arrays</td>
        <td>saving a group of stuff with multiple dimensions</td>
        <td>store a collection of same-type values that change, in rows and columns</td>
        <td><ul>
          <li>declaration (with row and column sizes)</li>
          <li>access a single element through the row <em>and</em> column <strong>indexes</strong></li>
          <li>access all elements with an outer <code>for</code> loop controlled by the row index and an inner <code>for</code> loop controlled by the column index</li>
        </ul></td>
    </tr>
    <tr>
        <td>Arrays of Strings</td>
        <td>saving a group of words</td>
        <td>store a collection of C-style strings</td>
        <td><ul>
          <li>declared as a 2D array of <code>char</code>s</li>
          <li>access a single element through the row <em>and</em> column <strong>indexes</strong></li>
          <li>access all elements with an outer <code>for</code> loop controlled by the row index and an inner <code>for</code> loop controlled by the null character <code>\0</code></li>
        </ul></td>
    </tr>
</table>
