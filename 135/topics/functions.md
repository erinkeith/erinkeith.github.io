<h2>Functions</h2>
<p><strong><em>Functions</em></strong> allow for <a href="https://www.lenovo.com/us/en/glossary/modularity/">modularity</a> in our programs.</p>
<p>
  "Modularity in computing and programming refers to dividing a system into separate modules or components. Each module handles a specific functionality and operates independently. It simplifies design, development, testing, and maintenance by allowing you to focus on one part at a time without affecting the rest of the system."
</p>
<p>
  Functions empower us to package up or enclose bits of code that will accomplish a particular <strong><em>task</em></strong> or <strong>BEHAVIOR</strong>. That function can be re-used whenever we need to execute that package of code in different parts of our programs, under different <strong><em>circumstances</em></strong> or <strong>STATE</strong>. For example, when drawing a table in our program to present some data, one of the tasks that the computer must perform could be drawing horizontal lines, like below. How many horizontal lines do you see?<br>
  <img src="https://github.com/user-attachments/assets/776dac77-a3a7-4ca5-accd-d52629d0b292">
</p>
<p>
  I counted 4!<br>
  <img src="https://github.com/user-attachments/assets/8a2766d6-a2c0-4877-816a-2b72ebdf81a9">
</p>
<p>
  The top and bottom lines (in orange) are 15 characters wide and use the equal sign <code>=</code>. It's important to note that the middle divider (in blue) is actually two different lines! While they both use the dash character <code>-</code>, the first line is 10 characters wide and the second is 5 characters wide. Since the things that vary between the lines are its width and the character used, we can identify those as the different circumstances (<strong>STATE</strong>). Also, since we can see it's useful to be able to display two lines without moving down the screen, moving to the next line is not part of the task of drawing a horizontal line (<strong>BEHAVIOR</strong>)! If we spend some time considering these conditions and circumstances, we can make our functions <strong>SPECIFIC ENOUGH TO ACCOMPLISH THE TASK, BUT GENERALIZABLE ENOUGH TO DO IT UNDER DIFFERENT CIRCUMSTANCES</strong>.
</p>
<ul>
    <li><a href="#syntax">Syntax</a>
    <ul><li><a href="#definition">Definitions</a></li>
    	 <li><a href="#call">Calls</a></li>
       <li><a href="#prototype">Prototypes</a></li>
    </ul></li>
    <li><a href="#metaphor">Metaphor: Like a Thanksgiving Dinner</a></li><!--
    <li><a href="#behavior">Behavior</a>
    <ul><li><a href="#input">Parameters vs Arguments</a></li>
        <li><a href="#scope">Scope and Duration</a></li>
        <li><a href="#output">Returned Values</a></li></ul>
    </li>-->
</ul>
  
<h3><a name="syntax">Syntax</a></h3>
  <h4><a name="definition">Definitions</a></h4>
  <p>
    Although there are many parts of incorporating functions into our programs, function <em>definitions</em> are at the core. They are where we put the code meant to accomplish the function's task or <strong>BEHAVIOR</strong>. Each function <em>definition</em> should include the <strong><em>return type</em></strong> of the function, the <strong><em>name</em></strong> of the function, a list of <strong><em>parameters</em></strong> and their data types, and the <strong><em>body</em></strong> of the function.
  </p> 
  <p>
    The <strong><em>return type</em></strong> should match the data type of any value that is sent out of the function back to another part of the program. If no value is sent back, the return type should be <code>void</code>, as we see below:<br>
<pre><code>void printHorizLine(int width, char symbol){
  for(int i = 0; i < width; i++){
    printf("%c", symbol);
  }
}</code></pre>
  </p>
  <p>
    The function <strong><em>name</em></strong> should be related to the task or <strong>BEHAVIOR</strong> the function performs, which helps our code read like a beautiful story! 
  </p>
  <p>
    <strong><em>Parameters</em></strong> are like special variables that save the values (<strong>STATE</strong>) sent into the function; they represent the <em>circumstances</em>. When we're writing a function definition, we just need to understand what the parameters represent. In our example above, the first <strong><em>parameter</em></strong> is a whole number that represents how many characters wide we want the line to be and the second <strong><em>parameter</em></strong> represents which character we'll be using for our line. Since these are the <em>circumstances</em> (<strong>STATE</strong>) that can change each time the function is used, the <strong><em>parameters</em></strong> are treated exactly like variables that already have a value stored in them; we don't have to worry about any actual values, but considering possible <em>circumstances</em> can help us write the code and catch any "edge cases".
  </p>
  <p>
    The function <strong><em>body</em></strong> is all of the code needed to accomplish the function's task (<strong>BEHAVIOR</strong>) and goes between the curly braces. Anything can go here, even other function <em>calls</em>!
  </p>
  <h4><a name="call">Calls</a></h4>
  <p>
    Speaking of function <em>calls</em>, let's get into them since we use them in our code where we want to see the actual <strong>BEHAVIOR</strong> of the function. Each function <em>call</em> should appropriately handle the <strong><em>returned value</em></strong> of the function (if there is one), reference the <strong><em>name</em></strong> of the function, and include a list of <strong><em>arguments</em></strong> to send into the function.
  </p>
  <p>
    If the function <strong><em>returns</em></strong> a value, the function <em>call</em> will evaluate to (be replaced by) it. Often the assignment operator <code>=</code> is used to store the <strong><em>returned value</em></strong> in another variable (although sometimes it can just be used directly). If the <strong><em>return type</em></strong> is <code>void</code>, then there's no <strong><em>returned value</em></strong> to consider, as demonstrated below:<br>
<pre><code>printHorizLine(15, '=');</code></pre>
  </p>
  <p>
    <strong><em>Arguments</em></strong> are the actual values (<strong>STATE</strong>) sent into the function; they are the specific <em>circumstances</em> for that instance or version of the function. In our example above, the first <strong><em>argument</em></strong> is the actual width of the line outlined in orange and the second <strong><em>argument</em></strong> is the actual character we want to use. Since the function <em>definition</em> is general enough to execute the task (<strong>BEHAVIOR</strong>) each time we send in different <strong><em>arguments</em></strong>, we get to re-use the function code each time we <em>call</em> it:<br>
<pre><code>printHorizLine(10, '-');</code></pre>
    This function <em>call</em> displays the first line outlined in blue!
  </p>
  <p>
    It's important to note that, while the data types of the arguments should match that of the function definition, data type keywords (like <code>int</code> or <code>char</code> should <strong>NOT</strong> be included in function calls.
  </p>
  <h4><a name="prototype">Prototypes</a></h4>
  <p>
    The final component of using functions in our programs will be function <em>prototypes</em>. While they aren't strictly necessary, they are considered a "best practice"; since using and understanding them will help students in future CSE courses, they will be required in this class. Luckily, they're pretty easy to incorporate!
  </p>
  <p>
    We just need to include all of the parts of function <em>definitions</em> before the <strong><em>body</em></strong> with a semicolon at the end:
  <pre><code>void printHorizLine(int width, char symbol);</code></pre>
  </p>
  <p>
    These new components change the overall structure of our program files:
    <ol>
      <li>header comments</li>
      <li>preprocessor directives</li>
      <li>function <em>prototypes</em></li>
      <li><code>main</code> function</li>
      <li>function <em>definitions</em></li>
    </ol>
    We can apply this new structure to put all the pieces of our example together:<br>
    <img src="https://github.com/user-attachments/assets/dd22e020-40bc-43c5-8c87-5927b4a8e867" width="400">
  </p>
<!--
<h3><a name="behavior">Behavior</a></h3>
  <h4><a name="input">Parameters vs Arguments</a></h4>
  <p>represent the "different circumstances"</p>
  <h4><a name="scope">Scope and Duration</a></h4>
  <h4><a name="output">Returned Values</a></h4>
-->
<h3><a name="metaphor">Metaphor: Like a Thanksgiving Dinner</a></h3>
<p>
  We've examined how programs are very similar to food recipes and we can take that comparison even further by considering preparing an entire meal. To prepare our meal we gather multiple recipes for multiple dishes, depending on what we want to serve that year. Some years we skip the cranberry sauce, some years we try a new recipe for cinnamon carrots (at least in my house!). Our meal system is more flexible when we keep the dishes <em>modular</em> and we can more easily assign the recipes to different family members to work on. As an added bonus, it would be easier to test an individual recipe without having to make the entire meal!
</p>
<p>
  While this comparison can help us understand why functions are important, it can also help us understand how to incorporate them into our programs if we imagine these recipes in a recipe book! The actual recipes themselves are like function <strong><em>definitions</em></strong>, since they contain the necessary instructions. The function <strong><em>call</em></strong> would be similar to when we actually use the recipe to make the dish. The function <strong><em>prototypes</em></strong> are like the table of contents at the beginning of the book, which is very convenient for finding the recipe pages when we need them.
</p>
<p>
  Finally, if we consider ingredients to be like <strong><em>arguments</em></strong> into the functions and the final dish as the <strong><em>returned output</em></strong>, the <strong><em>main</em></strong> function/chef becomes responsible for coordinating the larger aspects of the meal. They must guarantee the right ingredients are already in the kitchen (it would be strange to ask your uncle to make pumpkin pie, then tell him he has to go to the store first). They must make decisionns to synchronize the timing of when to start the dishes so everything can be ready to serve at roughly the same time. Finally, they must ensure there are enough serving bowls and platters to store finished dishes for the meal itself.<br>
  <img src="https://github.com/user-attachments/assets/b36395d8-dfab-4806-b0d0-f1a24c861075" width="200">
</p>
