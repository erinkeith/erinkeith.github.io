<h2>C-style Strings</h2>
<p>We use <strong>C-style strings</strong> to store language.</p>
<p>What is language? What makes "pizza" different from 🍕 or even "PZA"? What's the difference between "Erin Keith" and "EK"?</p>
<p>
  If we wanted to store a user's first and last initials in our program, we could use an array of type <code>char</code> and size <code>2</code> because initials are just one letter each for the first and last name.
  On the other hand, if we wanted to store a user's first and last names how many characters would we need? Turns out, there's not really a way to know in advance!
</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <li><a href="#behavior">Behavior</a></li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<p>Syntactically, <strong>C-style strings</strong> are just character arrays with one very important difference: they <strong><em><u>must</u></em></strong> include a <strong>null character</strong> [<a href="#note">1</a>]! The <strong>null character</strong> is an escaped character: <code>\0</code>. It signifies the end of a string, since we cannot know in advance how long it will be.
</p>
<p>
  Speaking of which, since we cannot know how many letters are in a name or phrase, the accepted approach is to declare a character array of an <em>arbitrarily large size</em>, as in the declaration below.<br>
  <pre><code>#define STRING_CAPACITY 100

int main(){
	char c_style_string[STRING_CAPACITY];</code></pre>
</p>
<p>
  Unlike other arrays, <strong>C-style strings</strong> can be incorporated directly into <a href="https://erinkeith.github.io/135/topics/formatted_io">Formatted IO</a> using a <code>%s</code> conversion specifier. As you can see below, this is the only time <code>scanf</code> <u>does not</u> need the <code>&</code> (I'll explain why soon!).
</p>
<img src="https://github.com/user-attachments/assets/aa938a03-df49-4707-a097-a7e806fa9470" width="60%"><br>
<p>
  With the exception of <a href="https://erinkeith.github.io/135/topics/formatted_io">Formatted IO</a>, the approach to acceesing the letter <em>elements</em> of <strong>C-style strings</strong> is the same as regular arrays, with one exception: <strong><em>the control condition</em></strong>. We must still use an array's bestie, the <a href="https://erinkeith.github.io/135/topics/iteration#for"><code>for</code> loop</a>, but instead of stopping at size (or <em>capacity</em>), the end of the <strong>C-style string</strong> is actually the <strong>null character</strong> <code>\0</code>, as demononstrated below.
<pre><code>for(int index = 0; c_style_string[index] != '\0'; index++){
  // loop body
}
</p>

<h3><a name="behavior">Behavior</a></h3>
If <code>scanf</code> is used to store user input, it is important to note that the <code></code> is 
  <ol>
    <li>If the user enters less than <code>STRING_CAPACITY - 1</code> characters, the <code>\0</code> (<strong>null character</strong>) is automatically stored after the last character entered (it replaces the <code>\n</code> <strong>endline character</strong>).</li>  
  </ol>

<a name="note">1</a>. Not be confused with a <strong>null <em>pointer</em></strong>.<br>
