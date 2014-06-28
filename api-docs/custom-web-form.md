Custom Web Form
========
> Initiate an opt-in from your own web form.

You can give a user the option of opting-in through a web-form. Set up the HTML form however you like, and configure it to perform the following HTTP call when submitted. The user must at least provide their mobile number. You may also request additional profile data from the user in this form, and send that information in your HTTP request.

### HTTP Method - `GET`

### URL
```
http://mosms.sumotext.com/mOptinMO.aspx?country=USA&shortcode=69872&key=SUMO&phone=5012474110&txt1=??&txt2=??&txt3=??&txt4=??&txt5=??&txt6=??&txt7=??&txt8=??txt9=??&txt10=??&txt11=??
```

### Parameters
Param | Description
--- | --- 
`shortcode` | Short code used.
`key` | Should reflect the keyword being used.
`phone` | The mobile number opting in.
`txt1` | Profile data field that matches the web form in the Sumotext online tools.
`txt2-txt11` | Up to 11 form fields for profile data. Fields not used should be left blank.




