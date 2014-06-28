Carrier Code Lookup
======
> Look up a mobile number's carrier.

There is a $0.005 charge to look up a mobile number's carrier code.

####Carrier Codes
View [Appendix A](https://github.com/SUMOTEXT/Sumotext-API-Guide/blob/master/api-docs/appendices/appendix-a.md) for a list of all carrier codes.

### HTTP Method - `GET`

### Example URL
```
http://mosms.sumotext.com/secure/sumoLookup.aspx?mobile=5015551234&shortcode=74700
```
#### Request Parameters
Param | Description
--- | --- 
`mobile` | Number to send MT to. 
`shortcode` | Short code used.

####Response Type - `string`
####Successful Response  - `{carrier_code}`
Response | Example | Description
--- | --- | ---
`{carrier_code}` | ATTUS | Carrier code for the mobile number's carrier.

#### Error Responses
Response | Description
--- | --- 
`IP NOT REGISTERED` | IP address not registered.
`ERROR CARRIER NOT FOUND FOR: {mobile}` | The carrier information for this number could not be found.


