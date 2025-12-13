---
title: CleverTap Product Release Notes
fullscreen: false
hidden: true
metadata:
  title: ''
  description: ''
---
Welcome to CleverTap's release notes. Release Notes are published every month so that you can stay abreast of the following (for the previous month):

# December 2022

### Enhancement ![Enhancement](https://files.readme.io/143b08f-Enhancement.png)

**Project Activity Dashboard v1**\
Empowering you with a new adoption and usage tracking dashboard to:

* Help measure how your team is doing.
* Get a holistic view of all the channels you use to reach your users, and get recommendations.
* Know about unused features, configurations, and add-ons, and get recommendations.

> 📘 Note
>
> This enhancement is for CleverTap for Startup customers only.

**New Webhooks Enhancement**

* Deliver both the system and custom user properties to your endpoint.
* Update your CRMs and dashboard with a holistic overview of your users and make informed decisions quickly and effortlessly.

<Image title="image (10).png" alt={2878} className="border" border={true} src="https://files.readme.io/eb9a087-image_10.png" />

> 📘 Note
>
> This feature is available only on the new campaign interface for all customers.

For more information, refer to the [Create a Webhook](https://docs.clevertap.com/docs/create-message-webhook).

**CleverTap and AppsFlyer Deep Linking Integration**\
With this integration: 

* Define AppsFlyer deep links in the dashboard. Streamline and provide a seamless email-to-app experience to your users. 
* Create contextual and personalized journeys to your app, measure campaign performance, and increase conversions.

<Image title="CT+ AF Integration.png" alt={3840} className="border" border={true} src="https://files.readme.io/e176de9-CT_AF_Integration.png" />

For more information, refer to the [AppsFlyer Onelink](https://docs.clevertap.com/docs/setup-email#appsflyer-onelink).

### New Feature ![New Feature](https://files.readme.io/ed7f117-New_Feature.png)

**No-code Web Native Display Campaigns with Ready-to-use Templates**

* We have released two new out-of-the-box templates—Banner and Banner with text. These templates help you to utilize visually appealing banners with personalized text to create highly contextual content for your website visitors.
* Get started with Web Native campaigns with zero code efforts, as CleverTap manages content delivery at the right moment and location on your website.

<Image title="image (1).png" alt={720} className="border" border={true} src="https://files.readme.io/78b26cc-image_1.png" />

For more information, refer to the [Web Native Display](https://developer.clevertap.com/docs/web-native-display) and [Web Native Display Templates](https://docs.clevertap.com/docs/web-native-display-create-message#web-native-display-templates) documentation.

**Super Fast Campaign Reports**

* Select up to 2000 campaigns and the lightning-fast reporting, taking a minimum of 10 mins.
* Reduce the reporting time by 800%, and select 20x the number of campaigns. Reduce manual effort considerably and increase your operational efficiency.
* Automatically export these reports to your partner cloud platforms, such as Amazon S3 or GCP, and enjoy error-free campaign reports ingestion.

For more information, refer to [Campaign Reports](https://docs.clevertap.com/docs/campaign-reports).

# November 2022

### New Feature ![New Feature](https://files.readme.io/ed7f117-New_Feature.png)

**RenderMax - Groundbreaking Push Notification Render Rate Technology by CleverTap**

* Engage your users with RenderMax and boost push notification render rates up to 90%.
* Power up the render rates of your push notifications, amplify the push notification reach, and maximizes user engagement with RenderMax. This is specifically true for devices in battery-saver mode or cannot be reached due to inactivity.

For more information, refer to the [RenderMax](https://docs.clevertap.com/docs/rendermax) and this [CleverTap RenderMax](https://clevertap.com/rendermax/).

**Supercharging Engagement for WhatsApp Campaigns with Enhanced Experimentation and Optimization**\
The WhatsApp channel on CleverTap is now powered with additional capabilities around experimentation and optimization, giving you the ability to:

* Experiment A/B and multivariate testing to compare up to three message versions with different templates, copies, creative calls to action, or any combination, to identify what works best.
* Utilize Split Delivery to decide what percentage of the audience gets a message variant and compare campaign stats to identify the winning variant.
* Create Multi-variant Campaigns optimized for location, demographics, purchase trends, and more. Boost engagement and conversion with up to 50 variants of the same message based on a user property type.

> 📘 Note
>
> These enhancements are available for all CleverTap WhatsApp customers in the new campaigns experience.

For more information, you can refer to the [WhatsApp Message Type](https://docs.clevertap.com/docs/create-message-whatsapp#whatsapp-message-types).

### Update ![Update](https://files.readme.io/ebebea5-Update.png)

**Push Amplification renamed to Pull Notifications**\
The Push Amplification feature is now Pull Notifications. The new name truly reflects the functioning and benefit of this feature because it pulls the pending notifications from the CleverTap server and successfully delivers them to mobile devices.

> 📘 Note
>
> Campaign reports column names *AmplifiedByPush* and *AmplifiedByInbox* have not been changed to maintain the continuity of running jobs at your end.

**Direct Access for Leanplum Customers**\
Leanplum customers now have read-only access to users for the current CleverTap Demo accounts with the Direct Access feature. This is a time-limited feature.

<HTMLBlock>{`
<section class="content-toc grid-25"><nav><ul class="toc-list"><li><a class="tocHeader" href="#" target="_self"><i class="icon icon-text-align-left"></i>Table of Contents</a></li><li class="toc-children"><ul>
<li>
<a href="#2022-q3" target="_self">2022 (Q3)</a>
<ul>
<li><a href="#november" target="_self">November</a></li>
</ul>
</li>
</ul>
  </li>
  </ul>
  </nav>
</section>

<style>
.content-toc {
    padding-bottom: 30px;
    padding-top: 30px;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    -webkit-box-flex: 0;
    -ms-flex: 0 0 var(--hub-toc-width);
    flex: 0 0 var(--hub-toc-width);
    padding-left: 0px;
    padding-right: 20px;
}
.content-toc {
    position: sticky;
    top: 0;
    max-height: 100vh;
    overflow: auto;
    display: block;
    float: none!important;
    font-size: 13px;
}
  .content-toc ul {
    list-style: none;
    padding-left: 0px;
    margin: 0;
}
  .field-description a[href], .field-description a:not([href=""]), .markdown-body a[href], .markdown-body a:not([href=""]) {
    text-decoration: underline;
}
 .content-toc .toc-list>li:not(.toc-children) :first-child {
    position: sticky;
    top: 0;
    z-index: 2;
    background: var(--color-bg-page);
    padding-left: 0px;
    pointer-events: none;
}
  .content-toc .toc-list>li:not(.toc-children) :first-child>i:first-child {
    text-align: center;
}    
  .hub-container, #content-container {
    max-width: var(--container,1140px);
    margin: 0px 350px 0px 250px;
}
</style>
`}</HTMLBlock>
