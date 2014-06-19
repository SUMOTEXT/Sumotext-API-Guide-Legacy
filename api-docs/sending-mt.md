Sending an MT
========
>Send an SMS to a mobile number.

### HTTP Method - `GET`

### URL
```
https://mosms.sumotext.com/secure/sumoSend.aspx?
```

#### Request Parameters
Param | Description
--- | --- 
`mobile` | Number to send MT to. 
`carrier` | Carrier code for Mobile Number.
`shortcode` | Short code used.
`key` | Keyword, may be specific or default.
`msg` | Message to be sent.

#### Response type - `string`
#### Response format - `{mobile}:{smsid}

### Example

*Call*
```
curl --data "mobile=5015555555&carrier=VERIZONUS&shortcode=84700&key=SUMO&msg=have a nice day" https://mosms.sumotext.com/secure/sumoSend.aspx?
```
*Response*
```
5015555555:7A2D2AF7-6851-4D22-BD41-BD8EE94C061E
```

### Responses
Response | Description
--- | --- 
`{mobile}:NOTIP` | IP address not registered.
`{mobile}:NOTOPT` | Mobile number is in the system, but the subscriber is not opted into the Keyword. 
`{mobile}:NOTFOUND` | Mobile Number is either not in the sysem or not in the Keyword.
