Carrier Code Lookup
======
> Look up a mobile number's carrier.

There is a $0.005 charge to look up a mobile number's carrier code.

### HTTP Method - `GET`

### URL
```
http://mosms.sumotext.com/secure/sumoLookup.aspx?
```
### Parameters
Param | Description
--- | --- 
`mobile` | Number to send MT to. 
`shortcode` | Short code used.

### Responses
Response | Description
--- | --- 
`IP NOT REGISTERED` | IP address not registered.
`ERROR CARRIER NOT FOUND FOR: {mobile}` | The carrier information for this number could not be found.


