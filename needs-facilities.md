# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given the sensor is working and each day count is stored
  
  When there is a new visitor in that particular day
  
  Then update the count 
  And report the visitor count trend to the manager during a week of operation 

Scenario: Alert when seating capacity is full

  Given there is seating availability and visitors
  
  When there is someone waiting without a seat
  
  Then report to facilities manager "seating is full"
