<h2>Using the "Autograder"</h2>
<p>Git includes a useful feature that allows for easy, automated testing of code. This testing serves two purposes: it allows graders to easily verify that your code compiled and it allows students to compare the output of their program to the correct output.<br> 
  <strong>Aside from verifying compilation, this tool is not used for grading purposes (even though it's called the "autograder").</strong></p>

<p>This tool runs automatically every time you submit your code via git. You can see the output from the GitHub website. If all of the tests pass, there will be a green checkmark above the list of files:<br>
  <img width="561" height="252" alt="greenCheck" src="https://github.com/user-attachments/assets/7298e20e-53e9-4c85-b2b8-b07de38b2ec9" /></p>

<p>If there is a red X, that means your tests did not pass. You can click on the red X, then the Details link for more information:<br>
  <img width="581" height="238" alt="redX" src="https://github.com/user-attachments/assets/b8c3d831-b797-4f58-a662-abde3117163e" /></p>

<p>There may be multiple tests with different names. Tests which pass will have a green check:<br>
  <img width="118" height="122" alt="compile" src="https://github.com/user-attachments/assets/28dac3c2-9861-4f92-aeeb-998c2802a3ea" /></p>

<p>Tests which don't pass will have a red X:<br>
  <img width="116" height="54" alt="runProgram" src="https://github.com/user-attachments/assets/0d911946-e310-4eda-94ad-40782c15482e" /></p>

<p>Your program's output is above the error message:<br>
  <img width="893" height="379" alt="yourOutput" src="https://github.com/user-attachments/assets/3b9733ba-9b0d-4057-932f-7826d70fc4f7" /></p>

<p>The expected output is below, but doesn't include any endline characters (so it looks pretty jumbled):<br>
  <img width="1160" height="209" alt="expectedOutput" src="https://github.com/user-attachments/assets/59bd7e6f-84e5-41c1-b937-cde4e754e7db" /></p>

<p>It can be difficult to find the difference if it's a matter of spacing, in which case you don't need to worry; it won't affect your grade. <strong>Make sure that the output values match, though, so you can verify that any processing your program does is correct.</strong> For example above, the issue is a typo in the header row. The output values match, though, so this program would get a high grade.</p>
