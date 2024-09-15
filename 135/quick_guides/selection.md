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

<h2>Selection Quick Guide</h2>
<table>
    <tr>
        <th>Type</th>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td><code>if</code></td>
        <td>execute a block of code when a <em><strong>condition is true</strong></em></td>
        <td><img alt="if" src="https://github.com/user-attachments/assets/79baa5d9-b940-401c-a8f4-a22ee00fad73"></td>
        <td>
          <ul>
            <li>statements within curly braces only execute when the expression between the parenthesis evaluates to <code>1</code> or <em>true</em></li>
            <li>when the expression between the parenthesis evaluates to <code>0</code> or <em>false</em>, the block of code is simply <strong>skipped</strong></li>
            <li>you can put anything inside these curly braces
              <ul><li>this includes more <code>if</code>/<code>else</code> statements (making them "nested")</li></ul>
            </li>
          </ul>
        </td>
    </tr>
    <tr>
        <td><code>else if</code></td>
        <td>execute a block of code with <em><strong>mututally exclusive conditions</strong></em></td>
        <td><img alt="else_if" src="https://github.com/user-attachments/assets/8f101fc3-ed52-4c31-b7f4-38a2a7a01f86"></td>
        <td>
          <ul>
            <li>only one of the paths can execute
              <ul><li>the first block of code with an expression that evaluates to <code>1</code> or <em>true</em> will execute</li>
                  <li>previous blocks with expresions that evaluated to <code>0</code> or <em>false</em> were <strong>skipped</strong></li>
                  <li>any following blocks beginning with an <code>else</code> will be <strong>skipped</strong></li></ul></li>
            <li>these are also known as "cascading" <code>if</code>/<code>else</code> statements</li>
          </ul>
        </td>
    </tr>
    <tr>
        <td><code>else</code></td>
        <td>execute the "leftover" block of code when <em><strong>no conditions are met</strong></em></td>
        <td><img alt="else" src="https://github.com/user-attachments/assets/bd53fdcb-6a8e-4a49-9ce8-23fdf2c8058f"></td>
        <td>these aren't always necessary</td>
    </tr>
    <tr>
        <td><code>switch</code></td>
        <td>execute a block of code based on <em><strong>the value stored in a <code>char</code> or <code>int</code> variable</strong></em></td>
        <td><img alt="switch" src="https://github.com/user-attachments/assets/818011fc-45d2-4d77-8ed7-7be5aa8f4fb3"></td>
        <td>
          <ul>
            <li>these <em><strong>do not</strong></em> work for decimal values</li>
            <li>execution begins immediately after a <em>true</em> <code>case</code> and does not stop until a <code>break;</code> statement or the end
              <ul><li>omitting the <code>break;</code> statement allows for "fall through" where code under subsequent cases also executes</li></ul>
            </li>
          </ul>
        </td>
    </tr>
</table>
