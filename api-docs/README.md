Sumotext API Guide
=====

> Use the Sumotext HTTPS API to integrate Sumotext events with your service.

###Overview
For developers who prefer to automate their mobile messaging programs from internal data sources and event triggers, we support API-only accounts with reliable, high throughput connectivity to our SMS, MMS, Coupon, and Mobile Wallet Gateways.

###Finding your credentials
Contact SUMOTEXT at 1-800-480-1248 to set up your account. Customers are provided a dedicated support matrix for their account. Our U.S. based help desk is available weekdays from 8:00 AM to 6:30 PM CST.
For after hours emergency support 24/7/365, please call 501-313-3318.

###Security
We use a combination of HTTPS, IP Address white-listing, and dedicated shortcode/keyword. Please contact your account manager for assistance with initial configuration.

###Receiving Post Data (API Callbacks)
The Sumotext platform can be configured to send your web server an http request when certain events are triggered (see [Receiving Post Data](receiving-post-data.md)), or when you [receive an MO](receiving-mo.md). Follow the directions below to tell Sumotext where to point the HTTP calls:

1. Log in at [sumotext.com](sumotext.com).
2. Go to the Settings tab.
3. Go to the Web Form settings tab.
4. Click “Edit Post CRM”.
5. Check the “Post” checkbox.
6. Configure the Post parameters that Sumotext will POST

###Table of Contents

1. [Receiving an MO](receiving-mo.md)
2. [Sending an MT](sending-mt.md)
3. [Carrier Code Lookup](carrier-code-lookup.md)
4. [Fetching MT Delivery Reports](fetching-mt-delivery-reports.md)
5. [Custom Web Form](custom-web-form.md)
6. [CRM API Callback](receiving-post-data.md)
7. [Managing Groups](managing-groups.md)