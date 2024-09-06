<h3>Operator Precedence and Associativity</h3>
<p>While there are more operators than these in C, we will primarily be using the following:</p>

<table>
<thead>
<tr>
<th>Symbol <sup>1</sup></th>
<th>Type of operation</th>
<th>Associativity</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>[</code> <code>]</code> <code>(</code> <code>)</code> <code>.</code> <code>-&gt;</code><br><code>++</code> <code>--</code> (postfix)</td>
<td>Expression</td>
<td>Left to right</td>
</tr>
<tr>
<td><code>*</code> <code>/</code> <code>%</code></td>
<td>Multiplicative</td>
<td>Left to right</td>
</tr>
<tr>
<td><code>+</code> <code>-</code></td>
<td>Additive</td>
<td>Left to right</td>
</tr>
<tr>
<td><code>&lt;</code> <code>&gt;</code> <code>&lt;=</code> <code>&gt;=</code></td>
<td>Relational</td>
<td>Left to right</td>
</tr>
<tr>
<td><code>==</code> <code>!=</code></td>
<td>Equality</td>
<td>Left to right</td>
</tr>
<tr>
<td><code>&amp;&amp;</code></td>
<td>Logical-AND</td>
<td>Left to right</td>
</tr>
<tr>
<td><code>||</code></td>
<td>Logical-OR</td>
<td>Left to right</td>
</tr>
<tr>
<td><code>=</code> <code>*=</code> <code>/=</code> <code>%=</code><br><code>+=</code> <code>-=</code> <code>&lt;&lt;=</code> <code>&gt;&gt;=</code> <code>&amp;=</code><br><code>^=</code> <code>|=</code></td>
<td>Simple and compound assignment <sup>2</sup></td>
<td>Right to left</td>
</tr>
<tr>
<td><code>,</code></td>
<td>Sequential evaluation</td>
<td>Left to right</td>
</tr>
</tbody>
</table>
<p><sup>1</sup> Operators are listed in descending order of precedence. If several operators appear on the same line or in a group, they have equal precedence.</p>
<p><sup>2</sup> All simple and compound-assignment operators have equal precedence.</p>
<p>An expression can contain several operators with equal precedence. When several such operators appear at the same level in an expression, evaluation proceeds according to the associativity of the operator, either from right to left or from left to right.</p>
<p>Only the sequential-evaluation (<code>,</code>), logical-AND (<code>&amp;&amp;</code>), and logical-OR (<code>||</code>) operators constitute sequence points, and therefore guarantee a particular order of evaluation for their operands. The function-call operator is the set of parentheses following the function identifier. The sequential-evaluation operator (<code>,</code>) is guaranteed to evaluate its operands from left to right. (The comma operator in a function call is not the same as the sequential-evaluation operator and does not provide any such guarantee.)</p>
<p>Logical operators also guarantee evaluation of their operands from left to right. However, they evaluate the smallest number of operands needed to determine the result of the expression. This is called "short-circuit" evaluation. Thus, some operands of the expression may not be evaluated. For example, in the expression</p>
<p><code>x &amp;&amp; y++</code></p>
<p>the second operand, <code>y++</code>, is evaluated only if <code>x</code> is true (nonzero). Thus, <code>y</code> is not incremented if <code>x</code> is false (0).</p>

This table is based on <a href="https://learn.microsoft.com/en-us/cpp/c-language/precedence-and-order-of-evaluation?view=msvc-170">https://learn.microsoft.com/en-us/cpp/c-language/precedence-and-order-of-evaluation?view=msvc-170</a> with examples and explanations outside the scope of this course removed.
