<p>Skip the explanation and go straight to the <a href="https://erinkeith.github.io/135/quick_guides/program_basics">Quick Guide</a>.</p>
<h2>In the beninging</h2>
<p>Generally, the code we write in this class will run <a href="https://www.dictionary.com/browse/sequentially"><i>sequentially</i></a>, so we should have a well-defined, consistent starting point. Enter the <strong><span style="font-family: 'courier new', courier;">main</span></strong> function! (We'll learn about "functions" later, I promise!)</p>

<p>Every program in C must include a <strong><span style="font-family: 'courier new', courier;">main</span></strong> function. While you may see some variations of the format in the wild, our programs will always start with</p>

![begin](https://github.com/user-attachments/assets/b59b5a94-c04e-4ed8-a672-b99e2c7b82f1)

<p>and end with</p>

![end](https://github.com/user-attachments/assets/7f7760f4-a856-4b7b-919e-0cb0007a4c0f)

<p>All our other code (at least to start with) will go between those two parts.</p>

<p>As far as "behavior" (what the computer does when we run our program), this code doesn't really <i>do</i> anything, but it is required and can be considered the "start" of our programs. So many questions about how to code are answered with "it depends", but this is something you can just memorize!</p> 

![preferred](https://github.com/user-attachments/assets/47c859fc-6649-4f76-bd66-40a6331ce9b7)

<p>If this is missing (or certain parts of it), you will see an error when trying to compile [<a href="#1">1</a>]. For example, compiling a program with: </p>

<pre><code>int main{

   return 0;
}</code></pre>

<p>will result in: </p>

![error](https://github.com/user-attachments/assets/235c00a6-14a2-4731-85fb-3cf3f578dedd)

<p>because the parentheses are missing before the curly brace on line 1. Compiler errors are pretty cryptic, but with some practice they'll start to make some sense.</p>

![error_notated](https://github.com/user-attachments/assets/81a11340-186f-4b6f-9435-8f22196ac473)

<h2>Comments</h2>

<p>Although code is also for communicating with humans, some things are easier in our every day language than in a programming language. Luckily, we can use <i>comments</i> for that. Any comments in our program files get ignored by the compiler, and therefore the computer. It's a great way to leave future-you a little note about what the heck you were thinking!</p>

<p>There are two types of comments in C:</p>

Single-line comments start with 2 forward slashes <code>//</code> and they end automatically at the end of the line.

Multi-line comments start with a forward slash then asterisk <code>/*</code> but only end after the reverse <code>*/</code> (an asterisk then forward slash).

<p>In most cases, especially if you have a short note, single-line comments will do. In this class, you will be expected to include what we call "header comments" at the top of each program file. It's a good habit to get into and it will help the graders do their work! You can use whatever kind of comments you like, but an example of my preferred style is below.</p>

<p><a name="PreferredFormat">The first code you should write in every program file should be:</a></p>

![with_comments](https://github.com/user-attachments/assets/7e6b5e76-18a1-4e67-a6ae-05c2b49e747f)

<p><a name="1">1</a> Technically, you only need</p>

<pre><code>int main(){

}</code></pre>

<p>but it's a best practice to include the return statement and grading will reflect that. Again, there are a couple of valid variations of this, but in this class you'll see the <a href="#PreferredFormat">preferred format</a>.</p>
