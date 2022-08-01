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

initializeClockElapsed('fastingElapsedDisplay','Mon Aug 01 2022 19:00:00 GMT-0500');
initializeClockRemaining('fastingRemainingDisplay','Wed Aug 3 2022 13:00:00 GMT-0500');

</script>

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


## log
  
* 2022/06/21 - Tue - 17:30 - 50 hours
* 2022/07/27 - Mon - 17:00 - 48 hours
* 2022/07/10 - Sun - 17:00 - 73 hours
* 2022/07/17 - Sun - 18:30 - 40 hours
* 2022/07/24 - Sun - 17:00 - 70 hours
* 2022/07/27 - Wed - 17:00 - 42 hours 
  
💯💚🌿
