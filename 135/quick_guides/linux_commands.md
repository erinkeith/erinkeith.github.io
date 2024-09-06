<p>These should be typed into the terminal window in a Linux Development Environment</p>
<p>The examples provided utilize the "current working directory" but can be used with an "absolute path". <a href="https://www.redhat.com/sysadmin/linux-path-absolute-relative" target="_blank" rel="noopener">https://www.redhat.com/sysadmin/linux-path-absolute-relative</a></p>
<table style="border-collapse: collapse; width: 97.8887%;" border="1">
    <tbody>
        <tr>
            <td style="width: 24.9755%;"><strong>Action</strong></td>
            <td style="width: 24.9755%;"><strong>Command</strong></td>
            <td style="width: 24.9755%;"><strong>Description</strong></td>
            <td style="width: 24.9755%;"><strong>Example</strong></td>
        </tr>
        <tr>
            <td style="width: 24.9755%;">Change Directory</td>
            <td style="width: 24.9755%;"><strong><span style="font-family: 'courier new', courier;">cd</span></strong></td>
            <td style="width: 24.9755%;">change from your current directory into the one specified<br /><br /></td>
            <td style="width: 24.9755%;">
                <p><strong><span style="font-family: 'courier new', courier;">cd ExampleFolder</span></strong><br />move from the current directory into the one called <span style="font-family: 'courier new', courier;">ExampleFolder</span></p>
                <p><strong><span style="font-family: 'courier new', courier;">cd ..</span></strong></p>
                <p>go back (or "up") to the previous&nbsp; directory</p>
            </td>
        </tr>
        <tr>
            <td style="width: 24.9755%;">List Contents</td>
            <td style="width: 24.9755%;"><strong><span style="font-family: 'courier new', courier;">ls</span></strong></td>
            <td style="width: 24.9755%;">show all the files and directories in the specified directory</td>
            <td style="width: 24.9755%;">
                <p><strong><span style="font-family: 'courier new', courier;">ls</span></strong><br />show everything contained in the current directory</p>
                <p><strong><span style="font-family: 'courier new', courier;">ls project4</span></strong><br />show everything contained in the <span style="font-family: 'courier new', courier;">project4</span> directory (assuming it is in your current directory)</p>
            </td>
        </tr>
        <tr>
            <td style="width: 24.9755%;">Remove (delete)</td>
            <td style="width: 24.9755%;"><strong><span style="font-family: 'courier new', courier;">rm</span></strong></td>
            <td style="width: 24.9755%;">
                <p>delete specified file or directory</p>
                <p>use the <strong><span style="font-family: 'courier new', courier;">-r</span></strong> flag to delete a directory and all of its contents</p>
            </td>
            <td style="width: 24.9755%;">
                <p><strong><span style="font-family: 'courier new', courier;">rm monkey.txt</span></strong><br />delete <span style="font-family: 'courier new', courier;">monkey.txt</span> from the current directory</p>
                <p><strong><span style="font-family: 'courier new', courier;">rm -r banan</span></strong><br />delete the <span style="font-family: 'courier new', courier;">banan</span> folder and all of its contents</p>
            </td>
        </tr>
        <tr>
            <td style="width: 24.9755%;">Create a file</td>
            <td style="width: 24.9755%;"><strong><span style="font-family: 'courier new', courier;">touch</span></strong></td>
            <td style="width: 24.9755%;">
                <p>create a file with the specified name</p>
            </td>
            <td style="width: 24.9755%;">
                <p><strong><span style="font-family: 'courier new', courier;">touch banan.c</span></strong><br />create a file called <span style="font-family: 'courier new', courier;">banan.c</span> in the current directory</p>
            </td>
        </tr>
        <tr>
            <td style="width: 24.9755%;">Create a folder</td>
            <td style="width: 24.9755%;"><strong><span style="font-family: 'courier new', courier;">mkdir</span></strong></td>
            <td style="width: 24.9755%;">
                <p>create a folder (aka directory) with the specified name</p>
            </td>
            <td style="width: 24.9755%;">
                <p><strong><span style="font-family: 'courier new', courier;">mkdir monkey_directory</span></strong><br />create a folder called <span style="font-family: 'courier new', courier;">monkey_directory</span> in the current directory</p>
            </td>
        </tr>
    </tbody>
</table>
<p>&nbsp;</p>
