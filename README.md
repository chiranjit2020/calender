# Calender UI
 Calender and Current Time using Vanilla JavaScript
```javascript
 //Get the Year, Month, Day, Day Name
 const lang = navigator.language;
 let date = new Date();

 let dayNumber = date.getDate();
 let month = date.getMonth();
 let datName = date.toLocaleString(lang, {weekday: 'long'});
 let monthName = date.toLocaleString(lang, {month: 'long'});
 let year = date.getFullYear();

 document.getElementById("monthName").innerText = monthName;
 document.getElementById("dayName").innerText = datName;
 document.getElementById("dayNumber").innerText = dayNumber;
 document.getElementById("year").innerText = year;
 
 //Current Time
 function clock(){
  let hr = new Date().getHours();
  let min = new Date().getMinutes();
  let sec = new Date().getSeconds();

  hr = (hr < 10) ? `0${hr}` : hr;
  min = (min < 10) ? `0${min}` : min;
  sec = (sec < 10) ? `0${sec}` : sec;

  document.getElementById("hour").innerText = hr;
  document.getElementById("minute").innerText = min;
  document.getElementById("second").innerText = sec;
 }
 setInterval(clock, 1000);
```
