<h2>2D Arrays</h2>
<p>
  <strong>2D Arrays</strong> allow us to store multiple values that also have multiple <em>dimensions</em>.
</p>
<p>
  A good example for <strong>2D arrays</strong> is the game board for TicTacToe, where there are 9 spaces to choose from laid out in a grid with 3 across and 3 down.<br>
  <img src="https://github.com/user-attachments/assets/403fab21-9968-4905-85e7-5361256b564e" width="200">
</p>
<p>
  Since we play with Xs and Os, it makes sense that we'll want to save each of those as <code>char</code> variables, which also means that a "blank" or empty space will need to be represented by a <code>char</code> value. I think a literal space <code>' '</code> would make the most sense!
</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <ul><li><a href="#declaration">Declaration</a></li>
        <li><a href="#element_access">Accessing an Element</a></li>
        <li><a href="#all_elements">Accessing All Elements</a></li></ul>
    <li><a href="#arrays_of_strings">Arrays of Strings</a></li>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<h4><a name="declaration">Declaration</a></h4>
<p>
  <strong>2D array</strong> syntax is similar to <a href="https://erinkeith.github.io/135/topics/arrays">(1D) array</a> syntax, with one important difference: an additional <strong>size</strong>. 
  The C syntax for a <strong>2D array</strong> declaration statement must include a data type, an identifier (or name), a row size (between the first square brackets), a column size (between the second square brackets), and end with a semicolon.
</p>
<p>For example, for our TicTacToe board, we can declare a <strong>2D array</strong>:<br>
  <code>char board[3][3];</code>
</p>
<h4><a name="element_access">Accessing Elements</a></h4>
<p>
  We will still need to access each <em>element</em> one at a time. To do that, we'll use the square brackets again but instead of having the size inside, it will be the row and column <em>index</em>.
</p>
<p>
  <strong>WARNING!</strong> Index values <u>still</u> always start at <code>0</code>. They <strong><em>do not</em></strong> start at <code>1</code> (and should almost never be used that way).
</p>
<p>
  For example, we can access the middle space through the following expression:<br>
  <code>board[1][1]</code><br>
  <img src="https://github.com/user-attachments/assets/8db00ea9-ad00-47b2-aa7a-01bbc7b1511c" width="200">
</p>
<p>
  To update the board to save player moves, we would use the assignment operator:
<pre><code>board[1][1] = 'X';
board[0][1] = 'O';</code></pre>
  <img src="https://github.com/user-attachments/assets/0b1e7859-9469-41b5-b31f-a053fdf6a56b" width="200">
</p>
<h4><a name="all_elements">Accessing All Elements</a></h4>
<p>
  Since the <code>for</code> loops we've been using with <a href="https://erinkeith.github.io/135/topics/arrays">(1D) arrays</a> would only access the elements in a single row, to access all of the elements in a <strong>2D array</strong> we would need to repeat that process for every row...
</p>
<p>
  ...with <em>another</em> <code>for</code> loop! This
<pre><code>for(int rowIndex = 0; rowIndex < size; rowIndex++){
  for(int colIndex = 0; colIndex < size; colIndex++){
    board[rowIndex][colIndex] = ' ';
  }
}</code></pre>
<em>clears</em> the board by setting every element to the space character.
</p>

<h3><a name="arrays_of_strings">Arrays of Strings</a></h3>
