Managing Groups
=====

The client can manage their groups through the Sumotext API. Groups can be managed with the following actions

Action | Description
----- | -----
`add` | Add a new group (named `{group}`) to a keyword
`delete` | Delete a group and its members
`clear` | Clear a group of its members
`addmember` | Add a member (member corresponds to their `{mobile}`)

### URL
<pre class="code"><code>http://mosms.sumotext.com/secure/sumoGroup.aspx?</code></pre>

#### Request Parameters
Params | Description
----|----
`country` | Country associated with shortcode
`shortcode` | Short code being used
`key` | Keyword being used
`group` | Name of the group to manage
`action` | Add, delete, clear, or adddmember
`mobile` | Mobile number of subscriber to add to group [Optional: may be left blank]

### Sample Request

<pre class="code"><code>GET /secure/sumoGroup.aspx?<span>country</span>=USA&<span>shortcode</span>=74700&<span>key</span>=SOMEKEY&<span>group</span>=group1&<span>action</span>=addmember&<span>mobile</span>=5015551234 HTTP/1.0
Host: mosms.sumotext.com
</code></pre>


### Sample Response
<pre class="code"><code>HTTP/1.1 200 OK
Content-Type: text/html; charset=utf-8

Action Addmember OK
</code></pre>

### Response Fields
The response data comes as a string 
<pre class="code"><code>Action {action} OK</code></pre>

###Error Response
If there is an error, the response contains an error description message after a colon.
<pre class="code"><code>Action {action} Error: [Error Description]</code></pre>
