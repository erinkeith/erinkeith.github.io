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

<h2>Strings Quick Guide</h2>
<table>
    <tr>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td>A <strong>declaration</strong> statement creates a <em>composite</em> variable to store a group of chars.</td>
        <td><img alt="declaration" src="https://github.com/user-attachments/assets/ac9bce7e-2788-4f7a-8039-a1a6ac8992c8"></td>
        <td>
          <ul><li>this is the same as regular <code>char</code> <strong>arrays</strong></li>
              <li>the <em>size</em> should be large enough to accommodate the longest possible string as the <strong>capacity</strong></li>
              <li>the <strong>capacity</strong> should also ensure there's enough room for the <strong>null character</strong>: <code>\0</code></li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>A single array <strong>element</strong> is used to access individual characters in the <em>string</em>.</td>
        <td></td>
        <td>
          <ul><li>this is the same as regular <code>char</code> arrays</li></ul>
        </td>
    </tr>
    <tr>
        <td>all array <strong>elements</strong> must be accessed one at a time</td>
        <td><img alt="element" src="https://github.com/user-attachments/assets/86a77eb0-5630-47c1-b4d9-5e1cf0a8b171"></td>
        <td>
          <ul><li>this is the same as regular <code>char</code> <strong>arrays</strong> except the loop should end at the <strong>null character</strong> <code>\0</code> NOT the <em>capacity</em></ul>
        </td>
    </tr>
    <tr>
        <td rowspan="2"><em>Strings</em> are the only arrays that can be used directly with <strong>Formatted IO</strong></td>
        <td rowspan="1">
          <h4><code>printf</code> and <code>scanf</code></h4>
          code in your program file:<br><img alt="variable length array" src="https://github.com/user-attachments/assets/7192c09e-9399-4e34-b048-e98027903d28"><br>
          terminal while running the executable:<br><img alt="variable length array" src="https://github.com/user-attachments/assets/1dd3c119-fee7-4c21-b04d-2e3a374dd7bb"> 
        </td>
        <td rowspan="1">
          <ul><li>the <code>%s</code> conversion specifier allows you to send whole strings into the <code>printf</code> and <code>scanf</code> functions<ul>
                <li><strong>CAUTION</strong>! you cannot do this with any other type of array</li>
                <li><strong>CAUTION</strong>! <code>printf</code> only works for strings if there is a <strong>null character</strong> <code>\0</code> in the array</li>
              </ul></li>
              <li>the <code>scanf</code> function stops at the first <em>blank space</em> it sees<ul>
                <li><strong>CAUTION</strong>! it does <u><em>not</em></u> guarantee that a <strong>null character</strong> <code>\0</code> is stored in the array</li>
              </ul></li>
          </ul>
        </td>
    </tr>
    <tr>
      <td rowspan="1">
        <h4><code>fgets</code></h4>
        code in your program file:<br><img alt="variable length array" src="https://github.com/user-attachments/assets/fe7af80f-6ff6-4f0d-93ab-32a0c6884074"><br> 
        terminal while running the executable:<br><img alt="variable length array" src="https://github.com/user-attachments/assets/729a08f3-1c20-490f-bc37-249f3f36f994"> 
      </td>
      <td rowspan="1">
        <ul><li>the <code>fgets</code> function stops at the first <strong>endline character</strong> <code>\n</code><ul>
              <li>it also stores that <strong>endline character</strong> <code>\n</code></li>
              <li>it <u><em>does</em></u> guarantee that a <strong>null character</strong> <code>\0</code> is stored in the array</li>
            </ul></li>
        </ul>
      </td>
    </tr>
</table>
