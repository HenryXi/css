# Javascript switch case example
`switch...case` is useful and easy to use in Javascript. I will show you how to use `switch...case` in Javascript.
Examples are here.
```javascript
var month='';
 switch (new Date().getMonth()) {
     case 0:
         month = "January";
         break;
     case 1:
         month = "February";
         break;
     case 2:
         month = "March";
         break;
     case 3:
         month = "April";
         break;
     case 4:
         month = "May";
         break;
     case 5:
         month = "June";
         break;
     case 6:
         month = "July";
         break;
     case 7:
         month = "August";
         break;
     case 8:
         month = "September";
         break;
     case 9:
         month = "October";
         break;
     case 10:
         month = "November";
         break;
     case 11:
         month = "December";
         break;
     default:
         month = "not found";
         break;
 }
 alert(month);
```
Don't forget `break` keyword.