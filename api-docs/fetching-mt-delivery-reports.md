Fetching MT Delivery Reports
========
> Check the status of a sent SMS.

You may receive a delivery report for an MT that was sent through the Sumotext API.

### HTTP Method - `GET`

### URL
```
https://mosms.sumotext.com/secure/sumoReport.aspx?
```

#### Request Parameters
Param | Description
--- | --- 
`smsid` | Unique smsid returned when sending the MT.
`shortcode` | Short code used.

#### Response Type - `string`
#### Response Format - `{smsid}:{sent-status}:{true/false message}`
where `sent-status` is either `TRUE` or `FALSE`, and the `true/false message` corresponds to one of the messages listed below.

### Example

*Call*
```
curl --data "smsid=4CD3A94F-B462-44CD-9710-E220F244F82E&shortcode=74700" https://mosms.sumotext.com/secure/sumoReport.aspx?
```
*Response*
```
4CD3A94F-B462-44CD-9710-E220F244F82E:TRUE:Sent by SUMOTEXT to Aggregator
```

#### Error Responses
Response | Description
--- | --- 
`{smsid}:TRUE:[True Message]` | Message successfully sent.
`{smsid}:FALSE:[False Message]` | Message failed to deliver. See "Not Sent Messages" for list of error messages.
`{smsid}:NOTFOUND:[single space char]` | The smsid is not in the system.

#####True Messages
* Sent by Sumotext to Aggregator.
* Message successfully delivered to handset.
* Message successfully sent to carrier.

#####False Messages
* Failed. We are unable to delier this message.
* Not Delivered, Billing failed, Billing.
* Not Delivered, Invalid destination, Destination permanent.
* Not Delivered, Invalid source address, Source.
* Not Delivered, No Information, No information.
* Not Delivered, System failure, System failure.
* EXPIRED: We are unable to deliver this message.
* FAIL: We are unable to deliver this message.
* FAILED: We were unable to send this to aggregator.
* UNDELIV: We are unable to deliver this message.
