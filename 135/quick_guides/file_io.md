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

<h2>File IO Quick Guide</h2>
<table>
    <tr>
        <th>Type</th>
        <th>Application</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Notes</th>
    </tr>
    <tr>
        <td><code>FILE*</code>'s<br>
            <code>fopen</code><br>
            <code>fclose</code><br>
        </td>
        <td>before you can interact with a file, you need to create a connection or <strong><em>stream</em></strong></td>
        <td><img src="https://github.com/user-attachments/assets/d858a786-ec2f-4612-93fe-439b5bceee30"></td>
        <td><ol>
            <li>save the connection
                <ul><li>declare a <code>FILE</code> pointer</li></ul>
            </li>
            <li>open the file
                <ul><li>call the <code>fopen</code> function<br>
                        <ul><li>send in the filename string</li>
                            <li>send in the mode string (double quotes, not single!)
                                <ul><li><code>"r"</code> is read</li>
                                    <li><code>"w"</code> is write</li>
                                    <li><code>"a"</code> is append</li>
                                </ul>
                            </li>
                       </ul>
                  </li></ul>
             </li>
             <li>verify the connection is made
                 <ul><li>check the <code>FILE</code> pointer for the <code>NULL</code> pointer
                         <ul><li>if it's the <code>NULL</code> pointer, quit</li>
                             <li><u><strong>CAUTION</strong></u>! If the <code>FILE</code> pointer is <code>NULL</code>, you will get a segmentation fault if you use it.</li>
                         </ul>
                 </li></ul>
             </li>
             <li>close the connection (after interacting with the file)
                 <ul><li>call the <code>fclose</code> function
                         <ul><li>send in the <code>FILE</code> pointer</li></ul>
                 </li></ul>
             </li>
        </ol></td>
    </tr>
    <tr>
        <td><code>fprintf</code></td>
        <td><strong><em>outputs</em></strong> text to a <strong><em>stream</em></strong></td>
        <td><img src="https://github.com/user-attachments/assets/f689dd44-ed15-48ba-9e4a-241cf882c153"></td>
        <td><ul>
            <li>this looks just like Formatted IO, but with the <code>FILE</code> pointer as the <strong>first</strong> argument</li>
            <li>you can use still things like field width and precision to format how your output looks</li></ul>
        </td>
    </tr>
    <tr>
        <td><code>fscanf</code></td>
        <td>gets <strong><em>input</em></strong> text from a <strong><em>stream</em></strong></td>
        <td><img src="https://github.com/user-attachments/assets/51af4c38-d26b-49b2-9f05-ca1f673f70c4"></td>
        <td><ul>
            <li>this looks just like Formatted IO, but with the <code>FILE</code> pointer as the <strong>first</strong> argument</li></ul>
        </td>
    </tr>
    <tr>
        <td><code>fgets</code></td>
        <td>gets <strong><em>input</em></strong> text as a <a href="https://erinkeith.github.io/135/topics/strings#fgets">C-Style String</a> from a <strong><em>stream</em></strong></td>
        <td><img src="https://github.com/user-attachments/assets/4d6efcea-fae2-44b1-9427-e2c14404934e"></td>
        <td><ul>
            <li>this looks just like Formatted IO with <a href="https://erinkeith.github.io/135/topics/strings#fgets">C-Style Strings</a>, but with the <code>FILE</code> pointer as the <strong>last</strong> argument</li></ul>
        </td>
    </tr>
</table>
