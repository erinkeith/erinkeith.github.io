<h2>Arrays in Functions</h2>
<p>Because <a href="https://erinkeith.github.io/135/topics/arrays#behavior">arrays</a> are for groups of the same type of values and parameters can only store one thing, passing arrays into <a href="https://erinkeith.github.io/135/topics/functions#definition">functions</a> is a little different...</p>
<ul>
    <li><a href="#1D">1D Arrays</a></li>
    <ul><li><a href="#1prototype">Prototypes</a></li>
        <li><a href="#1definition">Definitions</a></li>
        <li><a href="#1call">Calls</a></li>
    </ul></li>
    <li><a href="#2D">2D Arrays</a></li>
    <ul><li><a href="#2prototype">Prototypes</a></li>
        <li><a href="#2definition">Definitions</a></li>
        <li><a href="#2call">Calls</a></li>
    </ul></li>
    </ul>
<h3><a name="1D">1D Arrays</a></h3>
<p>
  Just a quick syntax reminder about arrays and <a href="https://erinkeith.github.io/135/topics/variables#behavior">variables</a>: the name of an array is "bound" to or refers to the starting address of the collection of values. This means that arrays are always <a href="https://erinkeith.github.io/135/topics/pass_by_address">passed by address</a>. This is just part of how C (and many other languages) work.
</p>
<h4><a name="1prototype">Prototypes</a></h4>
<p>
  Because the array parameter just stores a memory address, to be able to access all elements in the array, we will also need a parameter for <em>size</em> or length. </pre>
<pre><code>void displayDoubleArray(int length, const double array[]);</code></pre>
  <strong>IMPORTANT!</strong> There should never be anything in the square brackets. Even if you include a number or variable there, it will not have any effect at all on the behavior of the program. The length value should <strong><em>always</em></strong> be passed in as an additional parameter. [<a href="#const">1</a>]
</p>
<h4><a name="1definition">Definitions</a></h4>
<p>
  When the length value is passed in properly, it can be used as the upper bound (or limit) in <code>for</code> loops:
<pre><code>void displayDoubleArray(int length, const double array[]){
  for(int index = 0; index < length; index++){
    printf(".2lf ", array[index]);
  }
}</code></pre>
  <strong>NOTE!</strong> While you <strong><em>should</em></strong> also include the length value when working with <a href="https://erinkeith.github.io/135/topics/strings">C-style Strings</a>, it's not strictly necessary because the null character <code>\0</code> controls the <code>for</code> loop.
</p>
<h4><a name="1call">Calls</a></h4>
<p>
  Let's assume we have an array for hourly temperature measurements for one day, and a macro was used during that array declaration:
<pre><code>double temperatures[MEASUREMENTS];</code></pre>
  Then our function call would include the macro and <u>just the array name</u> as <em>arguments</em>.
<pre><code>displayDoubleArray(MEASUREMENTS, temperatures);</code></pre>
</p>


<a name="const">1</a>. Since array parameters are inheritly <a href="https://erinkeith.github.io/135/topics/pass_by_address">passed by address</a>, any modifications to the elements within the function <em>persist</em> (meaning changes to the element values don't disappear after the function is done). The <code>const</code> keyword prevents the array from being modified within the function, providing a sort of "read-only" protection against writing to the array.<br>
