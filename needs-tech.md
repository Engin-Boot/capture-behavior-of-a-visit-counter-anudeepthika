# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given the sensor is working and server contains visitor count
  
  When there is restart of server
  
  Then recover the data to avoid data loss

Scenario: Reconcile counts if the sensor is offline for a while
  
  Given updating the count is possible in the server
  When sensor is offline
  
  When the sensor is offline and there are new visitors
  
  Then update the count in the server.
