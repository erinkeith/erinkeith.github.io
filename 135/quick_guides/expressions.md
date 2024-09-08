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

<h2>Expressions Quick Guide</h2>
<p>For more information on the order of <em>expression evaluation</em>, see <a href="https://erinkeith.github.io/135/quick_guides/operators">Operator Precedence and Associativity</a></p>
<table>
    <tr>
        <th>Type</th>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td><strong>arithmetic</strong></td>
        <td>doing <strong><em>math</em></strong> with values</td>
        <td>
            <img src="">
        </td>
        <td>
          <ul>
              <li><code>+ - * / %</code></li>
              <li>an expression with two <code>int</code> values evaluates to an <code>int</code>
                  <ul>
                      <li>beware of integer division!</li>
                  </ul>
              </li>
              <li>an expression with <code>int</code> and <code>double</code> values evaluates to a <code>double</code></li>
              <li>since <code>chars</code> are stored as numerical values, you can do math (and comparisons) with them, too!</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td><strong>relational</strong></td>
        <td><strong><em>comparing</em></strong> values</td>
        <td><img src=""></td>
        <td>
          <ul>
              <li><code>< > <= >= == !=</code></li>
              <li>these always evaluate to either <code>1</code> or <code>0</code> (<em>true</em> or <em>false</em>)</li>
              <li>to determine if a values is within a <em>range</em>, relational expressions must be combined with logical expressions</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td><strong>logical</strong></td>
        <td>combining multiple <strong><em>truths</em></strong></td>
        <td><img src=""></td>
        <td>
          <ul>
              <li><code>&& ||</code></li>
              <li>Logical expressions can <em>short circuit</em> or skip evaluation if the first expression determines the result. For example, 
                <ul>
                  <li>if the first part of a <code>&&</code> expression is <code>0</code> (<em>false</em>), the second part won't evaluate because it won't change the overall (<em>false</em>) result</li>
                  <li>if the first part of a <code>||</code> expression is <code>1</code> (<em>true</em>), the second part won't evaluate because it won't change the overall (<em>true</em>) result</li>
                </ul></li>
          </ul>
        </td>
    </tr>
</table>
