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
	<ul><li><a href="#scanf"><code>scanf</code></a></li>
	    <li><a href="#fgets"><code>fgets</code></a></li>
	    <li><a href="#creating">Creating New Strings</a></li></ul>
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
}</code></pre>
</p>
<p>
  It is very important to note that, syntactically, <strong>C-style strings</strong> are just a special case (or subset) of regular <code>char</code> arrays, the only difference being the use of the <strong>null character</strong> <code>\0</code> to signify the end of the <strong><em>string</em></strong> within the <strong><em>array</em></strong>.
</p>
<h3><a name="behavior">Behavior</a></h3>
<p>
  The biggest difference between <strong>C-style strings</strong> and <code>char</code> is at an abstract level. For example, <strong>C-style strings</strong> would be appropriate for storing the make of a vehicle like <code>Honda</code> or <code>Ford</code>, since those are names and have different lengths. However, they would be the incorrect tool for storing a license plate number like <code>123-HUL</code>, since that's more like a code with letters in it and should always have the same number of characters.
</p>
<p>
  Additionally, while <a href="https://erinkeith.github.io/135/topics/arrays#behavior">Array Behavior</a> also applies to <strong>C-style strings</strong>, there are some differences to cover.
</p>
<h4><a name="scanf"><code>scanf</code></a></h4>
<p>
  The <code>scanf</code> function stops at the first "blank space" character it encounters. This means it only allows us to store one word at a time. If the user enters a word shorter than the capacity, then the <code>\0</code> (<strong>null character</strong>) is automatically stored after the last non-blank character entered.
</p>
<h4><a name="fgets"><code>fgets</code></a></h4>
<p>
  The <code>fgets</code> function stops after the first endline character it encounters. This means it  allows us to store multiple words at a time. Since it also uses the capacity, the <code>\0</code> (<strong>null character</strong>) is automatically stored after the endline character or in the last element, whichever comes first. There are some additional differences in syntax that we'll go over in class, but you can get a head start here: <a href="https://en.cppreference.com/w/c/io/fgets">https://en.cppreference.com/w/c/io/fgets</a>.
</p>
<p>
  Each of these tools work differently, so it's important to choose the right one for the job!
</p>
<img src="https://github.com/user-attachments/assets/39244448-b0cf-4fe4-b75b-2bc8840ac353" width="60%"><img src="https://github.com/user-attachments/assets/d3620b2a-8fa8-4b43-8f83-f0e2438abbec" width="40%"><br>
<h4><a name="creating">Creating New Strings</a></h4>
<p>
  Finally, it's crucial to keep track of the <strong>null character</strong> <code>\0</code> when you're creating your own <strong>C-style strings</strong>. For example, when creating a copy of a string in another character array, you'll have to add the <strong>null character</strong> <code>\0</code> to the new string in the program after all of the characters have been copied.
</p>
<h5>Notes</h5>
<a name="note">1</a>. Not be confused with the <strong>null <em>pointer</em></strong> or <strong>endline character</strong> <code>\n</code>.<br>
