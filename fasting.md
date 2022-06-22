---
title: fasting
description: cycle
---

<script type="text/javascript">

function calculateTimeElapsed(starttime){
  const total = Date.parse(new Date()) - Date.parse(starttime);
  const seconds = Math.floor( (total/1000) % 60 );
  const minutes = Math.floor( (total/1000/60) % 60 );
  const hours = Math.floor( (total/(1000*60*60)) % 24 );
  const years = Math.floor( total/(1000*60*60*24) / 365);
  const days = Math.floor( total/(1000*60*60*24) ) - (years * 365);

  return {
    total,
    years,
    days,
    hours,
    minutes,
    seconds
  };
}
  
function calculateTimeRemaining(endtime){
  const total = Date.parse(endtime) - Date.parse(new Date());
  const seconds = Math.floor( (total/1000) % 60 );
  const minutes = Math.floor( (total/1000/60) % 60 );
  const hours = Math.floor( (total/(1000*60*60)) % 24 );
  const years = Math.floor( total/(1000*60*60*24) / 365);
  const days = Math.floor( total/(1000*60*60*24) ) - (years * 365);

  return {
    total,
    years,
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
      'years: ' + t.years + '<br/>' +
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
      'years: ' + t.years + '<br/>' +
      'days: ' + t.days + '<br/>' +
      'hours: '+ t.hours + '<br/>' +
      'minutes: ' + t.minutes + '<br/>' +
      'seconds: ' + t.seconds + '<br/>';
    if (t.total <= 0) {
      clearInterval(timeinterval);
    }
  },1000);
}

initializeClockElapsed('fastingElapsedDisplay','Tue Jun 21 2022 17:30:00 GMT-0500');
initializeClockRemaining('fastingRemainingDisplay','Fri Jun 24 2022 17:30:00 GMT-0500');

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
  
💯💚🌿
