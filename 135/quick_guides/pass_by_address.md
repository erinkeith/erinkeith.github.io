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

<h2>Pass by Address Quick Guide</h2>
<table>
    <tr>
        <th>Component</th>
        <th>Notes</th>
        <th style="width:40%">Example</th>
        <th style="width:35%">Operator</th>
    </tr>
    <tr>
        <td>prototype</td>
        <td>parameter data types are <strong><em>pointers</em></strong></td>
        <td><img src="https://github.com/user-attachments/assets/58146713-4842-44b8-a34a-ecb8012cb2ec"></td>
        <td><code>*</code></td>
    </tr>
    <tr>
        <td>call</td>
        <td>arguments are the <strong><em>addresses of</em></strong> the variables which will be accessed in the <em>function definition</em></td>
        <td><img src="https://github.com/user-attachments/assets/9f52faef-d639-4d04-acbd-821b945b063a"></td>
        <td><code>&</code></td>
    </tr>
    <tr>
        <td>definition</td>
        <td><em>pointer</em> parameters are <strong><em>de-referenced</em></strong> to access the original variables' values</td>
        <td><img src="https://github.com/user-attachments/assets/249d2b6d-e4fd-4c4f-a185-fcae51d741ee"></td>
        <td><code>*</code></td>
    </tr>
</table>
