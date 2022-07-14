---
title: fasting
description: cycle
---

<script type="text/javascript">

function calculateTimeElapsed(starttime){
  var total = Date.parse(new Date()) - Date.parse(starttime);

  if (total <= 0) {
    total = 0;
  }

  const seconds = Math.floor( (total/1000) % 60 );
  const minutes = Math.floor( (total/1000/60) % 60 );
  const hours = Math.floor( (total/(1000*60*60)) % 24 );
  const days = Math.floor( total/(1000*60*60*24) );

  return {
    total,
    days,
    hours,
    minutes,
    seconds
  };
}
  
function calculateTimeRemaining(endtime){
  var total = Date.parse(endtime) - Date.parse(new Date());

  if (total <= 0) {
    total = 0;
  }

  const seconds = Math.floor( (total/1000) % 60 );
  const minutes = Math.floor( (total/1000/60) % 60 );
  const hours = Math.floor( (total/(1000*60*60)) % 24 );
  const days = Math.floor( total/(1000*60*60*24) );

  return {
    total,
    days,
    hours,
    minutes,
    seconds
  };
}

function initializeClockElapsed(clockId, starttime) {
  const timeinterval = setInterval(() => {
    const clockElement = document.getElementById(clockId);
    const t = calculateTimeElapsed(starttime);
    clockElement.innerHTML = 
      'days: ' + t.days + '<br/>' +
      'hours: '+ t.hours + '<br/>' +
      'minutes: ' + t.minutes + '<br/>' +
      'seconds: ' + t.seconds + '<br/>';
    if (t.total <= 0) {
      clearInterval(timeinterval);
    }
  },1000);
}
  
function initializeClockRemaining(clockId, endtime) {
  const timeinterval = setInterval(() => {
    const clockElement = document.getElementById(clockId);
    const t = calculateTimeRemaining(endtime);
    clockElement.innerHTML = 
      'days: ' + t.days + '<br/>' +
      'hours: '+ t.hours + '<br/>' +
      'minutes: ' + t.minutes + '<br/>' +
      'seconds: ' + t.seconds + '<br/>';
    if (t.total <= 0) {
      clearInterval(timeinterval);
    }
  },1000);
}

initializeClockElapsed('fastingElapsedDisplay','Sun Jul 17 2022 17:00:00 GMT-0500');
//initializeClockRemaining('fastingRemainingDisplay','Wed Jul 20 2022 17:00:00 GMT-0500');

</script>

## log
  
* 50 hours
    * Tue Jun 21 2022 17:30:00 GMT-0500
    * Thu Jun 23 2022 19:30:00 GMT-0500
* 48 hours
    * Mon Jun 27 2022 17:00:00 GMT-0500
    * Wed Jun 29 2022 17:00:00 GMT-0500
* 73 hours
    * Sun Jul 10 2022 17:00:00 GMT-0500
    * Wed Jul 13 2022 17:00:00 GMT-0500
  
## elapsed

<span id="fastingElapsedDisplay">
days:<br/>
hours:<br/>
minutes:<br/>
seconds:<br/>
</span>
  
## remaining

<span id="fastingRemainingDisplay">
days:<br/>
hours:<br/>
minutes:<br/>
seconds:<br/>
</span>
  
💯💚🌿
