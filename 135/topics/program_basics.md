<a href="#anchor">Quick Reference</a>
<p>Generally, the code we write in this class will run <a href="https://www.dictionary.com/browse/sequentially"><i>sequentially</i></a>, so we should have a well-defined, consistent starting point. Enter the <strong><span style="font-family: 'courier new', courier;">main</span></strong> function! (We'll learn about "functions" later, I promise!)</p>

<p>Every program in C must include a <strong><span style="font-family: 'courier new', courier;">main</span></strong> function. While you may see some variations of the format in the wild, our programs will always start with</p>

<code>int main(){</code>

<p>and end with</p>

<code>   return 0;
}</code>

<p>All our other code (at least to start with) will go between those two parts.</p>

<p>As far as "behavior" (what the computer does when we run our program), this code doesn't really <i>do</i> anything, but it is required and can be considered the "start" of our programs.</p>

<p>Many questions about how to code get a "it depends" answer, but this is something you can just memorize! The first code you should write in every program file should be:</p>

<code>int main(){
    return 0;
}</code>

<p>If this is missing, you will see an error when trying to compile<a href="#anchor">*</a>. For example: </p>

<a name="Quick Reference"></a>
<table style="border-collapse: collapse; width: 97.9535%; border-style: none; height: 587px;" border="1">
    <tbody>
        <tr style="height: 28px; border-style: groove;">
            <td style="width: 10%; border-style: none; height: 28px;"><strong>Level</strong></td>
            <td style="width: 15%; border-style: none; height: 28px;"><strong>Components</strong></td>
            <td style="width: 16.6508%; border-style: none; height: 28px;"><strong>Example</strong></td>
            <td style="width: 16.6508%; border-style: none;"><strong>Explanation</strong></td>
        </tr>
        <tr style="height: 203px; border-style: groove;">
            <td style="width: 10%; border-style: none; height: 203px;">Required Syntax</td>
            <td style="width: 15%; border-style: none; height: 203px;">
                <ul style="list-style-type: disc;">
                    <li>preprocessor directives</li>
                    <li>the main function</li>
                </ul>
            </td>
            <td style="width: 16.6508%; border-style: none; height: 203px;"><img src="https://webcampus.unr.edu/courses/109022/files/12923823/preview" alt="Required Syntax" width="277" height="162" data-api-endpoint="https://webcampus.unr.edu/api/v1/courses/109022/files/12923823" data-api-returntype="File" /></td>
            <td style="width: 16.6508%; border-style: none;">
                <ul>
                    <li>If you don't include the correct library for functions you call but don't write, there will be a compiler error.</li>
                    <li>All programs must have exactly one main function to compile and run.</li>
                </ul>
            </td>
        </tr>
        <tr style="height: 356px; border-style: groove;">
            <td style="width: 10%; border-style: none; height: 356px;">Conventions</td>
            <td style="width: 15%; border-style: none; height: 356px;">
                <ul>
                    <li>preprocessor directives
                        <ul>
                            <li><strong style="font-family: inherit; font-size: 1rem;">including "macros"</strong></li>
                        </ul>
                    </li>
                    <li>the main function
                        <ul>
                            <li><strong style="font-family: inherit; font-size: 1rem;"><span style="font-family: 'courier new', courier;">return 0;</span> statement at the end</strong></li>
                        </ul>
                    </li>
                </ul>
            </td>
            <td style="width: 16.6508%; border-style: none; height: 356px;"><img src="https://webcampus.unr.edu/courses/109022/files/12923826/preview" alt="Conventions" width="277" height="168" data-api-endpoint="https://webcampus.unr.edu/api/v1/courses/109022/files/12923826" data-api-returntype="File" /></td>
            <td style="width: 16.6508%; border-style: none;">
                <ul>
                    <li>Macros are like labels which make values in your code easier to read
                        <ul>
                            <li>a variable is not the right tool since the value doesn't change</li>
                            <li>use all caps so you can tell the difference!</li>
                        </ul>
                    </li>
                    <li>The <strong style="font-family: inherit; font-size: 1rem;"><span style="font-family: 'courier new', courier;">return 0;</span></strong> statement tells the operating system that the program finished running without issues.</li>
                </ul>
            </td>
        </tr>
        <tr style="border-style: groove;">
            <td style="width: 10%; border-style: none;">Best Practices</td>
            <td style="width: 15%; border-style: none;">
                <ul>
                    <li><strong>header comments</strong></li>
                    <li>preprocessor directives
                        <ul>
                            <li><strong style="font-family: inherit; font-size: 1rem;">only include libraries that are used in that program</strong></li>
                            <li>including "macros"</li>
                        </ul>
                    </li>
                    <li>the main function
                        <ul>
                            <li><strong>consistent indentation</strong></li>
                            <li>return 0 statement at the bottom</li>
                        </ul>
                    </li>
                </ul>
            </td>
            <td style="width: 16.6508%; border-style: none;"><img src="https://webcampus.unr.edu/courses/109022/files/12923827/preview" alt="Best Practices" data-ally-user-updated-alt="Best Practices" data-api-endpoint="https://webcampus.unr.edu/api/v1/courses/109022/files/12923827" data-api-returntype="File" /></td>
            <td style="width: 16.6508%; border-style: none;">
                <ul>
                    <li>Header comments give the reader more information, like who wrote the program.</li>
                    <li>Including libraries that aren't used can cause performance issues.</li>
                    <li>Indentation makes code easier by indicating where different blocks of code begin and end.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>
<a name="*"></a>* <p>Technically, you only need 

<code>int main(){

}</code>

but it's a best practice to include the return statement and grading will reflect that. Again, there are a couple of valid variations of this, but you'll see the format above in this class.</p>