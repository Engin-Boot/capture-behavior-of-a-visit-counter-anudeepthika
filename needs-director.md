# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given There is an entry card issued for patient
  
  When a patient enters the hospital
  And if there is an issue of new card or old card with validity
  
  Then increment number of visits by 1
  And report the total visitor count on working days and holidays separately to director

Scenario: Compute parking slots to reserve for visiting specialists

  Given there are visiting specialists
  
  When there are parking slots available
  
  
  Then update the number and report to the director
