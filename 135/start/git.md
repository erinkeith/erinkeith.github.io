<h2>We've got it <i>under control</i></h2>
<p>This page will provide background information on a very common industry tool we'll be using to support our project submission process.</p>

<h3>git</h3>

![git_defined](https://github.com/user-attachments/assets/f3581fd2-d71e-4f60-8580-89ec393ba9d7)

But what is "version control" (also know as "source control")? You can find an explanation here: https://aws.amazon.com/devops/source-control/

git is the application that gets installed onto your computer (git Setup) and is what's being "invoked" when you run the submission commands:

<code>
git add .
git commit -m "your commit message"
git push
</code>

<h3>GitHub</h3>

GitHub, on the other hand, is a way to view the "remote" version of the repository through a web browser. This is where you can get the URL for the clone command and it's where you can go to verify that the GitHub Submission process worked.

<h3>GitHub Classroom</h3>

"GitHub Classroom is a teaching tool that lets teachers and school administrators create and manage digital classrooms and assignments."

After I create the assignment in GitHub Classroom, a link to the assignment is created (which is what I include in WebCampus). Staff can see student submissions in their remote repositories (usually through GitHub) and can even download or clone them. This is why I request the repository link when students ask for help with their code.

GitHub Classroom also provides an "Autograder" functionality. While we don't use it for grading, it can be a helpful way for students to get quick feedback as to whether or not they're on the right track. I've put together more information on Using the GitHub Classroom Autograder , as it can be challenging to understand the messages.

<h3>Collaboration</h3>

For most of the semester, we use GitHub Classroom to manage the submission process but one of the greatest benefits of git is its support of collaboration, which will be useful during your Final Group Project. 

As such, you'll be adding a new <strong><span style="font-family: 'courier new', courier;">pull</span></strong> command to your repertoire! This command allows you to incorporates changes from a remote repository into your local repository. This means that if your groupmate <strong><span style="font-family: 'courier new', courier;">push</span></strong>es something, you can use the <strong><span style="font-family: 'courier new', courier;">pull</span></strong> command to easily get those changes onto your computer. This is the most basic process for most software engineering!

Throughout this process of <strong><span style="font-family: 'courier new', courier;">push</span></strong>ing and <strong><span style="font-family: 'courier new', courier;">pull</span></strong>ing, it's very common to encounter something called a "merge conflict". Although many things can cause a merge conflict, you would probably encounter it when multiple people try changing the same line in the same file. If you see a message in the terminal window about a "merge conflict", usually the fix is to "resolve the conflict" by editing the document. You can find more information on <a title="Resolving Merge Conflicts" href="https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line">Resolving Merge Conflicts</a> in the linked documentation.

<h3>Summary</h3>

GitHub classroom makes managing and grading these assignments much easier. For students to be able to participate, they must create GitHub accounts and have git installed in their development environment. Additionally, familiarity with git will make working in your Final Project Group easier and help prepare you to be able to contribute to professional-level projects.
