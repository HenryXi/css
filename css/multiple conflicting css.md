# Multiple conflicting CSS
When add multiple CSS to the same element which one will work? These CSS code may be in same CSS file, but
for the most case they are not. The question is which one will work? I found the answer [here](https://www.w3.org/TR/selectors/#specificity)
When browser parse the CSS it calculates the selector's specificity. Browser will make high selector
  "override" the low selector. 

**calculate the selector's specificity**

The value of a selector's specificity can be obtained by adding three parts(a, b, and c). Different 
selector belong different part.
 
* ID selector -> a
* class selectors, attributes selectors, and pseudo-classes -> b
* type selectors and pseudo-elements -> c

value = a * 100 + b * 10 + c 

If you can't remember the rules there are some pictures [here](http://cssspecificity.com/) can help you.

**Examples**

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>specificity</title>
    <style type="text/css">
        * {
            background-color: red /* a=0 b=0 c=0, value = 0 */
        }

        input {
            background-color: blue/* a=0 b=0 c=1, value = 1 */
        }

        .test[type=button] {
            background-color: green/* a=0 b=1+1 c=0, value = 20 */
        }

        #target {
            background-color: yellow/* a=1 b=0 c=0, value = 100 */
        }

        .test {
            background-color: brown/* a=0 b=1 c=0, value = 10 */
        }

        #div #target {
            background-color: orange/* a=2 b=0 c=0, value=200 */
        }
    </style>
</head>
<body>
<div id="div">
    <input id="target" type="button" class="test" value="test specificity"/>
</div>
</body>
</html>
```
You can save the code above as specificity.html, and open it in browser to see which css work. For example only use
``#target`` and ``.test[type=button]`` to see which one will work. In this way you can verify the specificity rules.