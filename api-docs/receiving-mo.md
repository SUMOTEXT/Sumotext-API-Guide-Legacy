Receiving an MO
=======

> Receive post data when your shortcode/key gets a text.

The SUMOTEXT platform can be configured to forward 'some' or 'all' mobile originated (MO) messages directly to the client. When a mobile originated (MO) text message is received by the SUMOTEXT System, it can be posted as an HTTP Get to a webpage you have registered in our system. 

### Parameters
Markdown | Less
--- | --- 
`mobile` | Mobile number SMS originated from. 
`carrier` | Carrier code for Mobile Number.
`smsid` | Unique SMS Identifier.
`shortcode` | Short code used.
`key` | Keyword, may be specific or default.