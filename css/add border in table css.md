# Add border in table CSS example
In this page I will show you how to add border CSS in table. It is better add border in table before adjusting
width and height. Example is here
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Add border in table css</title>
</head>
<body>
<style type="text/css">
    table {
        border-collapse: collapse;
    }

    table td, th, tr {
        border: 1px solid red;
    }
</style>
<table>
    <tr>
        <th>Name</th>
        <th>age</th>
        <th>address</th>
    </tr>
    <tr>
        <td>Henry</td>
        <td>28</td>
        <td>Beijing</td>
    </tr>
    <tr>
        <td>Justin</td>
        <td>28</td>
        <td>Shanghai</td>
    </tr>
    <tr>
        <td>Matthews</td>
        <td>21</td>
        <td>Guangzhou</td>
    </tr>
</table>
</body>
</html>
```
Don't recommend use table if you want show large content. `table` won't show until the content loading complete.
Another disadvantage is change width or height will affect other rows.