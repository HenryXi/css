# Multiple conflicting CSS
When add multiple CSS to one element which one will work? These CSS code may be in same CSS file, but
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

**Examples**

```
* {
    color:red
}
a=0 b=0 c=0 
value = 0

div {
    color:blue
}
a=0 b=0 c=1
value = 1

#button {
    color:yellow
}
a=1 b=0 c=0
value = 100

.test[type=button]{
    color:green
}
a=0 b=1+1 c=0
value = 20

.test{
    color:grey
}
```