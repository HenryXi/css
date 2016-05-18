# Jquery change element class
We can not change class of element directly. But we can use two steps to change class. Remove old then
add new one. Use ``addClass()`` function to add a class to each element. If you want add more than one class 
separating each one with a space. This function won't delete exist class it only append the specified 
class. Use ``removeClass()`` function to remove a class. Same as ``addClass()`` use space to separate
multiple classes if you need remove more than one class.
```lang-html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Jquery remove add class</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.3/jquery.min.js"></script>
    <script type="text/javascript">
        $(document).ready(function () {
            $("button").click(function () {
                $("p:first").removeClass("old").addClass('new');
            });
        });
    </script>
    <style type="text/css">
        .old {
            font-size: 120%;
            color: red;
        }

        .new {
            font-size: 90%;
            color: blue;
        }
        .new2 {
            background-color: yellow;
        }
    </style>
</head>
<body>
<h1>Jquery remove add class</h1>
<p class="old">when click the button will change the style of this paragraph.</p>
<p>This paragraph won't be changed.</p>
<button>Change</button>
</body>
</html>
```
When click the button jquery select the first paragraph. Use ``removeClass()`` to remove class "old"
 then use ``addClass()`` to add new classes "new" and "new2". 