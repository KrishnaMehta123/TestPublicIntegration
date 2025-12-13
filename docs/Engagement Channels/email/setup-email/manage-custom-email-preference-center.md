---
title: Manage Custom Email Preference Center
excerpt: >-
  Allow users to customize the communication preference and host a subscription
  management page using CleverTap's Email Preference Center feature.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

CleverTap's Email Preference Center feature allows you to customize user communication preferences. It also provides a ready-to-use preference management page, or you can create a custom Preference Center, empowering users to control their communication experience. This ensures they stay engaged with the content that matters most to them. Subscription groups allow users to select the content they want to receive, reducing unsubscription rates and fostering strong brand-user relationships. This approach enhances user satisfaction and builds a more personalized connection with your audience.

> 📘 Private Beta
> 
> Currently, this feature is released in Private Beta. If you want access to this feature, contact your Customer Success Manager.

# Create Your Custom Email Preference Center

You can modify CleverTap's default Email Preference Center and easily create a custom Email Preference Center using HTML, CSS, and JavaScript. It allows you to: 

- Design a personalized subscription page tailored to your audience's preferences.
- Instantly preview the content and refine your design.
- Effortlessly integrate your custom Email Preference Center into your email campaigns.

To create your custom Email Preference Center: 

1. Go to _Settings_ > _Channel_ > _Email_ > _Advanced Setup_. 
2. Expand the _Email Preference Center_ section and click **+ Preference Center**. The _New Preference Center_ page opens with the [CleverTap Preference Center](doc:manage-email-preferences) code pre-populated.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f663053-Click__Email_Preference_Center.png",
        null,
        "Create Custom Preference Center"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Custom Preference Center"
    }
  ]
}
[/block]


The _New Preference Center_ page opens with the [CleverTap Preference Center](doc:manage-email-preferences) default HTML code pre-populated. This HTML includes the following CleverTap JavaScript (JS) code:

```javascript India
// Copy and paste the below code snippet inside the <head></head> section of your landing page

<script type="text/javascript">
     var clevertap = {event:[], profile:[],region : 'in1', account:[], onUserLogin:[], notifications:[]};
 // replace with the CLEVERTAP_ACCOUNT_ID with the actual ACCOUNT ID value from your Dashboard -> Settings page
 clevertap.account.push({"id": "CLEVERTAP_ACCOUNT_ID"});
 (function () {
		 var wzrk = document.createElement('script');
		 wzrk.type = 'text/javascript';
		 wzrk.async = true;
     wzrk.src = 'https://d2r1yp2w7bby2u.cloudfront.net/js/clevertap.min.js';		 
     var s = document.getElementsByTagName('script')[0];
		 s.parentNode.insertBefore(wzrk, s);
  })();
</script>
```
```javascript Singapore
<script type="text/javascript">
     var clevertap = {event:[], profile:[], region : 'sg1', account:[], onUserLogin:[], notifications:[],privacy:[]};
 clevertap.account.push({"id": "CLEVERTAP_ACCOUNT_ID"});
 (function () {
 var wzrk = document.createElement('script');
 wzrk.type = 'text/javascript';
 wzrk.async = true;
 wzrk.src = 'https://d2r1yp2w7bby2u.cloudfront.net/js/clevertap.min.js'; 
 var s = document.getElementsByTagName('script')[0];
 s.parentNode.insertBefore(wzrk, s);
  })();
</script>
```
```javascript United States
<script type="text/javascript">
     var clevertap = {event:[], profile:[], region : 'us1', account:[], onUserLogin:[], notifications:[], privacy:[]};
 clevertap.account.push({"id": "CLEVERTAP_ACCOUNT_ID"});
 (function () {
 var wzrk = document.createElement('script');
 wzrk.type = 'text/javascript';
 wzrk.async = true;
 wzrk.src = 'https://d2r1yp2w7bby2u.cloudfront.net/js/clevertap.min.js'; 
 var s = document.getElementsByTagName('script')[0];
 s.parentNode.insertBefore(wzrk, s);
  })();
</script>
```
```javascript Indonesia
<script type="text/javascript">
     var clevertap = {event:[], profile:[], region : 'aps3', account:[], onUserLogin:[], notifications:[], privacy:[]};
 clevertap.account.push({"id": "CLEVERTAP_ACCOUNT_ID"});
 (function () {
 var wzrk = document.createElement('script');
 wzrk.type = 'text/javascript';
 wzrk.async = true;
 wzrk.src = 'https://d2r1yp2w7bby2u.cloudfront.net/js/clevertap.min.js'; 
 var s = document.getElementsByTagName('script')[0];
 s.parentNode.insertBefore(wzrk, s);
  })();
</script>
```
```javascript Middle East (UAE)
<script type="text/javascript">
     var clevertap = {event:[], profile:[], region : 'mec1', account:[], onUserLogin:[], notifications:[], privacy:[]};
 clevertap.account.push({"id": "CLEVERTAP_ACCOUNT_ID"});
 (function () {
 var wzrk = document.createElement('script');
 wzrk.type = 'text/javascript';
 wzrk.async = true;
 wzrk.src = 'https://d2r1yp2w7bby2u.cloudfront.net/js/clevertap.min.js'; 
 var s = document.getElementsByTagName('script')[0];
 s.parentNode.insertBefore(wzrk, s);
  })();
</script>
```
```javascript Europe (default region)
<script type="text/javascript">
       var clevertap = {event:[], profile:[], region : 'eu1', account:[], onUserLogin:[], notifications:[], privacy:[]};
 clevertap.account.push({"id": "CLEVERTAP_ACCOUNT_ID"});
 (function () {
 var wzrk = document.createElement('script');
 wzrk.type = 'text/javascript';
 wzrk.async = true;
 wzrk.src = 'https://d2r1yp2w7bby2u.cloudfront.net/js/clevertap.min.js'; 
 var s = document.getElementsByTagName('script')[0];
 s.parentNode.insertBefore(wzrk, s);
  })();
</script>
```

3. Replace the `region` value in the `clevertap` object with the correct region for your CleverTap account. To identify the region of your CleverTap account, refer to the following table:

| Region                  | CleverTap Dashboard URL                             |
| :---------------------- | :-------------------------------------------------- |
| India                   | <https://in1.dashboard.clevertap.com/login.html#/>  |
| Singapore               | <https://sg1.dashboard.clevertap.com/login.html#/>  |
| United States           | <https://us1.dashboard.clevertap.com/login.html#/>  |
| Indonesia               | <https://aps3.dashboard.clevertap.com/login.html#/> |
| Middle East (UAE)       | <https://mec1.dashboard.clevertap.com/login.html#/> |
| Europe (default region) | <https://eu1.dashboard.clevertap.com/login.html#/>  |

3. Replace the default code with your custom code for unsubscribing in the editor on the left side of the _New preference center_ window. The right side of the window displays a preview of your subscription page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f2dab58-Add_Code_for_Custom_Preference.png",
        null,
        "Add Code for Custom Preference Center"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Code for Custom Preference Center"
    }
  ]
}
[/block]


The CleverTap JS code provided above is essential to be able to use different methods for listing user's subscription groups, unsubscribing them, and so on. The following are some of CleverTap's functions that you can leverage when creating your custom preference center:

- `$WZRK_WR.getEmail(false, withGroups)`  
  Fetch data such as the user's email address, subscription groups, campaign ID, and identity.
- `$WZRK_WR.setSubscriptionGroups(subscriptionGroups)`  
  Once you get subscription groups via `$WZRK_WR.getEmail` method, you can use it to perform different operations, such as updating, retrieving, and displaying the user's subscription preferences.
- `$WZRK_WR.getSubscriptionGroups()`  
  Retrieves the current subscription groups associated with a user's profile on the CleverTap dashboard.

> 📘 Note
> 
> You must call the `$WZRK_WR.setSubscriptionGroups(subscriptionGroups)` method before calling this method.

- `$WZRK_WR.changeSubscriptionGroups(false, unsubcribeGroups)`  
  Triggered when the user updates their subscription preferences. It sends this updated subscription information to CleverTap.
- `$WZRK_WR.isGlobalUnsubscribe()`  
  Determines if the page is for unsubscribing from campaign-specific groups or for displaying the Email Preference Center.

The following is a sample code for creating a preference center:

```javascript
// Copy and paste the below code snippet inside the <head></head> section of your landing page

<script type="text/javascript">
     var clevertap = {event:[], profile:[],region : 'in1', account:[], onUserLogin:[], notifications:[]};
 // replace with the CLEVERTAP_ACCOUNT_ID with the actual ACCOUNT ID value from your Dashboard -> Settings page
 clevertap.account.push({"id": "CLEVERTAP_ACCOUNT_ID"});
 (function () {
		 var wzrk = document.createElement('script');
		 wzrk.type = 'text/javascript';
		 wzrk.async = true;
     wzrk.src = 'https://d2r1yp2w7bby2u.cloudfront.net/js/clevertap.min.js';		 
     var s = document.getElementsByTagName('script')[0];
		 s.parentNode.insertBefore(wzrk, s);
  })();
</script>
<style>
 .row {
   display: flex;
   align-items: center;
 }

 .manage-preferences {
   color: rgba(18, 107, 255, 1);
   text-decoration: none;
   text-wrap: nowrap;
 }

 .manage-preferences:hover {
   cursor: pointer;
 }

 .switch {
   position: relative;
   display: inline-block;
   width: 90px;
   height: 40px;
 }

 .slider span {
   display: inline-block;
   width: 50%;
   padding: 10px 5px 0 10px;
   color: black;
   font-size: 15px
 }

 .slider {
   display: flex;
   position: absolute;
   cursor: pointer;
   top: 0;
   left: 0;
   right: 0;
   bottom: 0;
   border-radius: 8px;
   -webkit-transition: .4s;
   transition: .4s;
   z-index: 1;
 }

 .slider:before {
   position: absolute;
   content: "";
   height: 40px;
   width: 45px;
   z-index: -1;
   background-color: rgba(241, 242, 245, 1);
 }

 input:checked+.slider {
   background-color: rgba(18, 107, 255, 1);
 }

 input+.slider {
   background-color: rgba(18, 107, 255, 1);
 }

 input[type="checkbox"]:not(:checked)+.slider:before {
   border-top-right-radius: 8px;
   border-bottom-right-radius: 8px;
   -webkit-transform: translateX(45px);
   -ms-transform: translateX(45px);
   transform: translateX(45px);
   color: black;
 }
 }
</style>
<div id="handle-group-unsubscribe">
 <!-- To show Group Unsubscribe page to user-->
 <div>
   <h2>Unsubscribe from the following types of emails?</h2>
 </div>
 <div id="unsubscribe-groups"></div>
 <!-- All the campaign level subscription groups will be added dynamically here -->
 <div id="sample-unsubscribe-groups">
   <!-- Sample group added for reference-->
   <p>Newsletter</p>
   <p>Product Updates</p>
 </div>
 <p>
   <span>To unsubscribe from all emails or receive only certain types of emails,</span>
   <a class="manage-preferences" onclick="managePreferenceLink()">Manage Email Preferences.</a>
 </p>
 <div>
   <button onclick="changeSubscriptionGroups()">Unsubscribe</button>
 </div>
</div>
<div id="handle-global-unsubscribe" style="display: none">
 <!-- To show global Unsubscribe page to user -->
 <div>
   <h2>Manage Email Preferences</h2>
   <p> Choose the emails you would like to receive from us. </p>
 </div>
 <hr />
 <div id="unsubscribe-global-groups"></div>
 <!-- All the subscription groups will be added dynamically here -->
 <div id="sample-global-unsubscribe-groups">
   <!-- Sample group added for reference -->
   <div class="row">
     <p>Newsletter</p>
     <label class="switch">
       <input type="checkbox">
       <div class="slider">
         <span class="no">NO</span>
         <span class="yes">YES</span>
       </div>
     </label>
   </div>
   <div class="row">
     <p>Product Updates</p>
     <label class="switch">
       <input type="checkbox">
       <div class="slider">
         <span class="no">NO</span>
         <span class="yes">YES</span>
       </div>
     </label>
   </div>
 </div>
 <div>
   <p>You will continue to receive non-promotional emails. For example - Privacy policy and Outage updates.</p>
 </div>
 <div>
   <button onclick="changeSubscriptionGroups()">Save Preferences</button>
 </div>
</div>
<div id="action-btns" style="display: none">
 <!-- If require to unsubscribe/resubscribe from all use below buttons -->
 <p>Unsubscribe from all future emails</p>
 <button onclick="unsubscribeAll()">Unsubscribe All</button>
 <p>Resubscribe to all email groups</p>
 <button onclick="resubscribeAll()">Resubscribe All</button>
</div>
<div id="unsubscribe-operation-failed-message" style="display: none;">
 <h2 id="error-message"></h2>
 <div>
   <ol>
     <li>Check your internet connection</li>
     <li>Disable ad-blockers if enabled</li>
     <li>Enable Javascript on your browser, if disabled</li>
   </ol>
   <p> If the issue persists, contact Customer Care </p>
 </div>
</div>
<!-- Added Manage Preference link for demo purpose Actually logic is added below in the other script -->
<script>
 function managePreferenceLink() {
   document.querySelector("#handle-global-unsubscribe").style.display = 'block';
   document.querySelector("#handle-group-unsubscribe").style.display = 'none';
 }
</script>
<script>
 var isReEncode = false window.onload = function() {
  const withGroups = true $WZRK_WR.getEmail(false, withGroups); // Fetch data such as the user's email address, subscription groups, campaign ID, and identity. } 
  function wzrk_email_fetched(emailStr, profile) {
   if (!profile || !profile.groups || profile.groups.length === 0) {
    console.log("did not recv groups in callback");
   }
   const subscriptionGroups = profile.groups; // extract subscription groups $WZRK_WR.setSubscriptionGroups(subscriptionGroups); $WZRK_WR.setUpdatedCategoryLong(profile); const divElement = document.createElement('DIV'); const campaignIdElement = document.createElement('SPAN'); campaignIdElement.innerHTML = "campaignid: " + profile.campaignId // extract campaignId divElement.appendChild(campaignIdElement); const identityElement = document.createElement('SPAN'); identityElement.innerHTML = "identity: " + profile.identity // extract identity divElement.appendChild(identityElement); const emailElement = document.createElement('SPAN'); emailElement.innerHTML = "email: " + emailStr // display email address divElement.appendChild(emailElement); const groupList = document.getElementById('handle-global-unsubscribe') groupList.append(divElement) displayGroups();//Sample function to display the subscription group details } function displayGroups() { const subscriptionGroups = $WZRK_WR.getSubscriptionGroups(); // Retrieves the current subscription groups associated with a user's profile const isGlobalUnsubscribe = $WZRK_WR.isGlobalUnsubscribe() // Determines if the page is for unsubscribing from campaign-speicifc groups or for displaying the Email Preference Center const managePreferencesElement = document.querySelector('.manage-preferences') if (!isGlobalUnsubscribe) { managePreferencesElement.href = getManagePreferenceLink() document.querySelector("#handle-global-unsubscribe").style.display = 'none'; document.querySelector("#handle-group-unsubscribe").style.display = 'block'; document.querySelector("#sample-unsubscribe-groups").style.display = 'none'; const groupList = document.getElementById('unsubscribe-groups') for (let obj of subscriptionGroups) { const groupNameElement = document.createElement("P"); groupNameElement.name = obj.name // extract name of subscription group groupNameElement.description = obj.description // extract description of subscription group groupNameElement.checked = false groupNameElement.innerHTML = obj.name; groupList.appendChild(groupNameElement) } } else { document.querySelector("#handle-global-unsubscribe").style.display = 'block'; document.querySelector("#handle-group-unsubscribe").style.display = 'none'; document.querySelector("#sample-global-unsubscribe-groups").style.display = 'none'; const addList = document.getElementById('unsubscribe-global-groups'); for (let obj of subscriptionGroups) { const groupContainerElement = document.createElement("DIV"); const groupNameElement = document.createElement("P"); const checkBox = document.createElement("INPUT"); const isUnsubscribed = obj.isUnsubscribed // extract subscription status of subscription group checkBox.setAttribute("type", "checkbox"); groupContainerElement.setAttribute("class", "unsubscribe-group-info") checkBox.checked = !isUnsubscribed checkBox.setAttribute("name", obj.name) checkBox.setAttribute("id", obj.name) checkBox.setAttribute("class", "ct-unsub-group-input-item"); const label = document.createElement("LABEL"); label.appendChild(checkBox); label.appendChild(getSliderElement()); label.setAttribute("class", "switch"); groupNameElement.innerHTML = obj.name; groupContainerElement.appendChild(groupNameElement); groupContainerElement.appendChild(label); addList.appendChild(groupContainerElement); addList.appendChild(document.createElement('HR')) } } } function changeSubscriptionGroups() { let unsubcribeGroups = []; const elements = document.getElementsByClassName("ct-unsub-group-input-item"); for (let i = 0;i < elements.length;i++) { const element = elements[i]; if (element.name) { const data = { name: element.name, isUnsubscribed: !element.checked } unsubcribeGroups.push(data) } } $WZRK_WR.changeSubscriptionGroups(false, unsubcribeGroups); //updates group subscription preference of user } function unsubscribeAll() { $WZRK_WR.unSubEmail(isReEncode); //completely unsubscribes user from email communication } function resubscribeAll() { resubscribeCalled = true $WZRK_WR.subEmail(isReEncode); //resubscribes user for email communication } function getManagePreferenceLink() { const searchParams = new URLSearchParams(window.location.search); searchParams.set("page_type", "global"); return window.location.pathname + '?' + searchParams.toString(); } function hideUnsubscribeOptions () { document.querySelector('#handle-global-unsubscribe').style.display = 'none'; document.querySelector('#handle-group-unsubscribe').style.display = 'none'; document.querySelector('#action-btns').style.display = 'none'; } function wzrk_email_subscription (status) { alert("Successful") } function wzrk_email_fetched_failed (error) { hideUnsubscribeOptions() document.querySelector('#unsubscribe-operation-failed-message').style.display = 'block'; const errorMsg = 'We could not retrieve your email address'; document.querySelector('#error-message').innerHTML = errorMsg; } function wzrk_email_subscription_failed (error) { hideUnsubscribeOptions() document.querySelector('#unsubscribe-operation-failed-message').style.display = 'block'; const errorMsg = 'Failed to save your preferences'; document.querySelector('#error-message').innerHTML = errorMsg; }  
</script>
```

4. Click **Save**.  The **Save Preference Center** dialog box appears. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a86d262-Save_Preference_Center.png",
        null,
        "Save Custom Preference Center"
      ],
      "align": "center",
      "border": true,
      "caption": "Save Custom Preference Center"
    }
  ]
}
[/block]


5. Enter the name of the preference center and click **Save**. The newly created custom email preference center is displayed under the _Email Preference Center_ page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dad40ae-Unpublished_Preference_Center.png",
        null,
        "Unpublished Preference Center"
      ],
      "align": "center",
      "border": true,
      "caption": "Unpublished Email Preference Center"
    }
  ]
}
[/block]


When you save a custom email preference center, it is initially set to an **Unpublished** state. You must publish it to activate it. Once published, it is available in the _Email Preference Center_ dropdown when [configuring the email provider](doc:manage-email-preferences#configure-email-preference-center). 

> 📘 Key Points to Remember
> 
> - You can create only one custom Preference Center page per account.
> - After setting the Email Preference Center to a custom preference center from the _Provider Setup_, the new custom preference center is now visible for scheduled campaigns and will be used for future recurring campaign runs.

# Manage Your Custom Email Preference Center

You can perform different actions on a custom preference center. To manage the custom email preference center: 

1. Go to _Settings_ > _Channel_ > _Email_ > _Advanced Setup_.
2. From the Email Preference Center page, click the  ![](https://files.readme.io/f870ff6-Ellipses.png) icon beside the custom email preference center. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3515281-Manage_Custom_Preference_Center.png",
        null,
        "Manage Custom Email Preference Center"
      ],
      "align": "center",
      "border": true,
      "caption": "Manage Custom Email Preference Center"
    }
  ]
}
[/block]


3. Perform one of the following actions: 
   - **Preview**: Allows you to preview the appearance and functionality of the custom preference center.
   - **Publish**: Allows you to use the custom preference page when setting up the email provider. 
   - **Edit**: Allows you to modify the content and layout of the custom page. When you edit an unpublished custom preference center, you need to save it and then publish it from the _Email Preference Center_. The changes are saved and published when you edit an already published customer preference center.  
     <br />
     > 📘 Edit Published Custom Preference Center
     > 
     > If you edit an already published custom preference center, the modifications reflect in the already sent campaigns, too.