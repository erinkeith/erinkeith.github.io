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

<h2>Functions Quick Guide</h2>
<table>
    <tr>
        <th>Component</th>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td>prototype</td>
        <td>allows programmer to <strong><em>call</em></strong> functions from anywhere in the program</td>
        <td><img src="https://github.com/user-attachments/assets/4942f79b-db38-4ac6-acc7-1e02071f3bed"></td>
        <td>
          <ul>
            <li>a list of function <em>prototypes</em> goes <u>above</u> the main function</li>
            <li>each function <em>prototype</em> includes
              <ul>
                <li>the <strong><em>return type</em></strong> of the function
                  <ul>
                    <li>this should match the data type of any information that is sent out of the function</li>
                  </ul>
                </li>
                <li>the <strong><em>name</em></strong> of the function</li>
                <li>a list of <strong><em>parameters</em></strong> and their data type
                  <ul>
                    <li><em>parameters</em> are like special variables that save the values sent into the function</li>
                  </ul>
                </li>
                <li>a semicolon</li>
              </ul>
            </li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>call</td>
        <td>where in the program the code in the function will run</td>
        <td><img src="https://github.com/user-attachments/assets/eb625dc0-21e0-4fed-a0d9-70d1cf845c29"></td>
        <td>
          <ul>
            <li>function <em>calls</em> go in <u>anywhere</u> in our program that we want the function's behavior</li>
            <li>each function <em>call</em> includes
              <ul>
                <li>a variable and assignment operator if the <strong><em>returned</em></strong> value of a function is being saved</li>
                <li>the function name</li>
                <li>a list of <strong><em>arguments</em></strong> and their data type
                  <ul>
                    <li><em>arguments</em> are the actual values sent into the function</li>
                  </ul>
                </li>
              </ul>
            </li>
            <li>a semicolon</li>
          </ul>
        </td>
    </tr>
    <tr>
        <td>definition</td>
        <td>where the code for the function goes</td>
        <td><img src="https://github.com/user-attachments/assets/58abfa39-7436-4f8a-a378-778c944117ab"></td>
        <td>
          <ul>
            <li>function <em>definitions</em> go <u>below</u> the main function</li>
            <li>the first line of a function <em>definition</em> is the same as the function <strong><em>prototype</em></strong> except that the semicolon is replaced with curly braces</li>
            <li>all of the functions code goes in between the curly braces
              <ul>
                <li>anything can go here, even other function <strong><em>calls</em></strong></li>
              </ul>
            </li>
          </ul>
        </td>
    </tr>
</table>
