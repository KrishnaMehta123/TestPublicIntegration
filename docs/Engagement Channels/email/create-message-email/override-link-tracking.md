---
title: Override Link Tracking
excerpt: Learn how to override redirection of Email links to the CleverTap server.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
To track clicks on email links, CleverTap redirects the links of your email body, first to a CleverTap server and then back to your landing page.

If you want to avoid click tracking through CleverTap, set the following tag in your email body:

```html
<a data-track="off" href="donotoverrride"> Your link </a>
```

Setting this tag will ensure that CleverTap does not redirect the links that you have specified in your email body.

> 🚧 Click Tracking
>
> If you set this tag, CleverTap will be unable to track clicks on your email message.
