---
title: parenting
description: compass
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

initializeClock('maintenanceDisplay','2026-01-31',true);
initializeClock('lifeInsuranceMaintenanceDisplay','2027-08-01',false);
initializeClock('childSupportJackDisplay','2032-07-23',false);
initializeClock('childSupportLilaDisplay','2036-02-07',false);
initializeClock('lifeInsuranceSupportDisplay','2041-05-2',false);

</script>

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
  
## decisions
  
### education
  
Significant decisions regarding the children’s education, including, but not limited to, choice of school, tutors, course of study and classes, and individualized educational programs, shall all be decided by Mother, after consultation with Father.  The parents further agree that Mother shall continue to manage all administrative tasks and responsibilities associated with the children’s school enrollment and involvement.  The parties agree to enroll the children in the public school from Kindergarten through 12th grade, if possible, unless the parties agree otherwise.  The parents may arrange appointments for parent-teacher conferences at independent times from the other parent.  Each parent shall also have independent access to the children’s records and shall have the right to communicate directly with any teachers and administrators regarding the children.
  
### health
  
Significant decisions regarding the children’s health, including, but not limited to, significant decisions relating to the physical, mental and dental health needs of the children and to the treatments arising or resulting from those needs shall require consultation between the parties.  “Significant” health decisions include choice of health care providers, and non-routine or extraordinary treatment.   The parties agree to consult one another regarding any significant health decisions for the children, attending mediation as soon as practicable if needed, consistent with the terms of this Agreement, to attempt to reach an agreement on the course of treatment.   Whatever is ultimately and jointly agreed, both parties will fully cooperate to carry out the selected treatment.   The parents agree to fully disclose and maintain the children’s current healthcare providers, and Mother shall manage the scheduling and other administrative tasks associated with routine health care.  New health care providers, particularly in specialized areas where there is no existing provider or current patient relationship, shall be selected by agreement, and after consultation, as outlined above, when necessary.  The parents shall advise each other fully of any serious illness or injury suffered by the children as soon as possible after learning of the same, including the name and phone numbers of attending healthcare providers.  All healthcare providers involved in the children’s care and treatment shall be directed to give both parties all information regarding said illness or injury immediately.  In cases of emergency, where time does not permit consultation with the other party, the party with physical possession of the children shall take whatever emergency action is necessary to meet the children’s emergency health care or other emergency needs - the one exception to this is that neither party will admit or agree to have children admitted for mental health hospitalization without the explicit and expressed written consent of the other party via email or text message.  If needed, the parties will make arrangements to take time off of work to directly monitor a situation while agreeable mental health care becomes available.  As soon as practicable in an emergency situation, the party shall advise the other party of the facts, circumstances, decision and condition of the children via phone, email, or text message and initiating subsequent consultation when needed thereafter.  For any therapeutic treatment of the children or family, both parents shall participate and attend the children's/family therapy to the extent the therapist recommends.
  
### religion
 
Significant decisions regarding the children’s religion/politics/philosophy, including, but not limited to, choice of denomination or party, schooling, training, or participation in customs or practices shall all be guided by the parties jointly.  It is self-evident that the children will ultimately decide their faith and any religious/political/philosophical affiliation of their own free will when they are legal adults however they so choose.
  
### extracurriculars
  
Significant decisions regarding the children’s extracurricular and recreational activities shall all be decided by both parents jointly, subject to the following terms:

1. Extracurricular and recreational activities shall be defined as activities (in and outside of school), sports, lessons, and camps (day and overnight) during the school year and summer months. 
1. In regard to any new extracurricular or recreational activity, enrollment shall require both parties’ agreement, but the parents shall defer to the minor children’s wishes when picking new activities.  Neither party will unreasonably withhold their consent for a new activity and shall consider and defer to the minor children’s wishes when picking new activities. 
1. Both parties shall be entitled to receive any and all information and shall have the right to attend and participate in any and all of the children’s extracurricular and recreational activities, both inside and outside of school.  The parents may also attend practices if parents are invited to the same. 
1. Both parents shall transport the children to their extracurricular and recreational activities and ensure that the children attend the same during their respective parenting times.   
1. The parents may arrange appointments for parent-coach conferences at independent times from the other parent.  Each parent shall also have independent access to the children’s records and shall have the right to communicate directly with any coaches and administrators regarding the children.

## rights

### mother

1. Default: overnights Sunday through Thursday
1. Summer Break: overnights for up to two weekend blocks
    * Friday through Sunday
    * Not to conflict with child birthdays or Father's Day
    * Optional at Mother's discretion
1. Winter Break: overnights split in half
    * First choice if desired
1. Spring Break: overnights split in half
    * First choice deferred to Father
1. Holiday Weekends: overnights for the weekend 
    * Limited to Easter, St. Patricks Day and Mother's Day
    * Friday through Sunday
    * Optional at Mother's discretion
1. Right of first refusal when Father unable to care for the children
    * Applies in situations of four or more hours
  
### father
  
1. Default: overnights on Friday and Saturday
1. Summer Break: overnights for up to two weekday blocks
    * Sunday through Thursday
    * Not to conflict with child birthdays
    * Optional at Father's discretion
1. Winter Break: overnights split in half 
    * First choice deferred to Mother
1. Spring Break: overnights split in half
    * First choice if desired
1. Holiday Weekends: overnights extending the weekend 
    * Limited to Labor Day and Memorial Day
    * Sunday and Monday
    * Optional at Father's discretion
1. Right of first refusal when Mother unable to care for the children
    * Applies in situations of four or more hours

## expectations

1. Birthday Celebration: Mother, Father, and the children have a shared outing including a meal
    * Invitation of children's friends and child relatives to be considered for the outing
1. Parenting Handoffs: each parent drops off the children to the other parent
    * Inclimate Weather: Mother will facilitate transporation bi-directionally by automobile
    * Pandemic Lockdown: Mother will facilitate transporation bi-directionally by automobile
1. Travel excursions within the United States: inform the other parent ahead of time
1. Travel excursions outside the United States: requires agreement prior to departure
1. Video Calls: the children are able to initiate video calls to the other parent and family
    * Respectful of digital device time and other constraints
    * Within reason to not interfere with plans, events, or other parental considerations
1. Children's Belongings: clothes, shoes, toys, travel machines, and the like are theirs
    * Transportation of such items will be through the use of a child-packed backpack
    * Larger item logistical considerations by agreement between the parents
  
## designations
  
1. Mother shall be designated as the custodian of the the children when legally required
    * This will in no way affect rights and expectations denoted above
1. The cildren will each maintain the surname of BASIL
    * No other surname or hyphenated name shall be used anywhere
  
💯💚🌿
