---
title: RCS Message Templates
excerpt: Learn more about setting up and creating RCS Messaging Templates
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

RCS (Rich Communication Services) Message Templates enable businesses to send rich, interactive messages to users, enhancing engagement beyond standard SMS capabilities. These templates support various media types, buttons, and formatting options, allowing for a more dynamic user experience.

Here are the key components that make up an RCS message template.

# Template Components

An RCS message template consists of the following key components:  

- **Title**: The headline of the message that appears prominently at the top of the template. It should be concise and engaging to quickly capture the recipient’s attention.  
- **Description**:  The main message body where the content of the RCS message is defined. This field provides detailed information to users and can include formatted text such as bold, italics, strikethrough, and emojis to enhance readability and engagement.
- **Buttons**: Interactive elements that allow users to take action directly from the message. RCS templates support up to four buttons, enabling businesses to drive customer engagement. The number of buttons rendered in an SMS inbox depends on the device's screen dimensions and UI limitations. Some buttons used in the template may not be visible on certain devices due to these constraints. It is recommended to test templates across different devices to ensure optimal rendering. CleverTap allows three types of buttons in RCS Text Templates:
  - [URL Redirect](doc:rcs-message-templates#url-redirect) 
  - [Dialer](doc:rcs-message-templates#dialer)
  - [Quick Reply](doc:rcs-message-templates#quick-reply) 

## URL Redirect

A button that redirects users to a specific webpage. Opens a specific URL when tapped, directing users to a landing page, website, or app.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4ffa1503d189efeaa24de75b27a679fadde093bd49d2e13c86807855347eadf3-URL_Redirect_RCS.png",
        "",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


- **Button Text**: Enter a label for the button (maximum 25 characters, no special characters).  
- **URL Type**: The destination URL. For dynamic URLs, use placeholders (e.g., <https://example.com/{{1}}>). Choose from the following options:  
  - **Static**: Fixed URL entered at the time of template creation.  
  - **Dynamic**: Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. Uses dynamic parameters, for example: <https://www.clevertap.com/{{1}}>.
  - **CleverTap Click Tracking**: Brands can leverage CleverTap click tracking functionality to monitor details of the user who clicked the URL. The entire URL can be personalized for each user during campaign creation.
- **Postback**: A button identifier that can be used to track button clicks. The Notification Replied event logs this interaction for analytics.

### Dialer

Initiates a phone call to a specified number, allowing users to contact a business instantly. Users can tap the button to initiate a phone call. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5fc52b4042d34a8a7203c39a7c959c88bd415614601cd5bd34a8cf98cf5fd9ce-Dialer_RCS.png",
        "",
        "Dialer Button"
      ],
      "align": "center",
      "border": true,
      "caption": "Dialer Button"
    }
  ]
}
[/block]


- **Button Text**: Enter a label for the button (maximum 25 characters, no special characters).
- **Phone number**: The number users will call when they click the button.
- **Postback**: A button identifier that can be used to track button clicks. The Notification Replied event logs this interaction for analytics.

### Quick Reply

A button that allows users to send predefined responses.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4e852c69f86248f2d9bb5cde84118bf8c5715b487bd7a255e56ccecea2a9bd3d-Quick_Reply_-_RCS.png",
        "",
        "Quick Reply Button"
      ],
      "align": "center",
      "border": true,
      "caption": "Quick Reply Button"
    }
  ]
}
[/block]


- **Button Text**: Enter a label for the button (maximum 25 characters, no special characters).
- **Postback**:  A button identifier that can be used to track button clicks. The Notification Replied event logs this interaction for analytics.

# Add Message Template

Easily create and manage RCS message templates in CleverTap to streamline your messaging campaigns. These templates are automatically sent to the relevant platforms based on registration. For example, if a template is registered with Vodafone, it will be sent to Vodafone. The status of the template will be updated within 24 hours, and you can track it directly within the dashboard.  

To create RCS campaigns for Indian users, you must have pre-approved RCS message templates saved in the CleverTap dashboard. Follow the steps below to add a new message template:  

1. Navigate to _Settings_ > _Channels_ > _SMS_ > _SMS Direct_ > _+ Provider_ 

   [block:image]{"images":[{"image":["https://files.readme.io/762fc449942aba1ccfbd894b9456ab9df28f0335b22630cdb0ae3567c18cb545-Set_up_-_RCS.png","","Add Provider"],"align":"center","border":true,"caption":"Add Provider"}]}[/block]
2. In the _Provider Nickname_ select _Infobip RCS Provider_ from the CleverTap dashboard. 

   [block:image]{"images":[{"image":["https://files.readme.io/da895c9dc2960d00a8be756e9dce30b89bb6393821e9f6476cb90a9bd62ce975-Provider_-_RCS.png","","Infobip RCS Provider "],"align":"center","border":true,"caption":"Infobip RCS Provider "}]}[/block]
3. Select the _Templates_ option and click **+ Template**. 

   [block:image]{"images":[{"image":["https://files.readme.io/676c7e96d063f681c29b73d2fb7099a1d651016d3378e54cd69e56c898652c8f-Create_Template_-_RCS.png","","Create Template"],"align":"center","border":true,"caption":"Create Template"}]}[/block]
4. Choose the Template Type:

   - [Text  ](doc:rcs-message-templates#text)
   - [Rich Card](doc:rcs-message-templates#rich-card-template)
   - [Carousel](doc:rcs-message-templates#carousel) 

     [block:image]{"images":[{"image":["https://files.readme.io/41665be20c86c2510f64dbfdd71f72b7609fdc01a610234af1a1d6dcbfee1281-Template_Type_-_RCS.png","","Template Type"],"align":"center","border":true,"caption":"Template Type"}]}[/block]
5. Configure Template Components:
   - **Title**: The headline of the message that appears prominently at the top of the template.
   - **Description**: Enter the main message content.
   - **Buttons**: Add interactive elements to enhance user engagement.
6. Click **Save** to save the template.

## Text

The text template is a simple RCS message format that consists of a plain text message with optional interactive buttons. It allows businesses to send structured messages while incorporating basic text formatting and engagement features. Follow these steps to create a text template:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ffc9ab4e10340484d43a582447d08d899436302cca8afd551a2f562c14ea885-Text_Template_1_-_RCS.png",
        "",
        "Text Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Text Template"
    }
  ]
}
[/block]


1. **Template Name**: Enter a name for the template (maximum 20 characters). 

> 📘 Naming RCS Templates
> 
> Template names and language variants must be unique for each provider configuration. This means that you can use the same template name once for each provider configuration.
> 
> For example, if you have multiple provider configurations, such as _Phone_1, phone_2_, you can use the same template name once within _Phone_1 and Phone_2_.

2. **Message Text**: Enter the text message content (maximum 1000 characters). 
   - **For body text formatting**: 
     - Adding Emojis: Copy from here and paste in the body.
     - Bold: Add asterisks (\*) at the beginning and end.
     - Italic: Add underscores (\_) at the beginning and end.
     - Strikethrough: Add tilde (~) at the beginning and end.
     - Monospace: Add three consecutive backticks (\`\`\`) at the beginning and end.
3. **Enable Buttons**: Toggle _ON_ if you want to include interactive buttons in the message (up to 4 buttons). There are three types of buttons that can be added. 
   - [URL Redirect ](doc:rcs-message-templates#url-redirect)
   - [Dialer ](doc:rcs-message-templates#dialer)
   - [Quick Reply](doc:rcs-message-templates#quick-reply)

## Rich Card Template

A Rich Card Template allow businesses to send RCS messages with images, videos, or other media to enhance engagement.. Rich Cards enhance user engagement by presenting information in an interactive, media-rich format that is more compelling than standard text messages. They are ideal for showcasing products, promotions, event details, and more. Follow the steps below to create a Rich Card template on CleverTap.

1. **Template Name**: Enter a name for the template (maximum 20 characters, only alphanumeric characters and underscores (\_) are allowed.).
2. Choose _Card Size & Layout _ to the layout for how media will be displayed in the message: 

   - Vertical Layout Options 
     - 3:1 Aspect Ratio – A tall vertical card for displaying more prominent visuals.
     - 2:1 Aspect Ratio – A slightly shorter vertical layout, maintaining a balanced visual hierarchy.
   - Horizontal Layout Options (Aspect Ratio: 3:4)

     - Image on Left – The image appears on the left side, with text and buttons on the right.
     - Image on Right – The image appears on the right side, with text and buttons on the left.  
       <br />

     [block:image]{"images":[{"image":["https://files.readme.io/c068cffc0dc6b06ab5d956d6d346d0c84f5c58a5128d19b3ae1a3c1593c3f7fe-Rich_card-_Aspect_ratio_-_RCS.png","","Aspect Ratio"],"align":"center","border":true,"caption":"Aspect Ratio"}]}[/block]
3. To configure card _Content_, select the _Media_ type for your Rich Card:

   - Static: The media file is uploaded at the time of template creation and cannot be changed later. Select between _Image_ or _Video_ and click **Upload Media**.  
     <br />

   [block:image]{"images":[{"image":["https://files.readme.io/94cd36f5583ad458e01b6358af5ceb289cac61bbb4f85cbec0b522620bf139e4-Rich_Card_-_Media_Type_-_Static_-_RCS.png","","Static "],"align":"center","border":true,"caption":"Static "}]}[/block]

   - Dynamic: Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. For example: <https://www.clevertap.com/{{1}}>. Enter Media URL.  
     <br />

   [block:image]{"images":[{"image":["https://files.readme.io/2975d3d6264e8d2585952d472a6e95ea92dc3f20704055a7d258f7aec14ba84e-Rich_card_-_Dynamic_-_RCS.png","","Dynamic"],"align":"center","border":true,"caption":"Dynamic"}]}[/block]

- Upload in Campaign: You upload media during campaign creation, but it cannot be personalized per user. Upload media at the campaign level when sending the RCS message. Since CleverTap will register a URL at the time of template creation to provide the flexibility of uploading media URL at the time of campaign creation, personalization will not be available for the URLs at the time of uploading the media while creating a campaign. A pre-determined URL will already be present in the URL field. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a48183f87aee11573d8b9122d30667cb46351969f06b7b633e25a2cd80c20250-Rich_Card_-_Upload_in_campaign_-_RCS.png",
        "",
        "Upload in Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Upload in Campaign"
    }
  ]
}
[/block]


4. Add a Thumbnail to provide a preview of the media in the Template. Incase of Videos, a thumbnail is mandatory and will be pre-selected automatically and in case of Image, a thumbnail is optional. It can be enabled by checking the _Add Thumbnail_ check box. For Images, thumbnails may not render properly when delivered to SMS inboxes. There are three types of media that can be used for the thumbnail. 
   - Static: A fixed image or video for the thumbnail. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06d8ef2f27e8a371240fe28b66aefd22b935524c81126a8a403eb6c0de078f1f-Static_Thumbnail_-_Rich_Card_-_RCS.png",
        "",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


- Dynamic: Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. For example: <https://www.clevertap.com/{{1}}>. 

  [block:image]{"images":[{"image":["https://files.readme.io/c5c1b525bf4516441ad9cc2b89d39aff60d43d64b848cbdd43c69bb75b5371a7-Dynamic_Thumbnail_-_Rich_Card_-_RCS.png","","Dynamic Thumbnail"],"align":"center","border":true,"caption":"Dynamic Thumbnail"}]}[/block]
- Upload in Campaign: Upload media at the campaign level when sending the RCS message. Since CleverTap will register a URL at the time of template creation to provide the flexibility of uploading media URL at the time of campaign creation, personalization will not be available for the URLs at the time of uploading the media while creating a campaign. 

  [block:image]{"images":[{"image":["https://files.readme.io/42807d723d3349029cc3ae4678feb76c11b2f33935464e334a57d371b1aae2d7-Upload_in_campaign_thumbnail_-_rich_card_-_rcs.png","","Upload in Campaign Thumbnail"],"align":"center","border":true,"caption":"Upload in Campaign Thumbnail"}]}[/block]

5. **Add a Title**: The title will be displayed in bold and can be up to 200 characters long. To add dynamic parameters, use {{1}}, {{2}}, etc., in sequence, where values will be replaced at runtime.
6. **Add a Description**: Enter the text message content, with a maximum limit of 2000 characters. To add dynamic parameters {{1}}, {{2}}, etc., for personalization.

   - **For body text formatting**: 

     - Adding Emojis: Copy from here and paste in the body.
     - Bold: Add asterisks (\*) at the beginning and end.
     - Italic: Add underscores (\_) at the beginning and end.
     - Strikethrough: Add tilde (~) at the beginning and end.
     - Monospace: Add three consecutive backticks (\`\`\`) at the beginning and end. 

       [block:image]{"images":[{"image":["https://files.readme.io/c4c503b881d91b34007c8a7b60afdcc7fe5559bed83eee83d4231e65100da380-Title_and_description_-_rich_card_-_rcs.png","","Title and Description"],"align":"center","border":true,"caption":"Title and Description"}]}[/block]
7. **Enable Buttons**: Toggle _ON_ if you want to include interactive buttons in the message (up to 4 buttons). There are three types of buttons that can be added. 

   - [URL Redirect](doc:rcs-message-templates#url-redirect) 
   - [Dialer](doc:rcs-message-templates#dialer) 
   - [Quick Reply](doc:rcs-message-templates#quick-reply) 

     [block:image]{"images":[{"image":["https://files.readme.io/16d54fdc182ddfe39e741ce075a33929cfdd6ba65c3eee762b9984ef18f34219-Rich_card_-_Buttons_-_RCS.png","","Buttons"],"align":"center","border":true,"caption":"Buttons"}]}[/block]

## Carousel

A Carousel Template is a multi-card format that allows businesses to display multiple Rich Cards within a single message. Users can scroll horizontally through the cards, making it an effective way to showcase multiple products, services, promotions, or event details within a single interaction. Each card in the carousel can contain an image or video, a title, a description, and interactive buttons, enhancing engagement and interactivity.

Follow the steps below to create a Carousel Template on CleverTap. You can add up to 10 cards in the template, with each card containing the following elements: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8f239bb7af6858e373116cf35ac5cdde2dae9558116e108e150d22b1794d7e45-Add_Card_-_Carousel.png",
        "",
        "Add Card in Carousel Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Card in Carousel Template"
    }
  ]
}
[/block]


1. **Template Name**: Enter a name for the template (maximum 20 characters).
2. Choose _Card Size & Layout_ to define the appearance of the Carousel:  

   - Vertical Layout Options  
     - 4:5 Aspect Ratio: A tall vertical card designed for prominent visuals, ideal for highlighting key content.  
     - 5:4 Aspect Ratio: A slightly shorter vertical layout that maintains a balanced visual hierarchy.  

   - Horizontal Layout Options  

     - 2:1 Aspect Ratio: A wide horizontal card designed for expansive visuals, ensuring clear and impactful content display.  
     - 4:3 Aspect Ratio: A slightly more compact horizontal layout that maintains a balanced visual structure. 

       [block:image]{"images":[{"image":["https://files.readme.io/0affb791731557bd5e89feb7611b5a5a89f885272c2a3524de94b7539a5b49ef-Carousel_Template_-_Aspect_Ratio.png","","Aspect Ratio"],"align":"center","border":true,"caption":"Aspect Ratio"}]}[/block]
3. To configure card _Content_, select the _Media_ type for your Carousel Template:

   - Static: A fixed image or video. Select between _Image_ or _Video_ and click **Upload Media**. 

     [block:image]{"images":[{"image":["https://files.readme.io/1f67a27d91e9b708a61ccf148a60b02467c997e25c178de76c66abe011856ec6-Static_-_Carousel_-_RCS.png","","Static"],"align":"center","border":true,"caption":"Static"}]}[/block]
   - Dynamic: Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. For example: <https://www.clevertap.com/{{1}}>. Enter Media URL. 

     [block:image]{"images":[{"image":["https://files.readme.io/4275b6b057c0282ba6d5b37a7772a234c362e63ad8aeade57839b33e94d60019-Dynamic_-_Carousel_-_RCS.png","","Dynamic"],"align":"center","border":true,"caption":"Dynamic"}]}[/block]
   - Upload in Campaign: Upload media at the campaign level when sending the RCS message. Since CleverTap will register a URL at the time of template creation to provide the flexibility of uploading media URL at the time of campaign creation, personalization will not be available for the URLs at the time of uploading the media while creating a campaign. A pre determined URL will already be present in the URL field. 

     [block:image]{"images":[{"image":["https://files.readme.io/cdfc80ee5a5b6073a3f88cbdc54728bf1ef9acf79da55a216bf3c8e072bee99a-Upload_in_campaign_-_Carousel_-_RCS.png","","Upload in Campaign"],"align":"center","border":true,"caption":"Upload in Campaign"}]}[/block]
4. Add a Thumbnail to provide a preview of the media in the Template. Incase of Videos, a thumbnail is mandatory and will be pre-selected automatically and in case of Image, a thumbnail is optional. It can be enabled by checking the _Add Thumbnail_ check box. There are three types of media that can be used for the thumbnail.

   - Static: A fixed image or video for the thumbnail. 

     [block:image]{"images":[{"image":["https://files.readme.io/c28a8fee007176660b9eaa6fd394acbbcd2143c1400cf7d8c6150135f9f718f5-Static_Thumbnail.png","","Static Thumbnail"],"align":"center","border":true,"caption":"Static Thumbnail"}]}[/block]
   - Dynamic: Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. For example: <https://www.clevertap.com/{{1}}>. 

     [block:image]{"images":[{"image":["https://files.readme.io/150728b1fdc13b71e2512e2637a0c75fc176c4d4dbff9e6c69e6a5f743646030-Dynamic_thumbnail_-_rcs.png","","Dynamic Thumbnail"],"align":"center","border":true,"caption":"Dynamic Thumbnail"}]}[/block]
   - Upload in Campaign: Upload media at the campaign level when sending the RCS message. Since CleverTap will register a URL at the time of template creation to provide the flexibility of uploading media URL at the time of campaign creation, personalization will not be available for the URLs at the time of uploading the media while creating a campaign. 

     [block:image]{"images":[{"image":["https://files.readme.io/f14f7888d59f4da9cf1b7383552abcb52c6c5455460466c634e60622d7b859c0-Upload_in_campaign_-_thumbnail_-_carousel_-_rcs.png","","Upload in Campaign Thumbnail"],"align":"center","border":true,"caption":"Upload in Campaign Thumbnail"}]}[/block]
5. **Add a Title**: The title will be displayed in bold and can be up to 200 characters long.  
6. **Add a Description**: Enter the text message content, with a maximum limit of 1000 characters. 

   - **For body text formatting**: 

     - Adding Emojis: Copy from here and paste in the body.
     - Bold: Add asterisks (\*) at the beginning and end.
     - Italic: Add underscores (\_) at the beginning and end.
     - Strikethrough: Add tilde (~) at the beginning and end. 
     - Monospace: Add three consecutive backticks (\`\`\`) at the beginning and end. 

       [block:image]{"images":[{"image":["https://files.readme.io/49f1c6804539b5ecab504c5baeec741613bcaf9ee09f0b4a42b36e53e4f45aaf-Title_and_Description_-_carousel.png","","Title and Description"],"align":"center","border":true,"caption":"Title and Description"}]}[/block]
7. **Enable Buttons**: Toggle _ON_ if you want to include interactive buttons in the message (up to 4 buttons). There are three types of buttons that can be added. 

   - [URL Redirect](doc:rcs-message-templates#url-redirect) 
   - [Dialer](doc:rcs-message-templates#dialer) 
   - [Quick Reply](doc:rcs-message-templates#quick-reply) 

     [block:image]{"images":[{"image":["https://files.readme.io/0921d035e6f65cb6af6365555690bb010c8c8cada730e0f876a9a70c0b2f51d1-Carousel_-_Buttons.png","","Buttons"],"align":"center","border":true,"caption":"Buttons"}]}[/block]