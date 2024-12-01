<h2>Arrays in Functions</h2>
<p>Because <a href="https://erinkeith.github.io/135/topics/arrays#behavior">arrays</a> are for groups of the same type of values and parameters can only store one thing, passing arrays into <a href="https://erinkeith.github.io/135/topics/functions#definition">functions</a> is a little different...</p>
<ul>
    <li><a href="#1D">1D Array Parameters</a>
    <ul><li><a href="#1prototype">Prototypes</a></li>
        <li><a href="#1definition">Definitions</a></li>
        <li><a href="#1call">Calls</a></li>
    </ul></li>
    <li><a href="#2D">2D Array Parameters</a>
    <ul><li><a href="#2prototype">Prototypes</a></li>
        <li><a href="#2definition">Definitions</a></li>
        <li><a href="#2call">Calls</a></li>
    </ul></li>
</ul>
<h3><a name="1D">1D Array Parameters</a></h3>
<p>
  Just a quick syntax reminder about arrays and <a href="https://erinkeith.github.io/135/topics/variables#behavior">variables</a>: the name of an array is "bound" to or refers to the starting address of the collection of values. This means that arrays are always <a href="https://erinkeith.github.io/135/topics/pass_by_address">passed by address</a>. This is just part of how C (and many other languages) work.
</p>
<h4><a name="1prototype">Prototypes</a></h4>
<p>
  Because the array parameter just stores a memory address, to be able to access all elements in the array, we will <strong>also</strong> need a parameter for <em>size</em> or length. </pre>
<pre><code>void displayDoubleArray(int length, const double array[]);</code></pre>
</p>
<p>
  <strong>IMPORTANT!</strong> There should never be anything in the square brackets. Even if you include a number or variable there, it will not have any effect at all on the behavior of the program. The length value should <strong><em>always</em></strong> be passed in as an additional parameter. [<a href="#const">1</a>]
</p>
<h4><a name="1definition">Definitions</a></h4>
<p>
  When the length value is passed in properly, it can be used as the upper bound (or limit) in the <code>for</code> loop:
<pre><code>void displayDoubleArray(int length, const double array[]){
  for(int index = 0; index < length; index++){
    printf(".2lf ", array[index]);
  }
}</code></pre>
</p>
<p>
  <strong>NOTE!</strong> While you <strong><em>should</em></strong> also include the length value when working with <a href="https://erinkeith.github.io/135/topics/strings">C-style Strings</a>, it's not strictly necessary because the null character <code>\0</code> controls the <code>for</code> loop.
</p>
<h4><a name="1call">Calls</a></h4>
<p>
  Let's assume we have an array for hourly temperature measurements for one day, and a macro was used during that array declaration:
<pre><code>double temperatures[MEASUREMENTS];</code></pre>
</p>
<p>
  Then our function call would include the macro and <u>just the array name</u> as <em>arguments</em>.
<pre><code>displayDoubleArray(MEASUREMENTS, temperatures);</code></pre>
</p>

<h3><a name="2D">2D Array Parameters</a></h3>
<p>
  Before we dive in, you may want to review some of their technical details of <a href="https://erinkeith.github.io/135/topics/2d_arrays#behavior">2D Array Behavior</a>.
</p>
<h4><a name="2prototype">Prototypes</a></h4>
<p>
  For 2D array parameters, we will <strong>also</strong> need parameters for both the row size <em>and</em> the column size!
<pre><code>void clearBoard(int numRows, int numCols, char board[][numCols]);</code></pre>
  <strong>IMPORTANT!</strong> There <strong><em>must always</em></strong> be a value in the <u>second</u> set of square brackets (but never the <u>first</u>). Generally, this is a reference to the column size <em>parameter</em> so it must come before the array in the function's list of parameters. The description of <a href="https://erinkeith.github.io/135/topics/2d_arrays#behavior">2D Array Behavior</a> explains why the value in the column size is necessary in the second set of square brackets.
</p>
<h4><a name="2definition">Definitions</a></h4>
<p>
  When the row <u>and column</u> sizes are passed in properly, they can be used as the upper bounds (or limit) in each of the <code>for</code> loops:
<pre><code>void clearBoard(int numRows, int numCols, char board[][numCols]){
  for(int rowIndex = 0; rowIndex < numRows; rowIndex++){
    for(int colIndex = 0; colIndex < numCols; colIndex++){
      board[rowIndex][colIndex] = ' ';
    }
  }
}</code></pre>
  <strong>NOTE!</strong> While you <strong><em>should</em></strong> also include the column size as a parameter when working with <a href="https://erinkeith.github.io/135/topics/strings">C-style Strings</a>, it's not strictly necessary because the null character <code>\0</code> controls the <em>inner</em> <code>for</code> loop. <br>
  However, you still need a value in the second set of square brackets to compile! In that case, the <strong>string capacity</strong> <a href="https://erinkeith.github.io/135/topics/arrays#macros">macro</a> can be used, since it is defined in the global space.
</p>
<h4><a name="2call">Calls</a></h4>
<p>
  Let's assume we have a 2D array for a TicTacToe board, and a macro was used during that array declaration:
<pre><code>char ticTacToe[SIZE][SIZE];</code></pre>
</p>
<p>
  Then our function call would include the macro and <u>just the array name</u> as <em>arguments</em>.
<pre><code>clearBoard(SIZE, SIZE, ticTacToe);</code></pre>
</p>

<a name="const">1</a>. Since array parameters are inheritly <a href="https://erinkeith.github.io/135/topics/pass_by_address">passed by address</a>, any modifications to the elements within the function <em>persist</em> (meaning changes to the element values don't disappear after the function is done). The <code>const</code> keyword prevents the array from being modified within the function, providing a sort of "read-only" protection against writing to the array.<br>
