<h2>Strings</h2>
<p>We use <strong>strings</strong> to store language.</p>
<p>What is language? What makes "pizza" different from 🍕 or even "PZA"? What's the difference between "Erin Keith" and "EK"?</p>
<p>
  If we wanted to store a user's first and last initials in our program, we could use an array of type <code>char</code> and size <code>2</code> because initials are just one letter for the first and last name.
  On the other hand, if we wanted to store a user's first and last names how many characters would we need? Turns out, there's not really a way to know in advance!
</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <li><a href="#behavior">Behavior</a>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<p>Syntactically, C-style strings are just character arrays with one very important difference: they <strong><em><u>must</u></em></strong> include a <strong>null character</strong>! [<a href="#note">1</a>] The <strong>null character</strong> is an escaped character: <code>\0</code>. It signifies the end of a string, since we cannot know in advance how long it will be.
</p>
<p>
  Speaking of which, since we cannot know how many letters are in the name or phrase, the accepted approach is to declare a character array of an <em>arbitrarily large size</em>.<br>
  <pre><code>#define STRING_CAPACITY 100

int main(){
	char c_style_string[STRING_CAPACITY];    
  </code></pre>
</p>
<h3><a name="behavior">Behavior</a></h3>

<a name="note">1</a>. Not be confused with a <strong>null <em>pointer</em></strong>.<br>
