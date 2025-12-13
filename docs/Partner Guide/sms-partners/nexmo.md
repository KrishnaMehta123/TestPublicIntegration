---
title: Nexmo/Voynage
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
CleverTap supports sending SMS through Nexmo. 

Sign up with Nexmo and then follow the steps below in the CleverTap Dashboard for successful integration.

# Integration Steps

- In the CleverTap Dashboard, navigate to Settings and click on Integrate SMS.
- Select Nexmo.
- In the API Key text box, fill in your API key from the Nexmo Dashboard.
- In the API Secret text box, fill in the API secret value from the Nexmo Dashboard.
- In the From Number text box, fill in either a Nexmo phone number, or a Shortcode.

You can enter phone numbers or short codes listed under the Nexmo dashboard → Numbers → Your Numbers.

> 📘 Encoding
> 
> CleverTap automatically detects if unicode characters are present in the SMS sent using Nexmo and encodes them using UTF-8. However, if no unicode characters are found in the message, it automatically switches to GSM-7 encoding. For more information about character set supported by Nexmo within each encoding, refer to the [Nexmo article](https://api.support.vonage.com/hc/en-us/articles/5587876190492-What-encoding-standards-does-Vonage-support-).