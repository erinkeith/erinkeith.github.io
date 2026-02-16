<h2>Iteration</h2>
<p><strong>Iteration</strong> allows us to repeat blocks of code a bunch of times in a row.<br><br>
  <strong>Loops</strong> are used to implement <em>iteration</em>. To craft a loop, we must know what <u>behavior</u> or action(s) we're repeating <em><strong>and</strong></em> what <u>state</u> or value(s) is changing over time.
<p>A real-life example is <u>going for a run</u>. The process we're repeating is moving one leg in front of the other more quickly than a walk. The "state" (or value) that changes over time is <em>distance</em>. 
  This is important because before <u>going for a run</u>, we need to decide where our run starts and ends. Then, as long as we haven't reached our destination (and can still breath) we keep running! 
  If we don't figure these things out, we either can't start running or will never stop (my personal nightmare)!</p>
<ul>
    <li><a href="#syntax">Syntax</a></li>
        <ul><li><a href="https://erinkeith.github.io/135/quick_guides/iteration">Coding Quick Guide</a></li></ul>
</ul>
<h3><a name="syntax">Syntax</a></h3>
<p>In addition to the <u>loop body</u>, there are 3 components that should be included in each loop:
  <ul>
    <li>The <u>initialization</u> expression allows to assign some <strong>start</strong>ing value to a variable that's going to change while the loop is running.
      <ul><li>In our real-life example, we could set a <code>stepsFromHome</code> variable to <code>0</code>.</li></ul></li>
    <li>The <u>controlling</u> expression generally compares the variable's value to another value that will tell us when to stop. The loop will <strong>continue</strong> as long as it evaluates to <code>1</code> or <em>true</em>.
      <ul><li>In our real-life example, we would continue as long as our <code>stepsFromHome</code> variable was less than <code>3000</code> steps.</li></ul></li>
    <li>The <u>update</u> expression should <strong>change</strong> the value of the variable at some point during each iteration.
      <ul><li>In our real-life example, every iteration could be a "step" and we could increase the <code>stepsFromHome</code> variable by <code>1</code> step each time.</li></ul></li>
  </ul>
</p>
<p>There are 3 types of loops in C, which rearrange these parts to make them more ideal for certain circumstances.</p>
<h4><a name="for"><code>for</code></a></h4>
<p>The <code>for</code> loop conveniently combines the required expressions in between the parenthesis. The general format is<br>
<pre><code>for(expression1; expression2; expression3){
  //loop body
}</code></pre>
where <code>expression1</code> is the <u>initialization</u> expression, <code>expression2</code> is the <u>controlling</u> expression, and <code>expression3</code> is the <u>update</u> expression.<br><br>
Our real-life example would look like this:<br>
<img src="https://github.com/user-attachments/assets/3a2d1e47-b36d-445e-8d90-be1a57b66801" width="500">
<br>
</p>
<h4><a name="while"><code>while</code></a></h4>
<p>The <code>while</code> loop includes the controlling expression between the parenthesis. The general format is<br>
<pre><code>while(control expression){
  //loop body, which should include the update expression
}</code></pre>
and the <u>initialization</u> expression is assumed to be included before the loop.<br><br>
Our real-life example would look like this:<br>
<img src="https://github.com/user-attachments/assets/f353f67c-6583-4e13-b6ea-6702f2933af0" width="350">
<br>
</p>
<h4><a name="do_while"><code>do while</code></a></h4>
<p>The <code>do while</code> loop moves the controlling expression to <em>after</em> the loop body. The general format is<br>
<pre><code>do{
  //loop body, which should include the update expression
}while(control expression);</code></pre>
and again, the <u>initialization</u> expression is assumed to be included before the loop. DON'T FORGET THE SEMICOLON!<br><br>
Our real-life example would look like this:<br>
<img src="https://github.com/user-attachments/assets/b02a4029-8d4a-402f-8e0a-33d9cb73a02a" width="360">
<br></p>
