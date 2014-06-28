Receiving an MO
=======

> Receive post data when your shortcode/key gets a text.

The SUMOTEXT platform can be configured to forward 'some' or 'all' mobile originated (MO) messages directly to the client. When a mobile originated (MO) text message is received by the SUMOTEXT System, it can be posted as an HTTP Get to a webpage you have registered in our system.

> Read about adding a postback URL [here](https://github.com/SUMOTEXT/Sumotext-API-Guide/blob/master/api-docs/receiving-post-data.md#add-a-postback-url).

### HTTP Method - `GET`
### URL
```
http://www.yourserver.com/your-endpoint
```

### Parameters
Param | Description
--- | --- 
`mobile` | Mobile number SMS originated from. 
`carrierId` | Carrier code for Mobile Number.
`shortcode` | Short code used.
`key` | Keyword, may be specific or default.
`country` | Country SMS originated from.

##Example
After the [postback URL](https://github.com/SUMOTEXT/Sumotext-API-Guide/blob/master/api-docs/receiving-post-data.md#add-a-postback-url) is pointed to a web server, this is the `GET` request querystring parameters that Sumotext will post to the server.
```
{ 
	mobile : '5015551234',
	carrierId : 'ATTUS',
   	shortcode : '74700',
   	key : 'TEST',
   	country : 'USA'
}
<<<<<<< HEAD
```
=======
````
>>>>>>> 39935be3adfbba28819d93d90efa9698fb956df9
