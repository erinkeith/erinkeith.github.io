<h2>Expressions</h2>
<p>Expressions combine an operator (symbol representing behavior) with one or more operands (values). The expression results in another value, through a process we call "evaluation".</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
    <li><a href="#behavior">Behavior</a></li>
    <ul><li><a href="#evaluation">Evaluation</a></li></ul>
    <ul><li><a href="#side_effect">Side Effects</a></li></ul>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<p>Most of the operators we'll use are either "unary" or "binary"[<a href="#ternary">1</a>]. Unary means the operator works with one operand, while binary means the operator works with two operands.<br>
<code>counter++</code><br>
is an expression where <code>counter</code> is the operand and <code>++</code> is the unary operator.[<a href="#post_pre">2</a>]<br>
<code>counter + 1</code><br>
is an expression where <code>counter</code> is the first operand, <code>1</code> is the second operand, and <code>+</code> is the binary operator.[<a href="#infix">3</a>]<br> 
<br>NOTE: I haven't included semicolons to emphasize that these are <i>expressions</i> not statements.<br><br>
</p>

<h3><a name="behavior">Behavior</a></h3>
<h4><a name="evaluation">Evaluation</a></h4>
<p>
  Each of our example expressions,<br>
  <code>counter++</code><br>
and<br>
  <code>counter + 1</code><br>
"evaluate to" (or result in) a value that is 1 more than whatever is stored in <code>counter</code>. For example, if <code>counter</code> was storing a value of <code>0</code>, then these expressions "evaluate" to <code>1</code>.
</p>
<p>Because all of our code is being broken to simpler instructions, the computer has to evaluate individual operator expressions one at a time. When we have more complex expressions with multiple operators, we need to understand what order the operators are evaluated in to know what the resulting value will be. This is determined by operator <i>precedence</i> and <i>associativity</i>.<br><br>
  Operator precedence is the priority operators are given to be evaluated first. <i>Arithmetic</i> operators generally follow a PEMDAS approach.<br>
  Associativity applies to multiple operators of the same precedence. Generally, binary operators have left to right associativity.<br>
  Here's a breakdown of relevant <a href="https://erinkeith.github.io/135/quick_guides/operators">Precedence and Associativity</a>
</p>
<h4><a name="side_effect">Side Effects</a></h4>
<p>A side effect is behavior in your programming that happens in addition to evaluation. Often, side effects make a change or modify a variable. For example,<br>
<code>counter = 0;</code><br>
evaluates to <code>0</code> but we use the assignment operator for its <i>side effect</i>, which is to change the value of <code>counter</code> to <code>0</code>.<br>

<code>counter++;</code><br>
evaluates to <code>1</code> but we use the postfix increment operator for its <i>side effect</i>, which is to increase the value of <code>counter</code> from <code>0</code> to <code>1</code>.<br>

The postfix and assignment operators (both simple and compound) are generally used for their side effects and any "evaluation" is ignored.
</p>

<a name="ternary">1</a>. There are occasionally "ternary" operators which include three operands.<br>
<a name="post_pre">2</a>. Unary operators can be in front of the operand (prefex) or after the operand (postfix). Most programmers use the postfix format, as it has a higher precedence.<br>
<a name="infix">3</a>. Binary operators use an infix format, where the operator goes between the operands. That is not true of all languages (>.> I'm looking at you, <a href="https://en.wikipedia.org/wiki/Lisp_(programming_language)">Lisp</a>).<br>
