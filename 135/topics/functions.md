<h2>Functions</h2>
<p><strong><em>Functions</em></strong> allow for <a href="https://www.lenovo.com/us/en/glossary/modularity/">modularity</a> in our programs.</p>
<p>
  "Modularity in computing and programming refers to dividing a system into separate modules or components. Each module handles a specific functionality and operates independently. It simplifies design, development, testing, and maintenance by allowing you to focus on one part at a time without affecting the rest of the system."
</p>
<p>
  Functions empower us to package up or enclose bits of code that will accomplish a particular task (<strong><em>BEHAVIOR</em></strong>). That function can be re-used whenever we need to execute that package of code in different parts of our programs, under different circumstances (<strong><em>STATE</em></strong>). For example, when drawing a table in our program to present some data, one of the tasks that the computer must perform could be drawing horizontal lines, like below. How many horizontal lines do you see?<br>
  <img src="https://github.com/user-attachments/assets/776dac77-a3a7-4ca5-accd-d52629d0b292">
</p>
<p>
  I counted 4!<br>
  <img src="https://github.com/user-attachments/assets/8a2766d6-a2c0-4877-816a-2b72ebdf81a9">
</p>
<p>
  The top and bottom lines (in orange) are 15 characters wide and use the equal sign <code>=</code>. It's important to note that the middle divider (in blue) is actually two different lines! While they both use the dash character <code>-</code>, the first line is 10 characters wide and the second is 5 characters wide. Since the things that vary between the lines are its width and the character used, we can identify those as the different <em>circumstances</em> (<strong><em>STATE</em></strong>). Also, since we can see it's useful to be able to display two lines without moving down the screen, moving to the next line is not part of the task of drawing a horizontal line (<strong><em>BEHAVIOR</em></strong>)! If we spend some time considering these conditions and circumstances, we can make our functions <strong>SPECIFIC ENOUGH TO ACCOMPLISH THE TASK, BUT GENERALIZABLE ENOUGH TO DO IT UNDER DIFFERENT CIRCUMSTANCES</strong>.
</p>
<ul>
    <li><a href="#syntax">Syntax</a>
    <ul><li><a href="#definition">Definitions</a></li>
        <li><a href="#call">Calls</a></li>
        <li><a href="#prototype">Prototypes</a></li></ul>
    </li>
    <li><a href="#behavior">Behavior</a>
    <ul><li><a href="#input">Parameters vs Arguments</a></li>
        <li><a href="#scope">Scope and Duration</a></li>
        <li><a href="#output">Returned Values</a></li></ul>
    </li>
    <li><a href="#metaphor">Metaphors</a></li>
    <ul><li><a href="#chapters">Like a Chapter Book</a></li></ul>
</ul>
  
<h3><a name="syntax">Syntax</a></h3>
  <h4><a name="definition">Definitions</a></h4>
  <p>
    Although there are many parts of incorporating functions into our programs, function <strong><em>definitions</em></strong> are at the core. They are where we put the code meant to accomplish the function's task. 
  </p>
  <h4><a name="call">Calls</a></h4>
  <h4><a name="prototype">Prototypes</a></h4>
<h3><a name="behavior">Behavior</a></h3>
  <h4><a name="input">Parameters vs Arguments</a></h4>
  <p>represent the "different circumstances"</p>
  <h4><a name="scope">Scope and Duration</a></h4>
  <h4><a name="output">Returned Values</a></h4>

<h3><a name="metaphor">Metaphors</a></h3>
  <h4><a name="chapters">Like a Chapter Book</a></h4>

[<a href="#note">1</a>]
<a name="note">1</a>. Explanation.<br>
