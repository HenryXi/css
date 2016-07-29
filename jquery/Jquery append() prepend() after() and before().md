# JQuery append() prepend() after() and before()
There are some methods in JQuery change the content of page. Different method add the element to different position.
In this blog I will show you the different of them. You can also save the following code as html file and run it.
Click the different button can add the different element to the page.

**demo code**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Jquery append() prepend() after() and before()</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.3/jquery.min.js"></script>
    <script type="text/javascript">
        $(document).ready(function () {
            $("#append").click(function () {
                $("#target").append(function () {
                    return "<p>append the other paragraph" + "</p>";
                });
            });
            $("#prepend").click(function () {
                $("#target").prepend(function () {
                    return "<p>prepend the other paragraph" + "</p>";
                });
            });
            $("#after").click(function () {
                $("#target").after(function () {
                    return "<p>after the other paragraph" + "</p>";
                });
            });
            $("#before").click(function () {
                $("#target").before(function () {
                    return "<p>before the other paragraph" + "</p>";
                });
            });
        });
    </script>
</head>
<body>
<div id="contain" style="border: 1px red solid;padding: 5px">
    <div id="target" style="border: 1px blue solid;padding: 5px">This is target div</div>
</div>
<button id="append">append</button>
<button id="prepend">prepend</button>
<button id="after">after</button>
<button id="before">before</button>
</body>
</html>
```

* `append` will add the element **in** the end of selector.
* `prepend` will add the element **in** the head of selector.
* `after` will add the element out of selector(**outside**).
* `before` will add the element out of selector(**outside**)