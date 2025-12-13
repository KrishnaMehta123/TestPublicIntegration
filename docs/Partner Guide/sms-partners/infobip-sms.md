---
title: Infobip
excerpt: SMS Provider
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
[Infobip SMS](https://www.infobip.com/) is a global communication platform that enables businesses to send and receive SMS messages, facilitating personalized and timely customer interactions. When integrated with CleverTap, this allows businesses to manage SMS campaigns seamlessly alongside other marketing channels. The integration enables personalized messaging based on user behavior, tracks performance metrics such as delivery and engagement rates, and automates workflows for timely communications. This combination enhances customer engagement and helps optimize marketing strategies through targeted SMS outreach.

> 📘 Note
>
> Infobip is an SMS Direct Partner.

# Prerequisites

Before setting up the Infobip integration on the CleverTap dashboard, ensure you have the following accounts ready.

* **Infobip account**: You will need an active Infobip account to access their SMS services and obtain the necessary API credentials.
* **CleverTap account**: An active CleverTap account is required to manage your user engagement and to configure the integration with Infobip for SMS communications.

# Set Up Infobip on CleverTap Dashboard

To successfully integrate Infobip with CleverTap, follow the steps below to configure your SMS settings and ensure seamless communication between the two platforms.

1. Go to *Settings > Channels > SMS > SMS Direct* and click **+ Add Provider**

<Image alt="SMS Provider - Infobip" align="center" border={true} src="https://files.readme.io/5dbb8ec41b13cf6f4f34da902d7908703fc5414637cc6f7b794270d32834bfbd-Infobip_2.png">
  SMS Provider - Infobip
</Image>

2. Add the following details: 

<Image alt="Provider Configuration - Infobip" align="center" border={true} src="https://files.readme.io/763ec968d74887d0527930829be1f4080684a7932cf681ba162c4e0f2247ce2e-image_43.png">
  Provider Configuration - Infobip
</Image>

* ###### **Provider**:
  Select CleverTap Infobip from the drop-down menu.
* ###### **Nickname**
  A customizable label for your Infobip SMS integration. This name helps you easily identify and manage the integration within the CleverTap dashboard, making it convenient to distinguish between multiple configurations.
* ###### **Sender ID**
  The identifier that recipients see as the sender of your SMS messages. This can either be a name or a number linked to your brand, helping build recognition and trust with your audience. Depending on your region, this identifier may be provided by Infobip or your telecom partner, and it’s the information that users will see when they receive the message.
* ###### **Base API URL**

  The primary endpoint for Infobip's SMS API. You can find it by navigating to *login > Developer Tools > Base API URL* in your Infobip account. Copy this URL and paste it into the CleverTap dashboard to ensure proper integration and functionality for sending and managing SMS messages. For more information, refer to the\
  [Infobip documentation](https://www.infobip.com/docs/essentials/api-essentials/base-url).

  <Image alt="API Base URL" align="center" border={true} src="https://files.readme.io/3557c6a28a862787b37a6971ec25037e53de8ec77d7eba9dbb12a70ba2dd3635-infobip_api_base_url.png">
    API Base URL
  </Image>
* ###### **API Key**
  A unique identifier used to authenticate your requests to Infobip's SMS API. You can find your [API key](https://www.infobip.com/docs/essentials/api-essentials/api-authorization) by navigating to *login > Developer Tools > API Key* in your Infobip account. Copy this key and paste it into the CleverTap dashboard to enable secure communication between the two platforms.\ <br />

<Image alt="API Key - Infobip" align="center" width="70% " border={true} src="https://files.readme.io/a058cc2a58601c28c887c170d12e4d642a48f2522d504526e35d24448f64837b-image_26.png">
  API Key - Infobip
</Image>

* **Regional Settings**: This field allows you to configure specific settings based on the region in which you are operating. 
  * **India**: If you select India, you must enter the **Principal Entity ID**. This ID can be found in the DLT portal for India and is required to comply with local regulations governing SMS communications.
  * **Turkey**: For Turkey, you need to enter the **Brand Code** and select either **BIREYCEL** or **TACIR**, which are the authorized sender identifiers for your SMS messages in that region. 
* **Inbound Message Callback URL**: The Inbound Message Callback URL is an endpoint where Infobip sends incoming SMS messages, such as replies from recipients. This URL is necessary for handling two-way communication, allowing your system to process and respond to user replies. You can find the URL by navigating to *Numbers > SMS > Inbound Configuration* in your Infobip account and configuring the Callback URL under the phone number's advanced settings. 

  <Image alt="Inbound Message Callback URL - Infobip dashboard" align="center" border={true} src="https://files.readme.io/4af8cb8ecb3a54ffef469a53cc285bd9887be59dcf773bd7191cc16a04742f7f-image_38.png">
    Inbound Message Callback URL - Infobip 
  </Image>

  > 📘 Note
  >
  > Ensure that the **MO JSON 2** option is selected, as it is mandatory for proper integration. This format is required to ensure that incoming messages are correctly processed by CleverTap.

  <br />

  <Image align="center" className="border" border={true} src="https://files.readme.io/b9a493f95578fd66d4986a3741916d44d204424acfe34a4252537356ff0e078b-image_41.png" />

  <br />
* **Delivery Report Callback URL**:  The Delivery Report Callback URL is where Infobip sends the delivery status updates for the SMS messages you’ve sent. It provides feedback on whether each message was successfully delivered, failed, or queued, enabling real-time tracking of your SMS campaigns. You can configure this URL in the Delivery Reports section under *SMS > Numbers* on the Infobip dashboard.
* **Enable Provider Click Tracking**: This feature allows you to track clicks on links within your SMS messages, providing insights into user engagement. 

  * **Default Domain**: If selected, this option uses Infobip's default domain for link tracking. It automatically generates trackable links for the SMS messages sent through the Infobip platform.
  * **Custom Domain**: This option allows you to use your own domain for link tracking, ensuring your SMS messages reflect your brand while still enabling you to track user interactions. Configure and verify your [custom domain ](https://www.infobip.com/docs/url-shortening/register-custom-domain)on the Infobip dashboard to get started. Once verified, you can use it within CleverTap to send your campaigns. 

  <Image alt="URL Shortener for Custom Domain - Infobip" align="center" border={true} src="https://files.readme.io/c04cf9f269db8733c458e8cc5bf4a4bad431bc2ef106ad81bdd278360d9a2d79-image_28.png">
    URL Shortener for Custom Domain - Infobip
  </Image>
* **Set Infobip as Default Service Provider**: By enabling this option, you designate Infobip as your primary service provider for sending SMS messages. This setting ensures that all outgoing SMS campaigns are routed through Infobip by default.

3. Select **Save** and then **Send test SMS** to verify that the integration is functioning correctly. This step ensures that your settings are accurate and messages are delivered as intended.
