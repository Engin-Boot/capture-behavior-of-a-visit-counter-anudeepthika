# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given the sensor is working and restart the count everyday in a week
  
  When there is a new visitor in that particular day
  
  Then update the count
  And report the visitor count trend to the manager during a week of operation
  
Scenario: Alert when seating capacity is full

  Given there is current seating availablity and maximum seating number
  
  When there is someone waiting without a seat
  Or there is minimum seating availability
  
  Then report to facilities manager "seating capacity is full"
