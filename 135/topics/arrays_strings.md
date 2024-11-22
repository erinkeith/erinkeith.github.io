<h2>Arrays of Strings</h2>
<p>
  <strong>Arrays of Strings</strong> are special uses of <strong>2D Arrays</strong> where each row is an entire <a href="https://erinkeith.github.io/135/topics/strings">C-style string</a>, allowing us to store a <em>collection of language</em>!
</p>
<ul>
    <li><a href="#syntax">Syntax</a>
    <ul><li><a href="#declaration">Declaration</a></li>
        <li><a href="#element_access">Accessing an Element</a></li>
        <li><a href="#all_elements">Accessing All Elements</a></li>
        <li><a href="#slicing">Slicing Arrays</a></li></ul>
      </li>
</ul>

<h4><a name="declaration">Declaration</a></h4>
  The syntax for an <strong>array of strings</strong> declaration is exactly the same as <strong>2D array</strong> declarations. The biggest difference is related to the <u>abstraction</u> of what it's used for: language.
</p>
<p>For example, for a song playlist, we can declare a <strong>2D array</strong>:<br>
  <code>char playlist[8][100];</code></p>
<p>
  where the row size <code>8</code> is the number of songs (and should be replaced with a <a href="https://erinkeith.github.io/135/topics/arrays#macros">macro</a> like<code>NUM_SONGS</code>). The column size <code>100</code> is the "arbitrarily large" capacity for each song name (and should be replaced with a <a href="https://erinkeith.github.io/135/topics/arrays#macros">macro</a> like <code>STR_CAP</code>).
</p>

<h4><a name="element_access">Accessing Elements</a></h4>
<p>
  We can look at individual letters in the strings in the same way as other <strong>2D Arrays</strong>. Continuing our example, if we wanted to check which songs started with certain letters, we could do something like this:
<pre><code>for(int songIndex = 0; songIndex < NUM_SONGS; songIndex++){
  if(playlist[songIndex][0] == 'A'){
    printf("Song %d starts with an A.\n", songIndex + 1);
  }
}</code></pre>
</p>

<h4><a name="all_elements">Accessing All Elements</a></h4>
<p>
  Accessing each element in an <strong>array of strings</strong> is a little different than with a regular <strong>2D array</strong>, since we cannot know the <em>string length</em> in advance. Therefore, instead of being controlled by the <em>column size</em>, the inner <code>for</code> loop should rely on finding the null character <code>\0</code> for stopping, like so:
<pre><code>int spaceCounter = 0;
for(int songIndex = 0; songIndex < NUM_SONGS; songIndex++){
  for(int stringIndex = 0; board[songIndex][stringIndex] != '\0'; stringIndex++){
    if(board[songIndex][stringIndex] == ' '){
      spaceCounter++;
    }
  }
}</code></pre>
</p>

<h4><a name="slicing">Slicing Arrays</a></h4>
<p>
  Since each row of the <strong>2D Array</strong> is a <strong>C-style String</strong>, that row can be treated just like one! This is different than accessing a single element, or <code>char</code>, in the array. Instead, we're referring to the beginning of each row, which is often called <em>slicing</em> the array because we're isolating one <em>slice</em> or row in a <strong>2D array</strong>.
</p>
<p>
  Continuing our song example, to display each of the the songs in the playlist array, we just need to send each row to the <code>printf</code> function:<br>
<pre><code>for(int songIndex = 0; songIndex < NUM_SONGS; songIndex++){
  printf("%d: %s.\n", songIndex + 1, playlist[songIndex]);
}</code></pre>
</p>
