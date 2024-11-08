<h2>File IO</h2>
<p>So far, any information coming and going between our programs and the "outside world" have been related to the idea of a person using the program. While that's a very important source/destination to consider, there are plenty more! The first one we'll learn about is <strong><em>files</em></strong></p>
<p>Since <strong>File IO</strong> is very similar to <a href="https://erinkeith.github.io/135/topics/formatted_io">Formatted IO</a>, it may help to review that topic before moving on.</p>
<p>
  One of the important technical details we skipped over when covering <a href="https://erinkeith.github.io/135/topics/formatted_io">Formatted IO</a> is <em>streams</em>. The term <em>streams</em> reflects an abstraction used to describe or imagine how information <u>flows</u> to and from the program. Since <em>streams</em> only flow in one direction, we tend to consider them in terms of <u>input</u> or <u>output</u> <em>streams</em>.
</p>

<ul>
    <li><a href="#syntax">Syntax</a></li>
    <li><a href="#behavior">Behavior</a>
    <ul><li><a href="#output">Output</a></li>
        <li><a href="#input">Input</a></li></ul>
    </li>
    <li><a href="#phone_calls">Metaphor</a></li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<p>
  In C, <em>streams</em> are implemented using a file pointer data type: <code>FILE *</code>. The <u>input</u> and <u>output</u> <em>streams</em> used for <a href="https://erinkeith.github.io/135/topics/formatted_io">Formatted IO</a> are called <code>stdin</code> and <code>stdout</code>. Since these always connect to the keyboard or screen as the source or destination, they can be maintained by the <code>stdio</code> library and we don't have to add any special code to use them.
</p>
<p>
  Files, on the other hand, are stored all over the hard drive so the information needed to connect to a file <u>changes over time</u>. This means we need to write code to create and use our own file pointers when we want to use <strong>File IO</strong>. Luckily, much of the code to create these file streams in our programs is pretty standard!
</p>
<p>
  <strong>File IO</strong> starts with a file pointer declaration:<br>
  <code>FILE* filePointer;</code>
</p>
<p>
  The <code>fopen</code> function is used to try to connect our file pointer to the file, thereby establishing the <em>stream</em>:<br>
  <code>filePointer = fopen("filename.txt", "r");</code>
</p>
<p>
  The first argument is a string containing the filename (this is the only time the filename is used). The second argument is the <em>mode</em>, which determines which "direction" the <em>stream</em> flows (in or out). Although there are more <em>modes</em>, we will stick to <code>"r"</code> for <em>read</em> (<u>input</u>) and <code>"w"</code> for <em>write</em> (<u>output</u>).
</p>
<p>
  If the it <em>fails</em> to connect to the file, the <code>fopen</code> function will return a <code>NULL</code>[<a href="#null">1</a>] pointer. Before we do anything with the <em>stream</em> or file pointer, we first have to check to see if the connection failed by checking the file pointer for <code>NULL</code>.
</p>
<pre><code>if(filePointer == NULL){ // unsuccessful connection
  printf("Could not open file.\n");

  // you must skip any further File IO code or
  // you could even end the program
  return 0;
}</code></pre>
<h3><a name="behavior">Behavior</a></h3>
<h4><a name="output">Output</a></h4>

<h4><a name="input">Input</a></h4>
<h3><a name="phone_calls">Metaphor</a></h3>
<p>
  I've often used the process of making a phone call as a metaphor for some parts of <strong>File IO</strong>.
</p>
<a name="null">1</a>. <code>NULL</code> is a commonly used label for the <em>null pointer</em>. It's a lot like a default value for pointers when they're not <em>pointing</em>at something.
