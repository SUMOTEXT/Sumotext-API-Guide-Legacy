Sending a Mobile Terminated (MT) Message
========

>Send an SMS to a mobile number.

In order to use the SUMOTEXT API to send an MT, your server‘s IP Address must be registered in the SUMOTEXT API Database and tied to a specific account and dedicated short code.
All clients can send messages from inside our online campaign management tools.
However, if you have a dedicated short code, you are free to send messages from your own internal system via this API.

When you want to send an MT text message from your own system, SUMOTEXT will provide a dedicated HTTPS URL. Use HTTP GET with 5 query string parameters. Parameter names are case sensitive and all lower case.

### HTTP Method - `GET`

### Example URL
```
https://mosms.sumotext.com/secure/sumoSend.aspx?mobile=5015551234&carrier=ATTUS&shortcode=74700&key=SUMO&msg=hello
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
#### Successful Response

Response | Example | Description
--- | --- | ---
`{mobile}:{smsid}` | 2125551212:ACAEEBE7-DFC3-4837-8E49-AAEB04D6E9E0 | SUCCESS: Returns Unique SMSID.

#### Error Responses
Response | Example | Description
--- | --- | ---
`{mobile}:NOTIP` | 2125551212:NOTIP | IP address not registered.
`{mobile}:NOTOPT` | 2125551212:NOTOPT | Mobile number is in the system, but the subscriber is not opted into the Keyword. 
`{mobile}:NOTFOUND` | 2125551212:NOTFOUND | Mobile Number is either not in the sysem or not in the Keyword.

