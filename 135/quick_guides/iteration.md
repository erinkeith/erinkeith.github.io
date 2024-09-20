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

<h2>Iteration Quick Guide</h2>
<table>
    <tr>
        <th>Type</th>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td><code>do while</code></td>
        <td>repeat actions <em><strong>at least once</strong></em></td>
        <td><img alt="do while" src="https://github.com/user-attachments/assets/60d3d3b9-7c30-4dc4-8333-576ba655733c"></td>
        <td>
          <ul>
            <li>the <u>initialization</u> expression can also be the <u>update</u> expression, since the body executes before evaluating the <u>controlling</u> expression</li>
            <li>the <u>controlling</u> expression comes after the <u>loop body</u></li>
            <li>the <u>update</u> expression is inside the <u>loop body</u></li>
          </ul>
        </td>
    </tr>
    <tr>
        <td><code>for</code></td>
        <td>repeat actions a certain <em><strong>number of times</strong></em></td>
        <td><img alt="for" src="https://github.com/user-attachments/assets/0c395a9b-3d73-4513-ba6f-dc926f6d60b2"></td>
        <td>
          <ul>
            <li>the <u>initialization</u>, <u>controlling</u>, and <u>update</u> expressions are all part of the loop setup</li>
            <li>they go in the parentheses before the <u>loop body</u></li>
          </ul>
        </td>
    </tr>
    <tr>
        <td><code>while</code></td>
        <td>any other circumstances!</td>
        <td><img alt="while" src="https://github.com/user-attachments/assets/a907c3a7-040c-48c8-bf22-ff6c9d8d0c19"></td>
        <td>
          <ul>
            <li>the <u>initialization</u> expression is definitely before the <u>controlling</u> expression</li>
            <li>the <u>controlling</u> expression comes before the <u>loop body</u>
              <ul><li>this means it is possible that the loop body does not even execute once!</li></ul>
            </li>
            <li>the <u>update</u> expression is inside the <u>loop body</u></li>
          </ul>
        </td>
    </tr>
</table>
