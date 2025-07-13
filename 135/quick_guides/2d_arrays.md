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

<h2>2D Arrays Quick Guide</h2>
<table>
    <tr>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td>A <strong>declaration</strong> statement creates a <em>composite</em> variable to store a group of values with multiple dimensions.</td>
        <td><img alt="declaration" src="https://github.com/user-attachments/assets/f794cbee-7c15-46b9-9503-33498eec7132"></td>
        <td>
          <ul><li>needs a <strong>data type</strong>, <strong>indentifier</strong>, and <strong> <em>two</em> sizes</strong> between <strong>square brackets</strong></li>
              <li>the <strong>sizes</strong> between the square brackets must be of type <code>int</code></li>
              <li>the first size is the number of <strong>rows</strong></li>
              <li>the second size is the number of <strong>columns</strong></li>
              <li><em>best practices</em> include using <strong>macros</strong> for the sizes</li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>A single array <strong>element</strong> is used for individual array <em>values</em>.</td>
        <td><img alt="element" src="https://github.com/user-attachments/assets/71bd5579-35d4-41ae-9655-29ebbf1f6212"></td>
        <td>
          <ul><li>needs a <strong>indentifier</strong> and <strong><em>two</em> indexes</strong> between <strong>square brackets</strong></li>
              <li>the <strong>indexes</strong> between the square brackets must be of type <code>int</code></li>
              <li>the first index is for the <strong>row</strong> number (starting at 0)</li>
              <li>the second index is for the <strong>column</strong> number (starting at 0)</li>
              <li>this expression should <strong><em>NOT</em></strong> include a <strong>data type</strong></li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>all array <strong>elements</strong> must be accessed one at a time</td>
        <td><img alt="elements" src="https://github.com/user-attachments/assets/6b2d5908-ff00-4fdb-9d42-f1627e659f10"></td>
        <td>
          <ul><li>needs <strong><em>nested</em></strong> <code>for</code> loops to repeat accessing each element</li>
              <li>the outer loop is generally for the controlling the <strong>row</strong> index</li>
              <li>the inner loop is generally for the controlling the <strong>column</strong> index</li>
              <li>the <strong>indexes</strong> will usually start at <code>0</code> and continue until <code>size - 1</code></li>
          </ul>
        </td>
    </tr>
    <tr>
        <td colspan="3"><strong>NOTE:</strong> 2D Arrays can also use <code>int</code> variables as the sizes during declaration.<br>
          <strong>NOTE:</strong> 2D Arrays can also have <strong>arbitrarily large</strong> sizes for any dimension for which we can't determine the number of objects <em>before</em> storing them in the array.</td>
    </tr>
</table>
