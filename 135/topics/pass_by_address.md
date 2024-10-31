<h2>Pass by Address</h2>
<p>
  Pass by Address utilizes pointers as parameters to bypass the limitations of scope and allow access to variables outside of the function. In our class, this is often to used to "output" multiple values instead of being constrained by the single value we can output through the function return mechanism.
</p>
<ul>
    <li><a href="#background">Background</a>
    <ul><li><a href="#value">Pass by Value</a></li>
        <li><a href="#pointers">Pointers</a></li></ul>
    <li><a href="#syntax">Syntax</a></li>
    <li><a href="#behavior">Behavior</a>
</ul>
<h3><a name="background">Background</a></h3>
<p>
  Pass by Address is a pretty complex concept, in large part because it combines many technical details to be able to accomplish something kind of abstract, so covering some background knowledge first might be helpful.
</p>
<h4><a name="value">Pass by Value</a></h4>
<p>It might help to start by examining the default method of managing parameters in C: Pass by Value.</p>
<p>
  In C (and C++), the default approach for managing "input" during a function call is to copy the value of the matching argument and store it in the function parameter. This supports scope rules by reinforcing a very concrete boundary around the functions and separating the arguments from the parameters. Any changes made to the parameter within the function do not affect the original argument at all (if it seems like it does, then it's actually Pass by Address under the hood).
</p>

<p>
  We've delved a little into how <a href="https://erinkeith.github.io/135/topics/variables#behavior">variables</a> work, so now it's time to contemplate a new level of data type! During runtime, the variable name is bound to a memory address that the operating system chooses. While we can't/shouldn't determine what that memory address is, we can not only access it, we can store it! And that's what pointers are for.
</p>
<p>
  Pointers are a special kind of variable that are specifically for storing the memory addresses of other variables. As such, pointers are only ever used as a reference to another variable and they must be "pointed" to one to work properly (we'll go over the syntax and details of that below).
</p>
<p>
  They're useful in a couple of situations that you'll cover in CS 202 (like polymorphism and dynamic memory allocation) or CPE courses, but we'll use them almost exclusively for Pass by Address (and just a smidge for File IO). Because of that, we'll cover general pointer syntax under the background section.
</p>
<h5>Declaration</h5>
<p>
  A big difference when using pointers is the data type portion of the declaration. Because they are a used as references to other variables, we must consider what type of variable they will "point" to, which gets used in the declaration. For example, if we need a pointer to point to an integer variable, the declaration will include the <code>int</code> type, along with an asterisk <code>*</code>:<br>
  <code>int* agePtr;</code><br>
  (I often add "<code>ptr</code>" to the end of the pointer variable name to help me keep track of things)
</p>
<h5>Assignment</h5>
<p>
  We won't do it in this class, but if you wanted to explicitly point at a variable, that other variable must first exist (order is important here!). Then we can combine the address of operator <code>&</code> with the assignment operator <code>=</code>:<br>
  <pre><code>int age;
  int* agePtr;

  agePtr = &age;</code></pre>
</p>
<h5>Aliasing</h5>
<p>
  Finally, once a pointer is referencing another variable, the pointer can be used as a alias by appling the dereference operator <code>*</code>:<br>
  <pre><code>int age = 0;
  int* agePtr;

  agePtr = &age;
  *agePtr = 45; // uses the pointer as an alias to save 45 in the age variable
  printf("%d\n", age); // would display 45
</code></pre>
</p>
<h3><a name="syntax">Syntax</a></h3>

<h3><a name="behavior">Behavior</a></h3>
<p>
  First of all, let's be clear that when we talk about "output" with respect to functions, we must determine which of the following 3 techniques are appropriate:
  <ol>
    <li>program output, like to the <a href="https://erinkeith.github.io/135/topics/formatted_io#printf">console</a> or a file</li>
    <li><a href="https://erinkeith.github.io/135/topics/functions#definition">returned</a> output, which can only be one value</li>
    <li>pass by address, which allows for "outputting" multiple values</li>
  </ol>
</p>
