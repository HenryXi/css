# JQuery loop array example
In this page I will show you how to loop an array by using JQuery and Javascript. I recommend using JQuery to 
loop an array. Examples are here.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Jquery loop array example</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.3/jquery.min.js"></script>
    <script type="text/javascript">
        var targetStr = '1,2,3,4,5,6,7';
        var array = targetStr.split(',');
        //use JQuery
        $.each(array, function (index, item) {
            alert('index:' + index + ', item:' + item);
        });


        //use forEach in Javascript
        array.forEach(function (item, index) {
            alert('index:' + index + ', item:' + item);
        });

        //generic way in Javascript
        for (i = 0; i < array.length; i++) {
            alert('index:' + i + ', item:' + array[i]);
        }
    </script>
</head>
<body>
</body>
</html>
```
`forEach` method is not support by all browsers. I recommend using Jquery or generic way in Javascript.