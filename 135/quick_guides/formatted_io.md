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

<h2>Formatted IO Quick Guide</h2>
<table>
    <tr>
        <th>Type</th>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td><code>printf</code></td>
        <td><strong><em>output</em></strong> text to the screen</td>
        <td>code in your program file:<br>
            <img src="https://github.com/user-attachments/assets/0025ff5f-7bd9-4868-8241-163f50d64c9a">
            terminal output when running the executable:<br>
            <img src="https://github.com/user-attachments/assets/56c9f6c1-d985-495a-b1cf-c840fcd91a5d">
        </td>
        <td>REMINDER!<br>You can use things like field width and precision to format how your output looks when displayed to the screen!</td>
    </tr>
    <tr>
        <td><code>scanf</code></td>
        <td>get <strong><em>input</em></strong> from the keyboard</td>
        <td>code in your program file:<br>
            <img src="https://github.com/user-attachments/assets/61f22e38-3666-4152-9548-3aecc8a8a6e9">
            terminal output when running the executable:<br><br>
            <strong>FIRST</strong> the prompt displays and the program does nothing until the user has entered the right information<br>
            <img src="https://github.com/user-attachments/assets/f8814ff0-7f14-467b-88bb-aeb4d7493bdf">
            <strong>THEN</strong> the program continues execution after the user has hit the Enter key<br>
            <img src="https://github.com/user-attachments/assets/f0055bc2-06dd-4c25-babf-70c6ec86b1a4">
        </td>
        <td>
          <ul>
            <li>only <em>conversion specifiers</em> go between the double quotes
              <ul>
                <li>unless we're trying to skip over blank space when saving a <code>char</code> value
                <ul>
                  <li>see the space before the <code>%c</code> in the example</li>
                </ul></li>
              </ul></li>
              <li>don't forget the <code>&</code> (<em>ampersand</em>) before each variable name</li>
              <li><strong>CAUTION!</strong>
                <ul>
                  <li><strong><em>nothing is ever displayed to the screen</em></strong>
                  <ul>
                    <li>trying to use formatting like field width and precision won't do anything</li>
                  </ul></li>
                </ul>
              </li>
            </ul>
        </td>
    </tr>
</table>
</table>
