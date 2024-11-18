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
  In C, <em>streams</em> are implemented using a file pointer data type: <code>FILE *</code>. The <u>input</u> and <u>output</u> <em>streams</em> used for <a href="https://erinkeith.github.io/135/topics/formatted_io">Formatted IO</a> are called <code>stdin</code> and <code>stdout</code>. Since these always connect to the keyboard or screen as the source or destination respectively, they can be maintained by the <code>stdio</code> library and we don't have to add any special code to use them.
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
  The first argument is a string containing the filename (this is the only time the filename is used). The second argument is the <em>mode</em>, which determines which "direction" the <em>stream</em> flows (in or out). Although there are more <em>modes</em>, we will stick primarily to the following modes:
</p>
<table>
  <tr>
    <th>Mode</th>
    <th>Code</th>
    <th>Road</th>
  </tr>
  <tr>
    <td><strong>Read</strong></td>
    <td><code>"r"</code></td>
    <td>get input info into the program from a file</td>
  </tr>
  <tr>
    <td><strong>Write</strong></td>
    <td><code>"w"</code></td>
    <td>output info from the program to a file, starting at the file beginning<br>
    (any previous contents are erased)</td>
  </tr>
  <tr>
    <td><strong>Append</strong></td>
    <td><code>"a"</code></td>
    <td>output info from the program to a file, starting at the file end<br>
    (any previous contents remain)</td>
  </tr>
</table>
<p>
  If it <em>fails</em> to connect to the file, the <code>fopen</code> function will return a <code>NULL</code>[<a href="#null">1</a>] pointer. Before we do anything with the <em>stream</em> or file pointer, we first have to check to see if the connection failed by checking the file pointer for <code>NULL</code>.
</p>
<pre><code>if(filePointer == NULL){ // unsuccessful connection
  printf("Could not open file.\n");
  // you must skip any further File IO code or...

  // you could even end the program
  return 0;
}</code></pre>
<p>
  If the file pointer is <em>not</em> <code>NULL</code>, then you can continue on to do the actual reading from or writing to a file (covered in the <a href="#behavior">Behavior</a> section). When you are done with the file, <u><em>you must close it</em></u> by sending the file pointer as an argument into the <code>fclose</code> function.<br>
  <code>fclose(filePointer);</code>
</p>
<p>
  Best practices often orgranize programs by putting the opening and closing of files in the <code>main</code> function, and passing the connected file pointer into a different function to do the actual <strong>File IO</strong> work. In that case our program looks a little something like this:<br>
  <img src="https://github.com/user-attachments/assets/35895d4d-2d4e-40e7-a9db-30a5e9a24ad4" width="500"><br>
</p>

<h3><a name="behavior">Behavior</a></h3>
<h4><a name="output">Output</a></h4>
<p>
  Once a <em>stream</em> or file pointer is successfully connected to a file in <code>"w"</code> mode, we can "output" or write to it. We primarily use the <code>fprintf</code> function for that. It is almost identical to <code>printf</code> with one exception... Can you find it?<br>
  <code>fprintf(filePointer, "Hello World!\n");</code>
</p>
<p>
  Yep! A new argument goes before the <em>format string</em>: the file pointer!
</p>
<h4><a name="input">Input</a></h4>
<p>
  Once a <em>stream</em> or file pointer is successfully connected to a file in <code>"r"</code> mode, we can get "input" or read from it. We primarily use the <code>fscanf</code> function for that. It is almost identical to <code>fscanf</code> with the same exception as above: the file pointer is added!<br>
  <code>fscanf(filePointer, "%s", &firstName);</code>
</p>
<p>
  The same constraints apply to <code>fscanf</code> as <code>scanf</code> for strings: it stops at the first blank space. If we need more than that, we can always use the <code>fgets</code> function!<br>
  <code>fgets(fullName, SIZE, filePointer);</code>
</p>
<p>
  We'll spend a lot of time in class going over examples, especially situations where we need to "read" multiple lines of data from a file and store that data into an array.
</p>
<h3><a name="phone_calls">Metaphor</a></h3>
<p>
  I've often used the process of making a phone call as a metaphor for some parts of <strong>File IO</strong>.
</p>
<p>
  The file pointer is the phone and we have to get one first! Then, we have to use the <code>fopen</code> function which is a lot like dialing the phone number, especially because we only use the phone number once then we talk on the phone. It's the same with <strong>File IO</strong>: we only use the filename once, then we use the file pointer for the rest of the program.
</p>
<p>
  It's also important we wait until the phone is connected before the conversation begins. If we don't connect then we can put the phone away. Same with <strong>File IO</strong>!
</p>
<p>
  Finally, once we're done with the conversation we hang open the phone (or call the <code>fclose</code> function in <strong>File IO</strong>). We don't need to hange up if the call doesn't go through and sending a <code>NULL</code> pointer to the <code>fclose</code> function will cause a <em>segmentation fault</em>. Also, if we don't hang up then we can't make another call!
</p>
<a name="null">1</a>. <code>NULL</code> is a commonly used label for the <em>null pointer</em>. It's a lot like a default value for pointers when they're not <em>pointing</em> at something.
