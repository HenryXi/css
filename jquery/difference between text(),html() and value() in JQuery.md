# Difference between text() html() and val() in JQuery
Do not know which to use when you want set or change the content of selector in JQuery? I will show you the difference
between `text()`, `html()` and `val()` in this page. Example is here, copy it and save as html file. Click different button
will change different selector's content.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Difference between text() html() val() in JQuery</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
    <script>
        $(document).ready(function(){
            $("#setText").click(function(){
                $("#text").text("new text");
            });
            $("#setHTML").click(function(){
                $("#html").html("<b>new html</b>");
            });
            $("#setValue").click(function(){
                $("#val").val("new value");
            });
        });
    </script>
</head>
<body>

<p id="text">old text</p>
<p id="html">old html</p>

<p>Input: <input type="text" id="val" value="old value"></p>

<button id="setText">Set new Text</button>
<button id="setHTML">Set new HTML</button>
<button id="setValue">Set new Value</button>

</body>
</html>
```
* `text()` method will change the text of selector. This method can not add html style to the selector.
* `html()` method will change the html of selector. You can add html style in the selector(add `<b>` in above example)
* `val()` method will change the value of "value" property. We often use it to change value of `input`.