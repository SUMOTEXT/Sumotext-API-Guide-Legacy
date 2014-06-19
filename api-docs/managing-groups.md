Managing Groups
=====
> Manage subscribers and groups.

The client can manage their groups through the Sumotext API. A client can clear a group of its members, delete a group and its members, add a group to a keyword, and add a member to a group.

### HTTP Method - `GET`

### URL
```
http://mosms.sumotext.com/secure/sumoGroup.aspx?
```

#### Request Parameters
Params | Description
----|----
`country` | Country associated with shortcode
`shortcode` | Short code being used
`key` | Keyword being used
`group` | Name of the group to manage
`action` | Add, delete, clear, or adddmember
`mobile` | Mobile number of subscriber to add to group [Optional: may be left blank]

#### Response Type - `string`
#### Response Format - `Action {action} OK`
#### Error Responses
Response | Description
--- | --- 
`Action Add OK` | Successfully added.
`NOTIP` | IP adress making the API call not registered with Sumotext.
`Action Add Error: [Error Descrioption]` | Error performing the action on the group.

