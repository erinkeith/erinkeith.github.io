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

<h2>Arrays Quick Guide</h2>
<table>
    <tr>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td>A <strong>declaration</strong> statement creates a <em>composite</em> variable to store a group of values.</td>
        <td><img alt="declaration" src="https://github.com/user-attachments/assets/2c2f6876-61c2-41e0-b3fb-4fb303b823ee"></td>
        <td>
          <ul><li>needs a <strong>data type</strong>, <strong>indentifier</strong>, and <strong>size</strong> between <strong>square brackets</strong></li>
              <li>The <strong>size</strong> between the square brackets must be of type <code>int</code>.</li>
              <li><em>Best practices</em> include using a <strong>macro</strong> for the size.</li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>A single array <strong>element</strong> is used to access individual values.</td>
        <td><img alt="element" src="https://github.com/user-attachments/assets/6c89ea21-1dce-440b-8522-dfca58883d87"></td>
        <td>
          <ul><li>needs a <strong>indentifier</strong> and <strong>index</strong> between <strong>square brackets</strong></li>
              <li>The <strong>index</strong> between the square brackets must be of type <code>int</code> and represents an <em>offset</em> from the beginning of the array.</li>
              <li>This expression <strong><em>should not</em></strong> include a <strong>data type</strong>.</li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>all array <strong>elements</strong> must be accessed one at a time</td>
        <td><img alt="elements" src="https://github.com/user-attachments/assets/488e8254-6727-40cf-b960-ee6b24fe25df"></td>
        <td>
          <ul><li>needs an <code>for</code> loop to repeat accessing each element</li>
              <li>The <strong>index</strong> will usually start at <code>0</code> and continue until <code>size - 1</code>.</li>
          </ul>
        </td>
    </tr>
    <tr>
        <td><strong>Variable length</strong> arrays use an <code>int</code> variable as the size during declaration.<br><br>For example, the size can be determined during runtime if the user enters the number of items before the array needs to be declared</td>
        <td><img alt="variable length array" src="https://github.com/user-attachments/assets/f178a7c5-1dfe-4a4c-8fa5-d53029e0b973"></td>
        <td>
          <ul><li>As long as the size variable stores a valid <code>int</code> value, it can be used as the size in the array declaration but <strong>the order of these statements is very important!</strong></li>
              <li>The variable used as the size during declaration can also be used to control any <code>for</code> loops used to access all the elements in the array.</li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>Arrays of an <strong>arbitrarily large</strong> size can be used when we can't determine the number of objects <em>before</em> storing them in the array.</td>
        <td><img alt="arbitrarily large" src="https://github.com/user-attachments/assets/5d8ad8d0-d484-4206-858f-e2e7a6418c7c"></td>
        <td>
          <ul><li>The size during array declaration is considered the <em>capacity</em>.</li>
              <li>The actual number of useful values must also be saved in another variable and would be used to control any subsequent <code>for</code> loops.</li>
          </ul>
        </td>
    </tr>
</table>
