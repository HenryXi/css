# JQuery add remove tr in table
In this page I will show you how to use JQuery remove and add `tr` element in `table`. Copy the code following and
click remove or add button. If you do not want remove the first `tr` element or add after last `tr` element just
change the JQuery selector.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Jquery remove add class</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.3/jquery.min.js"></script>
    <script type="text/javascript">
        $(document).ready(function () {
            $("button").click(function () {
                $("p:first").removeClass("old").addClass('new new2');
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