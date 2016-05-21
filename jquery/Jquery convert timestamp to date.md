# Javascript timestamp to date format
It is easy to use ``SimpleDateFormat `` format date in Java. There is no method in Javascript to format
date directly. When we want format date in javascript we have to use Date method to get Day, Month, 
Year and combine them together manually.
```javascript
var timestamp = 1463568871;
var date = new Date(timestamp * 1000);
var day = date.getDate();
var month = date.getMonth() + 1;
var year = date.getFullYear();
var formatted = year + "-" + month + "-" + day ;
alert(formatted);
```
Use timestamp in milliseconds to create ``Date`` in Javascript. Use ``getDate()`` to get day in month.
Use ``getMonth()`` to get month in year. But 0 means January, 1 means February and so on. When we get
month we need add 1. Use ``getFullYear`` to get the year. After getting them you can format the date as
 you like.