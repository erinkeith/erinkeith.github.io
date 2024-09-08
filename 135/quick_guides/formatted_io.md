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
        <td>
            <img src="">
        </td>
        <td>REMINDER!<br>You can use things like field width and precision to format how your output looks when displayed to the screen!</td>
    </tr>
    <tr>
        <td><code>scanf</code></td>
        <td>get <strong><em>input</em></strong> from the keyboard</td>
        <td>
            <img src="">
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
