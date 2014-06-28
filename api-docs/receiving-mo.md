Receiving a Mobile Originated (MO) Message
=======

The SUMOTEXT online self-service campaign management tools are typically used to configure what happens when a user sends a text message to your short code.
However, our platform and tools can be bypassed and your dedicated short code can be configured to instead forward 'some' or 'all' mobile originated (MO) messages directly to your server for you to respond based on your own business rules, logic, and data sources.

NOTE: This is different from the section that deals with 'CRM API CALLBACK' which is used to alert your service when the SUMOTEXT platform has collected an opt-in, opt-out, or a new profile element for a subscriber such as an email address.

 If you would like to bypass our platform and tools and receive 'some' or 'all' mobile originated (MO) messages directly to your server, please provide your account manager the the appropriate URL to register in our system. This can be HTTP or HTTPS. We strongly reccomend HTTPS.


### HTTP Method - `GET`
### URL
```
https://www.yourserver.com/your-endpoint
```

### Parameters
Param | Description
--- | --- 
`mobile` | Mobile number SMS originated from. 
`carrier` | Carrier code for Mobile Number.
`smsid` | Unique SMS identifier
`shortcode` | Short code used.
`key` | The keyword where the message is logged.
`msg` | Complete message sent.

##Example

The post will be a fully formed URL with 6 query string parameters:
<pre>
https://www.yourserver.com/your-endpoint?mobile=2125551212&carrier=VERIZONUS&smsid=2xgh679okl34x&shortcode=84700&key=SUMOX&msg=have a nice day
</pre>