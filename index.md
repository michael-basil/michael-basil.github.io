---
title: board
---

<script type="text/javascript">

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

function initializeClock(clockId, deadline, detail) {
  const timeinterval = setInterval(() => {
    const clockElement = document.getElementById(clockId);
    const t = calculateTimeRemaining(deadline);
    if (detail) {
      clockElement.innerHTML = 
        'years: ' + t.years + '<br/>' +
        'days: ' + t.days + '<br/>' +
        'hours: '+ t.hours + '<br/>' +
        'minutes: ' + t.minutes + '<br/>' +
        'seconds: ' + t.seconds + '<br/>';
    } else {
      clockElement.innerHTML = 
        'years: ' + t.years + '<br/>' +
        'days: ' + t.days + '<br/>';
    }
    if (t.total <= 0) {
      clearInterval(timeinterval);
    }
  },1000);
}

initializeClock('teacheringDisplay','2022-03-12',true);     
initializeClock('refinanceDisplay','2022-04-28',true);
initializeClock('maintenanceDisplay','2026-01-31',true);
initializeClock('lifeInsuranceMaintenanceDisplay','2027-08-01',false);
initializeClock('childSupportJackDisplay','2032-07-23',false);
initializeClock('childSupportLilaDisplay','2036-02-07',false);
initializeClock('lifeInsuranceSupportDisplay','2041-05-2',false);

</script>

## backlog
  
* Katie:
  * Nothing at this time.
* Michael:
  * All things considered.
  
## teachering

<span id="teacheringDisplay">
years:<br/>
days:<br/>
hours:<br/>
minutes:<br/>
seconds:<br/>
</span>

## refinance

<span id="refinanceDisplay">
years:<br/>
days:<br/>
hours:<br/>
minutes:<br/>
seconds:<br/>
</span>

## maintenance

<span id="maintenanceDisplay">
years:<br/>
days:<br/>
hours:<br/>
minutes:<br/>
seconds:<br/>
</span>

## life insurance - maintenance

<span id="lifeInsuranceMaintenanceDisplay">
years:<br/>
days:<br/>
</span>

## child support - jack

<span id="childSupportJackDisplay">
years:<br/>
days:<br/>
</span>

## child support - lila

<span id="childSupportLilaDisplay">
years:<br/>
days:<br/>
</span>

## life insurance - support

<span id="lifeInsuranceSupportDisplay">
years:<br/>
days:<br/>
</span>
