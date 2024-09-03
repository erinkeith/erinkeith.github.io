<style>
    table{
        width:100%;
    }
    td{
        vertical-align: top;
    }
    img{
        height: auto;
        max-width: 100%;
    }
</style>

<h2>Program Basics Quick Guide</h2>
<table>
    <tr>
        <th >Level</th>
        <th >Components</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Explanation</th>
    </tr>
    <tr>
        <td>Required Syntax</td>
        <td>
            <ul>
                <li>preprocessor directives</li>
                <li>the main function</li>
            </ul>
        </td>
        <td>
            <img src="https://github.com/user-attachments/assets/d8ef632a-7a25-4399-afdf-3efd216fcba0">
        </td>
        <td>
            <ul>
                <li>If you don't include the correct library for functions you call but don't write, there will be a compiler error.</li>
                <li>All programs must have exactly one main function to compile and run.</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Conventions</td>
        <td>
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
        <td><img src="https://github.com/user-attachments/assets/d99fc476-a933-4228-80ff-0a97b4fcb576"></td>
        <td>
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
    <tr>
        <td>Best Practices</td>
        <td>
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
        <td><img src="https://github.com/user-attachments/assets/b78a17e7-09b1-4af7-87f3-b2441124277d"></td>
        <td>
            <ul>
                <li>Header comments give the reader more information, like who wrote the program.</li>
                <li>Including libraries that aren't used can cause performance issues.</li>
                <li>Indentation makes code easier by indicating where different blocks of code begin and end.</li>
            </ul>
        </td>
    </tr>
</table>
