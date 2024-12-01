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
    <li><a href="#syntax">Syntax</a>
    <ul><li><a href="#declaration">Declaration</a></li>
        <li><a href="#element_access">Accessing an Element</a></li>
        <li><a href="#all_elements">Accessing All Elements</a></li></ul>
      </li>
    <li><a href="#behavior">Behavior</a></li>
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
  We will still need to access each <em>element</em> one at a time. To do that, we'll use the square brackets again but instead of having the sizes inside, it will be the row and column <em>index</em>.
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

<h3><a name="behavior">Behavior</a></h3>
<p>
  Just like <a href="https://erinkeith.github.io/135/topics/variables#behavior">variables</a> and <a href="https://erinkeith.github.io/135/topics/arrays#behavior">1D arrays</a>, there is no visible program behavior associated with 2D array declaration. However, it can be very useful to understand what's going on under the hood!
</p>
<p>
  Often, when we're in the abstraction or design phase of solving problems, we imagine or even draw 2D arrays with the 2 dimensions that apply to our problem (like the TicTacToe board above), but that's not how they're actually stored when using C. Instead, the operating system ensures that all of the addresses are still <em>contiguous</em> (or in a row) even though we imagine them on different <em>rows</em>. The compiler then does a bunch of simple arithmetic to ensure we're accessing the correct element with the two necessary indexes.
</p>
<p>To access the element <code>m[rowIndex][colIndex]</code>, the compiler must:</p>

<table>
    <tr>
        <td>1. multiply <code>rowIndex</code> by the size of a single row of <code>m</code> and add this result to <code>m</code>'s address to find the beginning of the correct row</td>
        <td><img src="https://github.com/user-attachments/assets/807a249a-bf0b-4a59-907c-7190264801b5"></td>
    </tr>
    <tr>
        <td>&emsp;i. (the size of the single row would be the product of <u><strong><em>the number of columns</em></strong></u> and the size of an array element)</td>
        <td><img src="https://github.com/user-attachments/assets/ef1a7461-e6f7-4ae4-b27a-e3c4f6e4e5ab"></td>
    </tr>
    <tr>
        <td>2. multiply <code>colIndex</code> by the size of an array element</td>
        <td><img src="https://github.com/user-attachments/assets/b27edd09-bb56-42e4-a3d1-c3d9d662eb11"></td>
    </tr>
    <tr>
        <td>3. add the previous result to the address from Step 1. to find the correct element</td>
        <td><img src="https://github.com/user-attachments/assets/c7b56443-baf9-491e-a716-c0845281e591"></td>
    </tr>
</table>
