---
title: Email Templates
excerpt: >-
  Learn about the HTML and AMP email templates offered by CleverTap out of the
  box.
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

CleverTap offers a wide range of email templates designed for a specific use case, from onboarding and re-engagement to promotions and transactional updates. This helps marketing and design teams identify the best fit for their campaign goals.

This document provides an overview of each template category and use case and highlights the customizable components available, such as logos, banners, Call-to-Action (CTAs), product grids, and theme colors. This ensures easy editing and brand consistency across campaigns. Whether launching a birthday offer, confirming an order, or showcasing a flash sale, this document gives you the structure and flexibility to build visually appealing emails that drive action and engagement.

<Callout icon="📘" theme="info">
  **Private Beta**

  The out-of-the-box HTML and AMP email templates are currently available in Private Beta. If you want access to this feature, contact your Customer Success Manager.
</Callout>

# HTML Templates

## Birthday Wish Template

This HTML email template is designed to help you celebrate your user's special day with a warm, personalized message. It combines festive visuals with a clear Call-to-Action (CTA) that can drive engagement, such as redeeming a gift, exploring birthday-exclusive deals, or simply revisiting the app or website. The layout is simple, responsive, and fully customizable to suit your brand.

<Image align="center" alt="Sample Birthday Template" border={true} caption="Sample Birthday Template" src="https://files.readme.io/c10b08d8ad83425b7524026133a40ae478093f2d6444dc41bad5ae1b936b0738-Birthday_HTML.png" width="25% " />

<br />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Send birthday wishes with a personalized message and special offer.
  * Deliver exclusive discount codes or gift coupons.
  * Encourage users to revisit your app, website, or store on their birthday.
  * Reinforce brand loyalty by showing you remember important moments.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
  	<title></title>
  	<style type="text/css">@font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 95% !important;             }                         .logo{                 width: 150px !important; height: 60px !important;             }             .offer-wrap{                 padding: 40px 15px !important;             }             .offer-title{                 font-size: 35px !important;                 line-height: 45px !important;             }             .cta{                 padding: 10px 25px !important;             }         }
  	</style>
  </head>
  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; background: aliceblue; cursor: auto;">
  <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%"><!-- header start-->
  	<tbody>
  		<tr>
  			<td align="center" class="container" style="display: block; padding: 24px 0; max-width: 90%; margin: 0 auto;">
  			<div class="logo-wrap"><!-- Change logo src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 159px; height: 73px; object-fit: cover;" /></div>
  			<!-- Change logo src as per your requirements --></td>
  		</tr>
  		<!-- header end-->
  		<tr>
  			<td style="text-align: center;">
  			<div class="container" style="max-width: 80%; margin: 0 auto 30px;"><!-- Change banner as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Birthday/banner.png" style="width: 100%; height: 100%; object-fit: cover;" /> <!-- Change banner as per your requirements --></div>
  			</td>
  		</tr>
  		<tr>
  			<td align="center" style="padding: 37px 0 47px; background: #FFF1EE;">
  			<div class="container" style="max-width: 80%; margin: 0 auto;">
  			<h2 style="margin: 0 0 20px; font-family: 'Jost', Arial, sans-serif; font-size: 30px; font-weight: 400 !important; color: #252525; line-height: 43px; text-align: center; ">08-09-2024</h2>

  			<p style="margin: 0; text-transform: none; font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 35px; text-align: center; color: #252525; "><strong>Happy Birthday, Emily!</strong></p>

  			<p style="margin: 0; text-transform: none; font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 35px; text-align: center; color: #252525; ">Celebrate your special day with a little something from us — an exclusive coupon code valid just for today. It’s our way of saying thanks for being part of our family.</p>
  			</div>
  			</td>
  		</tr>
  		<tr>
  			<td align="center" class="offer-wrap" style="padding: 50px 0;">
  			<div class="container" style="max-width: 80%; margin: 0 auto;">
  			<h3 class="offer-title" style="margin: 0 0 16px; font-family: 'Jost', Arial, sans-serif; font-size: 45px; font-weight: 300; line-height: 53px; text-align: center; ">Get <span style="font-style: italic; color: #FDB4AC; font-weight: 600;">30% </span>Off<br />
  			just for today!</h3>

  			<h4 style="margin: 0 0 16px; text-transform: uppercase; color: #545454; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 24px; text-align: center; ">USE CODE AT CHECKOUT: <strong>HAPPYBIRTHDAY</strong></h4>

  			<p style="margin: 0 0 23px; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 20px; color: #545454; text-align: center; text-transform: none;">Code valid only till February 15th 11:59pm</p>

  			<a class="cta" href="#" style="display:inline-block; background-color: #EDACAA; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400;line-height: 28px;text-align: center; color: #FFFFFF !important; text-transform: uppercase; border-radius: 25px; text-decoration: none; max-width: 233px; padding: 10px 63px;">shop now</a>
  			</div>
  			</td>
  		</tr>
  		<!-- footer start-->
  		<tr>
  			<td align="center" style="background: #FFF1EE;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin: 0 auto;">
  				<tbody>
  					<tr>
  						<td>
  						<p style="color: #252525; font-size: 18px; font-weight: 400; line-height: 35px; text-align: center; margin: 43px auto 25px; text-transform: none; max-width: 80%;">For assistance, connect with us on social media or reach out to our support team at 
  						<a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
  						</p>
  						</td>
  					</tr>
  					<tr>
  						<td style="border-top: 1px solid #EDACAA; padding: 25px 0;">
  						<table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
  							<tbody>
  								<tr>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 26px; height: 26px;"><!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/72bce39c01ce48258457146cb33a7a23.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 26px; height: 26px;"><!-- Change image src as per your requirements --><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/26e39559cb10487f8aa6db321f7ddf71.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 26px; height: 26px;"><!-- Change image src as per your requirements --><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/166c4d889bea433bb8790b99791b7409.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- footer end-->
  	</tbody>
  </table>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration></body>
  </html>
  ```
</Accordion>

## Feedback Template

This HTML template is designed to collect user input after a purchase, interaction, or experience. It features a clean layout with a feedback prompt, rating icons, text inputs, and a CTA that directs users to a feedback form or survey page.

<Image align="center" alt="Sample Feedback Template" border={true} caption="Sample Feedback Template" src="https://files.readme.io/2dcb3c6cd637b64182faf1f138ccaf5b1d13a61431b6caccf32834f1a1a7d544-Feedback_Template_HTML.png" width="35% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Example

  * Request feedback after a product purchase or delivery.
  * Gather user opinions following a customer support interaction.
  * Collect insights during a product beta or feature rollout.
  * Run CSAT or NPS to gauge loyalty.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">
  <head>
  	<title>Feedback</title>
  	<style type="text/css">@font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 90% !important;             }                         .logo{                 width: 150px !important; height: 60px !important;             }                        .cta{                 padding: 10px 25px !important;             }         }
  	</style>
  </head>
  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1198.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
  <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; border-spacing: 0 !important;" width="100%"><!-- header start-->
  	<tbody>
  		<tr>
  			<td align="center" class="container" style="display: block; padding: 20px 0; max-width: 90%; margin: 0 auto;">
  			<div class="logo-wrap"><!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 159px; height: 73px; object-fit: cover;" /></div>
  			</td>
  		</tr>
  		<!-- header end-->
  		<tr>
  			<td style="text-align: center; padding-bottom: 5px;background: #5A3D2B;"><!-- Change image src as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/banner.jpg" style="width: 100%; height: 100%; object-fit: cover;" /></td>
  		</tr>
  		<tr>
  			<td align="center" style="padding: 43px 0 80px;">
  			<div class="container" style="max-width: 85%; margin: 0 auto;">
  			<h2 class="title" style="margin: 0 0 15px; font-family: 'Jost', Arial, sans-serif; font-size: 32px; font-weight: 400 !important; color: #000000; line-height: 42px; text-align: center; text-transform: none;">We value your feedback</h2>

  			<p class="desc" style="margin: 0; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 30px; text-align: center; color: #7D7D7D;">Hi Emily,<br />
  			We’d love to hear about your experience ordering from our app! Your feedback will help us improve the app experience for you and other customers. Click on the button below to answer a few quick questions — this will only take a few minutes.</p>

  			<a class="cta" display_text_og="SHARE%20FEEDBACK" href="#" href_og="%23" style="margin-top: 30px; display: inline-block; background-color: rgb(90, 61, 43); font-family: Jost, Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28px; text-align: center; text-transform: none; border-radius: 5px; text-decoration: none; padding: 13px 10px; width: 85%; color: rgb(255, 255, 255) !important;">SHARE FEEDBACK</a>
  			</div>
  			</td>
  		</tr>
  		<!-- footer start-->
  		<tr>
  			<td align="center">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="padding: 50px 0; border-top: 1px solid #ADADAD">
  				<tbody>
  					<tr>
  						<td style="padding: 0 0 18px;">
  						<table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
  							<tbody>
  								<tr>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;"><!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d84491d2c49a419695672cacb928bde3.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;"><!-- Change image src as per your requirements --><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d84491d2c49a419695672cacb928bde3.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;"><!-- Change image src as per your requirements --><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/a2e1ff645faa427f997b50f6277f98fb.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<p style="color: #939393; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin: 0 auto; max-width: 80%;">For assistance, connect with us on social media or reach out to our support team at 
  						<a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
  						</p>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">To opt out of sharing feedback in the future, 
  						<a href="#" style="color:#5A3D2B;font-weight:bold;text-decoration:none;">unsubscribe here</a>
  						</p>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- footer end-->
  	</tbody>
  </table>
  </body>
                                                                                                      <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
  </html>
  ```
</Accordion>

## First Purchase Incentive Template

This HTML template is crafted to convert new users into paying customers by offering a compelling discount or reward on their first purchase. It combines welcoming language with a strong CTA, encouraging users to explore the catalog or complete their first transaction.

<Image align="center" alt="First Purchase Incentive Template" border={true} caption="Sample First Purchase Incentive Template" src="https://files.readme.io/13d1a813ccb1ef1a834b3415c855e2ea2d765b0b9574d47bddb6ad846522ba6a-First_Incentive_Template_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Send a welcome discount, for example, 10% off, after sign-up or app install.
  * Offer free shipping or a gift on the first order to increase conversion.
  * Trigger this email as part of an onboarding journey for new users.
  * Reinforce a sense of exclusivity with limited-time first-order benefits.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">
  <head>
  	<title>First Purchase Incentive</title>
  	<style type="text/css">@font-face { 			font-family: 'Jost', Arial; 			src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\'); 			font-style: normal; 			font-weight: 300; 		}  		@font-face { 			font-family: 'Jost', Arial; 			src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\'); 			font-style: normal; 			font-weight: 400; 		}  		@font-face { 			font-family: 'Jost', Arial; 			src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\'); 			font-style: normal; 			font-weight: 500; 		}  		@font-face { 			font-family: 'Jost', Arial; 			src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\'); 			font-style: normal; 			font-weight: 600; 		}  		@font-face { 			font-family: 'Jost', Arial; 			src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\'); 			font-style: normal; 			font-weight: 700; 		}  		@media screen and (max-width: 480px) { 			.container { 				max-width: 100% !important; 			}  			.content { 				max-width: 90% !important; 			}              .cta{                 padding: 5px !important;                 font-size: 10px !important;             }             .logo{                 width: 110px !important;                 height: 50px !important;             } 		}
  	</style>
  </head>
  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="cursor: auto;"><!-- Change Theme -->
  <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #ffffff; font-family: Jost, Arial, sans-serif; font-weight: 400;" width="100%">
  	<tbody>
  		<tr>
  			<td align="center" style="padding: 15px 0;"><!-- Change Logo Image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 145px; height: 60px; object-fit: cover;" /> <!-- Change Logo Image src as per your requirements --></td>
  		</tr>
  		<tr>
  			<td align="center">
  			<table class="container" style="background-color: #FFEEEE; padding: 30px 0; max-width: 81%; width: 100%; padding: 0 25px 30px; border: 0; border-spacing: 0; " width="100%">
  				<tbody>
  					<tr>
  						<td>
  						<table class="content" style="max-width: 83%; width: 100%; margin: 0 auto; border: 0; border-spacing: 0; " width="100%">
  							<tbody>
  								<tr>
  									<td align="center" style="padding: 45px 25px 30px; background-color: #FF5252;">
  									<h2 style="font-size: 22px; font-weight: 500; line-height: 26px; text-align: center; color: #FFFFFF; text-transform: uppercase; margin: 0;">WELCOME! HERE’S A SPECIAL DISCOUNT TO GET YOU STARTED</h2>

  									<p style="font-size: 10px; font-weight: 400; line-height: 31px; text-align: center; color: #FFFFFF; margin-bottom: 10px;">Enter the code below when making your first purchase. Hurry! Code valid only till Feb 15th.</p>

  									<a class="cta" href="#" style="padding: 5px 35px; font-size: 12px; font-weight: 400; line-height: 24px; color: #000; text-align: center; text-transform: uppercase; background-color: #FFFFFF; text-decoration: none; display: inline-block;">Shop Now</a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td align="center">
  						<div style="width: 100%; max-width: 430px; height: 247px;"><!-- Change Banner Image src as per your requirements --><img alt="Banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/first_purchase_incentive/banner.png" style="width: 100%; height:100%; object-fit: cover;" /> <!-- Change Banner Image src as per your requirements --></div>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<table class="content" style="max-width: 83%; width: 100%; margin: 0 auto; border: 0; border-spacing: 0; " width="100%">
  							<tbody>
  								<tr>
  									<td align="center" style="padding: 25px 15px 30px; background-color: #FF5252;">
  									<table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
  										<tbody>
  											<tr>
  												<td style="font-size: 14px; font-weight: 700; line-height: 20px; color: #FFFFFF; text-align: left;">GET FLAT 20% OFF <span style="font-weight: 500; display: block;">USE COUPON CODE</span>SAVE20</td>
  												<td align="right">
  												<a class="cta" href="#" style="padding: 5px 15px; font-size: 12px; font-weight: 400; line-height: 24px; color: #000 !important; background-color: #FFFFFF; text-decoration: none; text-transform: uppercase; display: inline-block;">Shop Now</a>
  												</td>
  											</tr>
  										</tbody>
  									</table>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- Footer Section -->
  		<tr>
  			<td align="center" style="background-color: #FF5252; padding: 30px 0;">
  			<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF; margin: 0 0 21px; max-width: 80%;">For assistance, connect with us on social media or reach out to our support team at 
  			<a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #FFFFFF" title="support@example.com">support@example.com</a>
  			</p>

  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin-bottom: 29px;">
  				<tbody><!-- Privacy Policy -->
  					<tr>
  						<td style="padding: 0 5px;">
  						<a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF !important; text-decoration: none;">Privacy</a>
  						</td>
  						<td style="padding: 0 5px;">
  						<a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF !important; text-decoration: none;">Account</a>
  						</td>
  					</tr>
  					<!-- Privacy Policy -->
  				</tbody>
  			</table>
  			<!-- Add Links --><!-- Download Android Section -->

  			<table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
  				<tbody>
  					<tr>
  						<td style="display: inline-block; padding: 5px 39px; border: 1px solid #FFFFFF;">
  						<a href="#" style="vertical-align: middle;display: inline-block; width: 24px; height: 24px;"><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
  						</td>
  						<td style="display: inline-block; padding: 5px 39px; border: 1px solid #FFFFFF;">
  						<a href="#" style="vertical-align: middle;display: inline-block; width: 24px; height: 24px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
  						</td>
  						<td style="display: inline-block; padding: 5px 39px; border: 1px solid #FFFFFF;">
  						<a href="#" style="vertical-align: middle;display: inline-block; width: 24px; height: 24px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/a971a978e8544cbfb0a0f3456c21463e.png" style="width: 100%; height: 100%;" /></a>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			<!-- Download Android Section --><!-- Add Links --></td>
  		</tr>
  		<!-- Footer Section -->
  		<tr>
  			<td align="center" style="background-color: #FF5252; padding: 30px 0;">
  			<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF; margin: 0 0 21px; max-width: 80%;">To opt out of promotional emails like this, 
  			<a href="#" style="color:#fff;font-weight:bold;text-decoration:none;">unsubscribe here</a>
  			</p>
  			</td>
  		</tr>
  	</tbody>
  </table>
    <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration></body>
  </html>
  ```
</Accordion>

## Flash Sale Template

The Flash Sale HTML template is optimized for high-conversion campaigns built around urgency. With clear messaging, a clear call-to-action, and support for a countdown timer, this template encourages users to take fast action during limited-time promotions or seasonal offers.

<Image align="center" alt="Sample Flash Sale Template" border={true} caption="Sample Flash Sale Template" src="https://files.readme.io/368ed48afa3fcadaf3c5e530141a5bf6cae026b6b2a822284905ec3c9762602a-Flash_Sale_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Example

  * Promote time-bound sales events (for example, 24-hour, weekend-only).
  * Run end-of-season clearance or flash discounts.
  * Highlight limited inventory to boost FOMO-driven engagement.
  * Launch app-exclusive or email-only timed deals.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)
  * [Configure the Countdown Timer](doc:ootb-email-templates#countdown-timer-flash-sale-only)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">
  <head>
  	<title>Flash Sale</title>
  	<link href="https://fonts.googleapis.com" rel="preconnect" />
  	<link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
  	<link href="https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,100..900;1,100..900&amp;display=swap" rel="stylesheet" />
  	<style type="text/css">@media only screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }             .product-container,             .footer-wrap,             .content {                 max-width: 95% !important;             }             .content-wrap{                 width: 60% !important;             }             .btn-wrap{                 width: 40% !important;             }             .flash-detail-wrap{                 height: 140px !important;                 padding: 0px 20px !important;             }             .img-wrap{                 height: 95px !important;                 width: 100% !important;             }             .logo{                 max-width: 130px !important;             }             .cta{                 padding: 5px 15px !important;             }             .media-item{                 padding: 0 20px !important;             }         }         @media only screen and (max-width: 360px) {             .img-wrap {                 height: 80px !important;                 width: 100% !important;             }         }
  	</style>
  </head>
  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
  <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%"><!-- header start-->
  	<tbody>
  		<tr>
  			<td style="text-align: center; position: relative; padding-top: 25px; background: #FFFFFF;">
  			<table border="0" cellpadding="0" cellspacing="0" width="100%">
  				<tbody>
  					<tr>
  						<td style="width: 50%; vertical-align: middle;">
  						<div style="border-top: 1px solid #FF7056;"> </div>
  						</td>
  						<td style="width: auto; text-align: center; vertical-align: middle;"><!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; max-width: 159px; height: auto; background: #FFFFFF; padding: 0 10px; vertical-align: middle;" /></td>
  						<td style="width: 50%; vertical-align: middle;">
  						<div style="border-top: 1px solid #FF7056;"> </div>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- header end-->
  		<tr>
  			<td style="text-align: center; background: #FFFFFF;">
  			<h1 style="font-family: 'Jost', Arial, sans-serif; font-size: 45px; font-weight: 300; line-height: 65.03px; color: #252525; text-transform: none; margin:28px 0 30px;">Mid-season sale <span style="display: block; font-size: 30px; font-weight: 300; line-height: 43.35px; text-transform: uppercase;">Up to</span> <span style="display: block; font-size: 45px; font-style: italic; font-weight: 500; line-height: 65.03px; color: #FF7056; text-transform: uppercase;">50%OFF</span></h1>
  			</td>
  		</tr>
  		<tr><!-- Change image src as per your requirements -->
  			<td class="flash-detail-wrap" style="background: #3B3B3B url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Flash%20Sale/Screenshot%202024-09-06%20at%208.05.56%E2%80%AFPM.png); background-position: center; background-repeat: no-repeat; background-size: cover; height: 168px; vertical-align: middle; padding: 0 100px;">
  			<div class="flash-details" style="width: 50%; vertical-align: middle;">
  			<h3 style="font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 900; line-height: 25px; text-align: left; color: #FBFBF6; margin: 0;">Only <span style="color: #FF7056;">two</span> days to go!</h3>

  			<p style="font-family: 'Jost', Arial, sans-serif; font-size: 9.2px; font-weight: 400; line-height: 13.3px; text-align: left; color: #FFFFFF; margin: 0">Hurry, the clock is ticking…</p>
  			</div>
  			</td>
  		</tr>
  		<tr>
  			<td style="text-align: center;">
  			<table border="0" cellpadding="0" cellspacing="0" width="100%">
  				<tbody>
  					<tr>
  						<td style="background: #FF7056;"><!-- Change image src as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Flash%20Sale/banner.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
  					</tr>
  					<tr>
  						<td style="padding: 15px 0 20px; background: #FF7056;">
  						<table border="0" cellpadding="0" cellspacing="0" style=" max-width: 90%; margin: 0 auto;" width="100%">
  							<tbody>
  								<tr>
  									<td class="content-wrap" style="width: 70%; text-align: left;">
  									<h3 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px;font-weight: 400;line-height: 24px; color: #FFFFFF; display: inline-block; text-align: left; margin-right: 10px;">Sale ends on Feb 15 2025, so hurry!</h3>
  									</td>
  									<td class="btn-wrap" style="width: 30%; text-align: right;">
  									<a class="cta" href="#" style="text-decoration: none; padding: 8px 36px;font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 24px; text-align: center; color: #000000 !important; background: #FFFFFF;">Shop Now</a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- product section -->
  		<tr>
  			<td style="background: #FFFFFF;">
  			<div class="product-container" style="margin: 0 auto; width: 100%; padding-top: 30px;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width: 100%;">
  				<tbody>
  					<tr>
  						<td style="padding-bottom: 20px; ">
  						<h3 style="font-family: 'Jost', Arial, sans-serif;font-size: 24px;font-weight: 300;line-height: 52px; color: #000000; text-transform: uppercase; margin: 0;vertical-align: middle;">Products</h3>
  						</td>
  						<td colspan="2" style="vertical-align: middle; padding-bottom: 20px;">
  						<div style="border-top: 1px solid #FF7056;"> </div>
  						</td>
  					</tr>
  					<tr>
  						<td style="vertical-align: top; width: 30%; padding: 0 5px;"><!-- product card -->
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin-bottom: 15px; ">
  							<tbody>
  								<tr>
  									<td colspan="2">
  									<div class="img-wrap" style="height: 157px;"><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Flash%20Sale/product-1.png" style="width: -webkit-fill-available; height: 100%; object-fit: cover;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td style="width: 60%; margin-bottom: 2px; vertical-align: top;">
  									<h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 18px; color: #252525; margin: 5px 0;padding-right: 5px;">Urban Lace - Ups</h4>
  									</td>
  									<td style="width: 20%; vertical-align: top;">
  									<p style="margin:5px 0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height: 18px; text-align: right;"><span class="rupee-sign">$</span>1500</p>
  									</td>
  								</tr>
  								<tr>
  									<td colspan="2">
  									<p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Step out in style with these sleek, versatile lace-ups perfect for any occasion.</p>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  						<td style="vertical-align: top; width: 30%; padding: 0 5px;"><!-- product card -->
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin-bottom: 15px;">
  							<tbody>
  								<tr>
  									<td colspan="2">
  									<div class="img-wrap" style="height: 157px;"><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Flash%20Sale/product-2.png" style="width: -webkit-fill-available; height: 100%; object-fit: cover;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td style="width: 60%; margin-bottom: 2px; vertical-align: top;">
  									<h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 18px; color: #252525; margin: 5px 0;padding-right: 5px;">Caramel Classic Heels</h4>
  									</td>
  									<td style="width: 20%; vertical-align: top;">
  									<p style="margin:5px 0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height: 18px; text-align: right;"><span class="rupee-sign">$</span>1500</p>
  									</td>
  								</tr>
  								<tr>
  									<td colspan="2">
  									<p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Elegant and comfortable, these timeless heels pair effortlessly with every outfit.</p>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  						<td style="vertical-align: top; width: 30%; padding: 0 5px;"><!-- product card -->
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin-bottom: 15px;">
  							<tbody>
  								<tr>
  									<td colspan="2">
  									<div class="img-wrap" style="height: 157px;"><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Flash%20Sale/product-3.png" style="width: -webkit-fill-available; height: 100%; object-fit: cover;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td style="width: 60%; margin-bottom: 2px; vertical-align: top;">
  									<h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 18px; color: #252525; margin: 5px 0;padding-right: 5px;">Strappy Wedges</h4>
  									</td>
  									<td style="width: 20%; vertical-align: top;">
  									<p style="margin:5px 0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height: 18px; text-align: right;"><span class="rupee-sign">$</span>1500</p>
  									</td>
  								</tr>
  								<tr>
  									<td colspan="2">
  									<p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Add height and ease with these chic wedges designed for all-day wear.</p>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</div>
  			</td>
  		</tr>
  		<tr>
  			<td style="background: #FFFFFF;">
  			<div style="max-width: 90%; margin: 0 auto; width: 100%; text-align: right; padding-bottom: 39px;">
  			<a class="btn-link" href="#" style="font-family: 'Jost', Arial, sans-serif;                     font-size: 12px; font-weight: 400; line-height: 15px; text-transform: none; color: #FF5252 !important; text-decoration: none; ">VIew All <img alt="arrow" class="margin-left: 10px" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Flash%20Sale/arrow.png" /></a>
  			</div>
  			</td>
  		</tr>
  		<!-- product section --><!-- footer start-->
  		<tr>
  			<td align="center" style="padding: 26px 0;  background: #FF7056;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" class="footer-wrap" role="presentation" style=" max-width: 63%; margin: 0 auto;">
  				<tbody>
  					<tr>
  						<td style="padding: 0 0 29px ;">
  						<table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
  							<tbody>
  								<tr>
  									<td class="media-item" style="padding: 7px 40px; display: inline-block; border-right: 1px solid #FFFFFF;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px; "><!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td class="media-item" style="padding: 7px 40px; display: inline-block; border-right: 1px solid #FFFFFF;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><!-- Change image src as per your requirements --><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td class="media-item" style="padding: 7px 40px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><!-- Change image src as per your requirements --><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/71671637f46e471bb27fbe3cdd00859a.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF; margin: 0 0 24px;">For assistance, connect with us on social media or reach out to our support team at 
  						<a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #FFFFFF;" title="support@example.com">support@example.com</a>
  						</p>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
  							<tbody>
  								<tr>
  									<td style="padding: 0 5px;">
  									<a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF !important; text-decoration: none;">Privacy</a>
  									</td>
  									<td style="padding: 0 5px;">
  									<a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF !important; text-decoration: none;">Account</a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #fff; padding-top:10px;">To opt out of promotional emails like this, 
  						<a href="#" style="color:#fff;font-weight:bold;text-decoration:none;">unsubscribe here</a>
  						</p>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- footer end-->
  	</tbody>
  </table>
    <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration></body>
    </html>
  ```
</Accordion>

## Cart Abandonment Template

The Cart Abandonment HTML template is a re-engagement template designed to remind users about items they have added to their cart but have not purchased. It combines persuasive text, compelling visuals, and a CTA to recover potential lost revenue and guide users back to checkout.

<Image align="center" alt="Sample Cart Abandonment Template " border={true} caption="Sample Cart Abandonment Template" src="https://files.readme.io/260c597f1463ea160bfdbb9c740f8b65957555a0500892a16c70fc1cd18c0348-Cart_Abandonment_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Re-engage users who left products in their cart without completing the purchase.
  * Offer limited-time discounts or free shipping to incentivize completion.
  * Showcase cart contents with dynamic product previews.
  * Trigger automated emails based on cart inactivity (for example, after 1 hour, 24 hours).

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">
  <head>
  	<title>Cart Abandonment</title>
  	<style type="text/css">@font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }              .main {                 max-width: 90% !important;             }              .look-sec {                 padding-top: 30px !important;             }              .sec-head {                 max-width: 65% !important;             }             .cta{                 font-size: 10px !important;                 padding: 5px !important;             }         }
  	</style>
  </head>
  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;"><!-- Change Theme -->
  <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%"><!-- header start-->
  	<tbody>
  		<tr>
  			<td style="text-align: left; vertical-align: middle; padding: 20px"><!-- Change Logo Image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /> <!-- Change Logo Image src as per your requirements --></td>
  			<td style="text-align: right; vertical-align: middle; padding: 20px">
  			<div class="head-nav"><img alt="call icon" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/call-icon.png" style="width: 20px; height: 20px; display: inline-block; vertical-align: middle;" /> <span style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #464646; display: inline-block; vertical-align: middle;">9878725637</span></div>
  			</td>
  		</tr>
  		<!-- header end--><!-- Banner Image -->
  		<tr>
  			<td colspan="2"><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/banner.png" style="width: 100%; height: 100%; max-height: 361px; object-fit: cover;" /></td>
  		</tr>
  		<!-- Banner Image --><!-- looks section -->
  		<tr>
  			<td class="look-sec" colspan="2" style="padding: 50px 0 0; text-align: center;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 90%; margin: 0 auto; width: 100%;" width="100%">
  				<tbody>
  					<tr>
  						<td style="text-align: center;">
  						<h2 style="padding: 12px 26px; border-bottom: 1px solid #000000; text-transform: uppercase;font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; max-width: 400px; margin: 0 auto;">YOU LEFT THESE ITEMS IN YOUR CART</h2>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin: 30px 0; width: 100%;" width="100%">
  							<tbody>
  								<tr>
  									<td style="text-align: center; padding: 8px 0; background: #1E1E1E;">
  									<p style="margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 13px; letter-spacing: 0.25em; color: #FFFFFF;">Check out in the next 12 hours to get flat 20% off!</p>
  									</td>
  								</tr>
  								<tr>
  									<td>
  									<div class="look-img" style="background: #F1F1F1;"><img alt="look" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-1.png" style="width:100%; height: 100%; object-fit: contain;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td>
  									<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="padding: 10px 15px; background: #F1F1F1; width: 100%;">
  										<tbody>
  											<tr>
  												<td style="width: 50%; text-align: left; vertical-align: middle;">
  												<h2 style="margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #252525;">Orange Long-Sleeved Tee</h2>
  												</td>
  												<td style="width: 50%; text-align: right; vertical-align: middle;">
  												<p style="margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 22px; font-style: italic; font-weight: 400; line-height: 26px;"><span style="font-size: 10px; line-height: 26px;">$</span>150</p>
  												</td>
  											</tr>
  											<tr>
  												<td style="width: 50%; text-align: left; vertical-align: middle;">
  												<p style="margin: 0; text-transform: none; color: #545454; font-family: 'Jost', Arial, sans-serif; font-size: 10px; font-weight: 400; line-height: 13px; text-align: left; ">Stylish and comfortable, perfect for casual wear or layering.</p>
  												</td>
  												<td style="width: 50%; text-align: right; vertical-align: middle;">
  												<a class="cta" href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; text-transform: uppercase; line-height: 20px; color: #FFFFFF !important; text-decoration: none; background: #000000; padding: 4px 34px; display: inline-block; text-align: center; max-width: 167px;">ADD TO CART</a>
  												</td>
  											</tr>
  										</tbody>
  									</table>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin: 30px 0; width: 100%;" width="100%">
  							<tbody>
  								<tr>
  									<td style="text-align: center; padding: 8px 0; background: #1E1E1E;">
  									<p style="margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 13px; letter-spacing: 0.25em; color: #FFFFFF;">Check out in the next 12 hours to get flat 20% off!</p>
  									</td>
  								</tr>
  								<tr>
  									<td>
  									<div class="look-img" style="background: #F1F1F1;"><img alt="look" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-2.png" style="width:100%; height: 100%; object-fit: contain;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td>
  									<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="padding: 10px 15px; background: #F1F1F1; width: 100%;">
  										<tbody>
  											<tr>
  												<td style="width: 50%; text-align: left; vertical-align: middle;">
  												<h2 style="margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #252525;">Midnight Black Hoodie</h2>
  												</td>
  												<td style="width: 50%; text-align: right; vertical-align: middle;">
  												<p style="margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 22px; font-style: italic; font-weight: 400; line-height: 26px;"><span style="font-size: 10px; line-height: 26px;">$</span>150</p>
  												</td>
  											</tr>
  											<tr>
  												<td style="width: 50%; text-align: left; vertical-align: middle;">
  												<p style="margin: 0; text-transform: none; color: #545454; font-family: 'Jost', Arial, sans-serif; font-size: 10px; font-weight: 400; line-height: 13px; text-align: left; ">Cozy, comfortable, and ideal for any occasion.</p>
  												</td>
  												<td style="width: 50%; text-align: right; vertical-align: middle;">
  												<a class="cta" href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; text-transform: uppercase; line-height: 20px; color: #FFFFFF !important; text-decoration: none; background: #000000; padding: 4px 34px; display: inline-block; text-align: center; max-width: 167px;">ADD TO CART</a>
  												</td>
  											</tr>
  										</tbody>
  									</table>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- looks section --><!-- product section -->
  		<tr>
  			<td colspan="2" style=" background: #F1F1F1;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 90%; margin: 30px auto; width: 100%;" width="100%">
  				<tbody>
  					<tr>
  						<td>
  						<h2 class="sec-head" style="padding: 12px 26px; border-bottom: 1px solid #000000; text-transform: uppercase;font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; max-width: 55%; margin: 0 auto; text-align: center;">YOU MAY ALSO LIKE THESE</h2>
  						</td>
  					</tr>
  					<!-- product section -->
  					<tr>
  						<td>
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width: 100%; margin-top: 20px;">
  							<tbody>
  								<tr>
  									<td style="vertical-align: top; width: 30%;"><!-- product card -->
  									<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0 5px 10px; padding: 5px;">
  										<tbody>
  											<tr>
  												<td colspan="2">
  												<div class="product-img-wrap" style="max-width: 161px; max-height: 255px; "><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-1.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
  												</td>
  											</tr>
  											<tr>
  												<td style="width: 60%; margin-bottom: 2px; vertical-align: middle;">
  												<h4 class="p-title" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 18px; color: #252525; margin: 5px 0;padding-right: 5px;">Earthy Comfort Tee</h4>
  												</td>
  												<td style="width: 20%; vertical-align: middle;">
  												<p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 10px;font-weight: 300; line-height: 15px; text-align: right; font-style: italic;">$150</p>
  												</td>
  											</tr>
  											<tr>
  												<td colspan="2">
  												<p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Soft and breathable brown tee, perfect for everyday casual wear.</p>
  												</td>
  											</tr>
  										</tbody>
  									</table>
  									</td>
  									<td style="vertical-align: top; width: 30%;"><!-- product card -->
  									<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0 5px 10px; padding: 5px;">
  										<tbody>
  											<tr>
  												<td colspan="2">
  												<div class="product-img-wrap" style="max-width: 161px; max-height: 255px; "><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-2.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
  												</td>
  											</tr>
  											<tr>
  												<td style="width: 60%; margin-bottom: 2px; vertical-align: middle;">
  												<h4 class="p-title" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 18px; color: #252525; margin: 5px 0;padding-right: 5px;">Classic White Crew</h4>
  												</td>
  												<td style="width: 20%; vertical-align: middle;">
  												<p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 10px;font-weight: 300; line-height: 15px; text-align: right; font-style: italic;">$150</p>
  												</td>
  											</tr>
  											<tr>
  												<td colspan="2">
  												<p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">A timeless white tee, effortlessly stylish and ultra-comfortable.</p>
  												</td>
  											</tr>
  										</tbody>
  									</table>
  									</td>
  									<td style="vertical-align: top; width: 30%;"><!-- product card -->
  									<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0 5px 10px; padding: 5px;">
  										<tbody>
  											<tr>
  												<td colspan="2">
  												<div class="product-img-wrap" style="max-width: 161px; max-height: 255px; "><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-3.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
  												</td>
  											</tr>
  											<tr>
  												<td style="width: 60%; margin-bottom: 2px; vertical-align: middle;">
  												<h4 class="p-title" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 18px; color: #252525; margin: 5px 0;padding-right: 5px; ">Indigo Essentials Jeans</h4>
  												</td>
  												<td style="width: 20%; vertical-align: middle;">
  												<p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 10px;font-weight: 300; line-height: 15px; text-align: right; font-style: italic;">$150</p>
  												</td>
  											</tr>
  											<tr>
  												<td colspan="2">
  												<p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Flattering blue jeans designed for ultimate comfort and versatility.</p>
  												</td>
  											</tr>
  										</tbody>
  									</table>
  									</td>
  								</tr>
  								<tr>
  									<td colspan="3" style="text-align: right;">
  									<a display_text_og="View%20All" href="#" href_og="%23" style="font-family: Jost, Arial, sans-serif; font-size: 12px; font-weight: 400; text-transform: none; line-height: 15px; text-decoration: none; display: inline-block; text-align: center; margin-top: 15px; color: rgb(0, 0, 0) !important;">View All</a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<!-- product section -->
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- product section --><!-- Footer Section -->
  		<tr>
  			<td align="center" colspan="2" style="padding-top: 50px;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background: #1E1E1E; padding: 32px 0 34px;">
  				<tbody>
  					<tr>
  						<td style="padding: 0;">
  						<table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%"><!-- Add Links --><!-- Download Android Section -->
  							<tbody>
  								<tr>
  									<td style="padding: 7px 40px; display: inline-block; border: 1px solid #ffffff;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px; "><!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 7px 40px; display: inline-block; border: 1px solid #ffffff;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 7px 40px; display: inline-block; border: 1px solid #ffffff;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/c6684e1db05c4ce4b7783b6181e11c89.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  								</tr>
  								<!-- Add Links -->
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<p style="font-size: 14px; font-weight: 400; line-height: 20px; text-align: center; color: #FFFFFF ;margin: 20px auto 0; max-width: 84%;  text-transform: none;">For assistance, connect with us on social media or reach out to our support team at 
  						<a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #FFFFFF;" title="support@example.com">support@example.com</a>
  						</p>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #fff; padding-top:10px;">To opt out of promotional emails like this, 
  						<a href="#" style="color:#fff;font-weight:bold;text-decoration:none;">unsubscribe here</a>
  						</p>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- footer end-->
  	</tbody>
  </table>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration></body>
  </html>
  ```
</Accordion>

## Early Access to Sale Template

The Access to Early Sales HTML template is designed to give a sense of exclusivity to loyal or high-value users by offering them early access to upcoming sales or product launches. The layout focuses on premium branding, urgency, and conversion, encouraging users to take advantage of their early access window before it opens to the public.

<Image align="center" alt="Sample Early Access to Sale Template" border={true} caption="Sample Early Access to Sale Template" src="https://files.readme.io/52f0c237409986e177dee4c23a61d92a54f8c615dcad584d3e06ee04fb88015f-Early_Access_to_Sale_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Reward loyal customers with a 24-hour head start on sale events.
  * Launch new collections or limited-edition products with VIP previews.
  * Offer sneak peeks of seasonal drops or collaborations.
  * Boost conversions from high-intent segments (for example, waitlisted users or subscribers).

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">
  <head>
  	<title>Access to early sale</title>
  	<style type="text/css">@font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @font-face {             font-family: \'Poppins\', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }              .main {                 max-width: 90% !important;             }              .img-wrap {                 max-width: 50px !important;                 max-height: 50px !important;             }              .logo {                 width: 130px !important;                 height: 52px !important;                 padding: 15px 0 !important;             }              .main-title {                 font-size: 30px !important;                 line-height: 40px !important;             }              .main-desc {                 font-size: 12px !important;                 line-height: 18px !important;                 max-width: 70% !important;             }         }
  	</style>
  </head>
  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
  <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%"><!-- header start-->
  	<tbody>
  		<tr>
  			<td style="text-align: center; position: relative;">
  			<table border="0" cellpadding="0" cellspacing="0" class="main" style="max-width: 90%; margin: 0 auto; border: 1px solid #AC8763; border-top: 0 ;" width="100%">
  				<tbody>
  					<tr>
  						<td><!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 146px; height: 57px; object-fit: cover; padding: 30px 0;" /></td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- header end--><!-- category start-->
  		<tr>
  			<td>
  			<table border="0" cellpadding="0" cellspacing="0" class="main" style="max-width: 90%; margin: 0 auto;border-left: 1px solid #AC8763; border-right: 1px solid #AC8763; padding: 26px 0 31px;" width="100%">
  				<tbody>
  					<tr>
  						<td>
  						<div class="img-wrap" style="max-width: 103px; max-height: 103px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/category-1.png" style="width: 100%; height: 100%; object-fit: cover; border: 3px solid #DFDCD1; border-radius: 50%;" /></div>

  						<p style="font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">Jackets</p>
  						</td>
  						<td>
  						<div class="img-wrap" style="max-width: 103px; max-height: 103px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/category-2.png" style="width: 100%; height: 100%; object-fit: cover; border: 3px solid #DFDCD1; border-radius: 50%;" /></div>

  						<p style="font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">Shirts</p>
  						</td>
  						<td>
  						<div class="img-wrap" style="max-width: 103px; max-height: 103px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/category-3.png" style="width: 100%; height: 100%; object-fit: cover; border: 3px solid #DFDCD1; border-radius: 50%;" /></div>

  						<p style="font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">Jeans</p>
  						</td>
  						<td>
  						<div class="img-wrap" style="max-width: 103px; max-height: 103px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/category-4.png" style="width: 100%; height: 100%; object-fit: cover; border: 3px solid #DFDCD1; border-radius: 50%;" /></div>

  						<p style="font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">T-Shirts</p>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- category end--><!-- banner start-->
  		<tr>
  			<td><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/banner.png" style="width: 100%; height: 100%; max-height: 355px; object-fit: cover;" /></td>
  		</tr>
  		<!-- banner end--><!-- product start -->
  		<tr>
  			<td style="text-align: center; position: relative; border-top: 1px solid #AC8763 ">
  			<table border="0" cellpadding="0" cellspacing="0" class="main" style="max-width: 90%; margin: 0 auto; border-left: 1px solid #AC8763; border-right: 1px solid #AC8763 ; padding: 40px 0 30px;" width="100%">
  				<tbody>
  					<tr>
  						<td colspan="3">
  						<h2 class="main-title" style="margin: 0 0 5px; color: #525C46; font-family: 'Jost', Arial, sans-serif; font-size: 50px; font-weight: 400; line-height: 62px; text-align: center; text-transform: uppercase;">EXCLUSIVE EARLY ACCESS!</h2>

  						<h2 class="main-title" style="margin: 0 0 5px; color: #525C46; font-family: 'Jost', Arial, sans-serif; font-size: 50px; font-weight: 400; line-height: 62px; text-align: center; text-transform: uppercase;"><span style="font-weight: 300;font-size: 30px;">Get</span> <span style="font-weight: 300;">30% </span>Off</h2>

  						<p class="main-desc" style="font-family: \'Poppins\', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; text-transform: none; color: #6F6F6F; max-width: 70%; margin: 0 auto 30px;">Here are some items on sale we think you’ll love.</p>
  						</td>
  					</tr>
  					<tr>
  						<td style="vertical-align: top; width: 30%;"><!-- product card -->
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFF3E7; margin: 0 5px 35px; padding: 5px 5px 10px;">
  							<tbody>
  								<tr>
  									<td>
  									<div class="product-img-wrap" style="max-width: 161px; max-height: 255px; "><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/product-1.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td style="vertical-align: middle; text-align: left;">
  									<h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 500; line-height: 20px; margin: 7px 0 0; color: #000000; text-transform: none;">Earthly Comfort Tee</h4>

  									<p class="desc" style="margin:0 0 10px; font-family: \'Poppins\', Arial, sans-serif; font-size: 8px; line-height: 12px; color: #6F6F6F; text-transform: none;">Soft and breathable brown tee, perfect for everyday casual wear.</p>

  									<a class="btn-link" href="#" style="display: block; font-family: 'Jost', Arial, sans-serif;                                         font-size: 10px; font-weight: 400; line-height: 12px; text-align: center; padding: 5px; text-decoration: none; background: #AC8763;color: #FFFFFF !important">Shop Now</a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  						<td style="vertical-align: top; width: 30%;"><!-- product card -->
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFF3E7; margin: 0 5px 35px; padding: 5px 5px 10px;">
  							<tbody>
  								<tr>
  									<td>
  									<div class="product-img-wrap" style="max-width: 161px; max-height: 255px; "><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/product-2.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td style="vertical-align: middle; text-align: left;">
  									<h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 500; line-height: 20px; margin: 7px 0 0; color: #000000; text-transform: none;">Classic White Crew</h4>

  									<p class="desc" style="margin:0 0 10px; font-family: \'Poppins\', Arial, sans-serif; font-size: 8px; line-height: 12px; color: #6F6F6F; text-transform: none;">A timeless white tee, effortlessly stylish and ultra-comfortable.</p>

  									<a class="btn-link" href="#" style="display: block; font-family: 'Jost', Arial, sans-serif;                                         font-size: 10px; font-weight: 400; line-height: 12px; text-align: center; padding: 5px; text-decoration: none; background: #AC8763;color: #FFFFFF !important">Shop Now</a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  						<td style="vertical-align: top; width: 30%;"><!-- product card -->
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFF3E7; margin: 0 5px 35px; padding: 5px 5px 10px;">
  							<tbody>
  								<tr>
  									<td>
  									<div class="product-img-wrap" style="max-width: 161px; max-height: 255px; "><!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/access-to-early-sales/product-3.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
  									</td>
  								</tr>
  								<tr>
  									<td style="vertical-align: middle; text-align: left;">
  									<h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 500; line-height: 20px; margin: 7px 0 0; color: #000000; text-transform: none;">Indigo Essentials Jeans</h4>

  									<p class="desc" style="margin:0 0 10px; font-family: \'Poppins\', Arial, sans-serif; font-size: 8px; line-height: 12px; color: #6F6F6F; text-transform: none;">Flattering blue jeans designed for ultimate comfort and versatility.</p>

  									<a class="btn-link" href="#" style="display: block; font-family: 'Jost', Arial, sans-serif;                                         font-size: 10px; font-weight: 400; line-height: 12px; text-align: center; padding: 5px; text-decoration: none; background: #AC8763;color: #FFFFFF !important">Shop Now</a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td colspan="3" style="text-align: center;">
  						<a class="btn-link" display_text_og="Access%20Sale" href="#" href_og="%23" style="display: block; font-family: Jost, Arial, sans-serif; font-size: 10px; font-weight: 400; line-height: 12px; text-align: center; padding: 7px; text-decoration: none; background: rgb(172, 135, 99); width: 106px; margin: 0px auto; color: rgb(255, 255, 255) !important;">Access Sale</a>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- You might also start-->
  		<tr>
  			<td style="text-align: center; position: relative; border-top: 1px solid #AC8763 ">
  			<table border="0" cellpadding="0" cellspacing="0" class="main" style="max-width: 90%; margin: 0 auto; border-left: 1px solid #AC8763; border-right: 1px solid #AC8763 ; padding: 33px 0 40px;" width="100%">
  				<tbody>
  					<tr>
  						<td>
  						<h3 class="sec-title" style="margin: 0 0 20px; color: #909090; font-family: 'Jost', Arial, sans-serif;                            font-size: 20px;font-weight: 400;line-height: 20px;text-align: center; text-transform: none;">Thank you for being a part of the Elite Savings Club</h3>

  						<p class="sec-desc" style="margin: 0; font-family: \'Poppins\', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; text-transform: none;">As a valued member of our inner circle, you’re among the first to enjoy exclusive early access to our biggest deals.</p>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- You might also end--><!-- footer start-->
  		<tr>
  			<td align="center" style="background: #AC8763;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 80%; margin: 0 auto;">
  				<tbody>
  					<tr>
  						<td style="padding: 24px 0; border-bottom: 1px solid #FFFFFF;">
  						<table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
  							<tbody>
  								<tr>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px; "><!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  									<td style="padding: 0 15px; display: inline-block;">
  									<a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9c7f49934be54fefa121589ed170c74a.png" style="width: 100%; height: 100%;" /></a>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  					<tr>
  						<td>
  						<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF; margin: 20px auto 30px;">For assistance, connect with us on social media or reach out to our support team at 
  						<a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #FFFFFF;" title="support@example.com">support@example.com</a>
  						</p>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<tr>
  			<td align="center" style="background: #AC8763;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin: 0 auto;  padding: 15px 0; border-top: 1px solid #FFFFFF; width: 100%;">
  				<tbody>
  					<tr>
  						<td>
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
  							<tbody>
  								<tr>
  									<td style="padding: 0 5px;">
  									<a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF !important; text-decoration: none;">Privacy</a>
  									</td>
  									<td style="padding: 0 5px;">
  									<a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #FFFFFF !important; text-decoration: none;">Account</a>
  									</td>
  								</tr>
  								<tr>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<tr>
  			<td align="center" style="background: #AC8763;">
  			<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin: 0 auto;  padding: 15px 0; border-top: 1px solid #FFFFFF; width: 100%;">
  				<tbody>
  					<tr>
  						<td>
  						<table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
  							<tbody>
  								<tr>
  									<td>
  									<p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #fff; padding-top:10px;">To opt out of promotional emails like this, 
  									<a href="#" style="color:#fff;font-weight:bold;text-decoration:none;">unsubscribe here</a>
  									</p>
  									</td>
  								</tr>
  							</tbody>
  						</table>
  						</td>
  					</tr>
  				</tbody>
  			</table>
  			</td>
  		</tr>
  		<!-- footer end-->
  	</tbody>
  </table>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration></body>
  </html>
  ```
</Accordion>

## Email Verification Template

A transactional HTML email template designed to verify user identity during account creation or to confirm secure actions such as login from a new device. It prioritizes clarity, trust, and accessibility to ensure users can complete verification quickly.

<Image align="center" alt="Sample Account Verification Template" border={true} caption="Sample Email Verification Template" src="https://files.readme.io/4de714623cf3130b69168813bdf02546185d4568a4ef71a6c74b0d57f1e2fdaf-Email_Verification_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Example

  * Send a One-Time Password (OTP) or verification link for new user sign-ups.
  * Confirm user identity during suspicious login attempts or password resets.
  * Verify email before allowing access to sensitive features or gated services.
  * Validate changes to account details such as email, phone number, or device login.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Account Verification</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }             .box-table{                 margin: 15px 15px 0px !important;                 padding: 20px 0px !important;             }             .imgConfirmation{                 width:50% !important;             }             .content-sec {                 padding: 10px !important;                 margin-top: 0px !important;             }             .footer-content{                 padding: 0px 10px !important;             }             .expiry-para{                 padding: 0px 0px !important;             }             .main-heading{                 font-size: 24px !important;                 line-height: 30px !important;             }         }
      </style>
  </head>

  <body data-new-gr-c-s-loaded="14.1198.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #F0EEF6; padding: 30px 0px 0px;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="text-align: center; vertical-align: middle; padding: 20px; margin: 0px 30px; display: block;">
                      <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /></td>
              </tr>
              <!-- header end-->
              <tr>
                  <td>
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="box-table" role="presentation" style="padding: 50px 0px;box-shadow: 0px 1px 12px 0px #0000001A;margin: 0px 30px; display: block; background-color: #ffffff;;">
                          <tbody>
                              <!-- Information Section -->
                              <tr>
                                  <td class="information-sec" style="text-align: center;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;"><img alt="look" class="imgConfirmation" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AccountVerification/verifyemail.png" style="width:auto; height: auto; object-fit: cover;" /></td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <!-- Information Section -->
                              <!-- Content section -->
                              <tr>
                                  <td class="content-sec" style="background: #ffffff; padding: 0px 80px; text-align: center; display: block;margin-top: 30px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <h2 class="main-heading" style="text-transform: none;font-family: 'Jost', Arial, sans-serif; font-size: 30px; font-weight: 400; line-height: 43px; margin: 0 auto; color:#525C46;">Verify your email address</h2>

                                                      <div style="border-bottom: 1px solid #8E6AD0; width: 62px; display: block; margin: 10px auto;"> </div>

                                                      <p class="expiry-para" style="text-transform: none; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; ">Thank you for signing up with our app! To activate your account and get started, please verify your email address by clicking the button below.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <!-- Content Point section -->
                              <!-- confirm  section -->
                              <tr>
                                  <td>
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="width: 100%; text-align: center; vertical-align: middle;"><a display_text_og="Verify%20Email" href="#" href_og="%23" style="font-family: Jost, Arial, sans-serif; font-size: 20px; font-weight: 400; text-transform: none; line-height: 28px; text-decoration: none; background: rgb(142, 106, 208); padding: 4px 34px; display: inline-block; text-align: center; max-width: 167px; color: rgb(251, 252, 252) !important;">Verify Email</a></td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <!-- confirm  section -->
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer start-->
              <tr>
                  <td align="center" colspan="2">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="box-table" role="presentation" style="box-shadow: 0px 1px 12px 0px #0000001A; margin: 30px 30px 0px; display: block; background: #ffffff; padding: 25px 0 25px;">
                          <tbody>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/81d373cbc26b47238e3d1a24d1231781.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block; ">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/6a6ac7e37ba14cf79779d55f517088cb.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/0a46830d31674b52ae3e701ddd996adf.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 20px">
                                                      <p style="text-transform: none; color: #909090; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center;">For assistance, connect with us on social media or reach out to our support team at <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #909090;" title="support@example.com">support@example.com</a></p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="padding: 0px 15px; display: inline-block;"><a href="#" style="vertical-align: middle;display: inline-block; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center;font-family: 'Jost', Arial, sans-serif;text-decoration: none;color:#1E1E1E; ">Privacy</a></td>
                                                  <td style="padding: 0px 15px; display: inline-block; "><a href="#" style="vertical-align: middle;display: inline-block; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center;font-family: 'Jost', Arial, sans-serif;text-decoration: none;color:#1E1E1E;">Account</a></td>
                                              </tr>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 20px">
                                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">This is a system-generated email. Please do not reply.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
      </body>
    	</html>
  ```
</Accordion>

## Anniversary Wish Template

A relationship-nurturing HTML template designed to celebrate a customer’s anniversary with your brand, whether it is their sign-up, first purchase, or membership milestone.

<Image align="center" alt="Sample Anniversary Wish Template" border={true} caption="Sample Anniversary Wish Template" src="https://files.readme.io/f05b33c85a4f8bf90b9e0378cb52bfcaae386e2b1c1a049a22f24eaf6a7a93ba-Anniversary_Wish_Template_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Celebrate the anniversary of user sign-up, account creation, or first interaction.
  * Reinforce brand loyalty with personalized greetings and exclusive discounts.
  * Use dynamic content (such as user name, years with brand) to boost emotional connection.
  * Perfect for loyalty campaigns, long-term engagement, and reactivation efforts.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Anniversary</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 478px) {             .container {                 max-width: 90% !important;             }                         .logo{                 width: 150px !important; height: 60px !important;             }             .cta{                 padding: 10px 25px !important;             }             .offer-wrap{                 padding: 40px 15px !important;             }             .offer-title{                 font-size: 35px !important;                 line-height: 45px !important;             }             .title{                 font-size: 35px !important;                 line-height: 45px !important;             }             .code{                 line-height: 20px !important;                 margin-bottom: 20px !important;             }             .date{                 font-size: 26px !important;                 line-height: 30px !important;             }             .wishes-txt{                 font-size: 16px !important;                 line-height: 24px !important;             }             .footer-desc{                 line-height: 28px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; background: aliceblue; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td align="center" class="container" style="display: block; padding: 24px 0; max-width: 90%; margin: 0 auto;">
                      <div class="logo-wrap">
                          <!-- Change logo as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 159px; height: 73px; object-fit: cover;" />
                          <!-- Change logo as per your requirements -->
                      </div>
                  </td>
              </tr>
              <!-- header end-->
              <tr>
                  <td style="text-align: center;">
                      <div class="container" style="max-width: 78%; margin: 0 auto 30px;">
                          <!-- Change image src as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Anniversary/banner.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
                  </td>
              </tr>
              <tr>
                  <td align="center" style="padding: 37px 0 47px; background: #FF5252;">
                      <div class="container" style="max-width: 78%; margin: 0 auto;">
                          <h2 class="title" style="margin: 0 0 10px; font-family: 'Jost', Arial, sans-serif; font-size: 50px; font-weight: 600; line-height: 65px; text-align: center; color: #FFFFFF; text-transform: none;">Happy Anniversary</h2>

                          <p class="date" style="margin: 0 0 15px; font-family: 'Jost', Arial, sans-serif; font-size: 30px; font-weight: 400; color: #FFFFFF; line-height: 43px; text-align: center; ">Emily</p>

                          <p class="wishes-txt" style="margin: 0; text-transform: none; font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 35px; text-align: center; color: #FFFFFF; "><span style="font-size:16px;">Celebrate your special day with a little something from us — an exclusive coupon code valid just for today. It’s our way of saying thanks for being part of our family.</span></p>
                      </div>
                  </td>
              </tr>
              <tr>
                  <td align="center" class="offer-wrap" style="padding: 50px 0;">
                      <div class="container" style="max-width: 78%; margin: 0 auto;">
                          <h3 class="offer-title" style="margin: 0 0 14px; font-family: 'Jost', Arial, sans-serif; font-size: 45px; font-weight: 300; line-height: 53px; text-align: center; ">Get <span style="font-style: italic; color: #FF4747; font-weight: 600;">30% </span>Off<br />
  			just for today!</h3>

                          <h4 class="code" style="margin: 0 0 20px; text-transform: uppercase; color: #545454; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 24px; text-align: center; ">USE CODE AT CHECKOUT: <strong>HAPPYANNIVERSARY</strong></h4>

                          <p style="margin: 0 0 40px; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 29px; color: #545454; text-align: center; text-transform: none;">Code valid only till February 15th 11:59pm</p>
                          <a class="cta" href="#" style="display:inline-block; background-color: #FF5252; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400;line-height: 28px;text-align: center; color: #FFFFFF !important; text-transform: uppercase; border-radius: 25px; text-decoration: none; max-width: 233px; padding: 10px 63px;">shop now</a></div>
                  </td>
              </tr>
              <!-- footer start-->
              <tr>
                  <td align="center" style="background: #FF5252;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin: 0 auto;">
                          <tbody>
                              <tr>
                                  <td>
                                      <p class="footer-desc" style="color: #FFFFFF; font-size: 18px; font-weight: 400; line-height: 35px; text-align: center; margin: 43px auto 25px;  max-width: 78%;">For assistance, connect with us on social media or reach out to our support team at <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #ffffff;" title="support@example.com">support@example.com</a></p>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="border-top: 1px solid #FFFFFF; padding: 25px 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 26px; height: 26px;">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 0 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 26px; height: 26px;">
                                                          <!-- Change image src as per your requirements --><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 0 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 26px; height: 26px;">
                                                          <!-- Change image src as per your requirements --><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/a971a978e8544cbfb0a0f3456c21463e.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
      <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
     </body>
    	</html>
  ```
</Accordion>

## Informative Email Template

A neutral, content-focused HTML template designed to communicate important updates without a promotional tone. Suitable for compliance notices, product changes, or business-wide announcements.

<Image align="center" alt="Sample Informative Email Template" border={true} caption="Sample Informative Email Template" src="https://files.readme.io/b929cb18516c6bd42b772107850b0b63c010e4a85df006fe6f215042d50a8910-Informative_Email_Template_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Announce policy updates or changes in terms of service.
  * Notify users about new features, UI enhancements, or release rollouts.
  * Share account-related communications such as billing reminders or operational changes.
  * Ideal for transactional or compliance-driven engagement.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Informative</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 480px) {             .container {max-width: 100% !important;}             .main {max-width: 90% !important;}             .faq-sec {padding: 10px !important;}             .product-sec{padding: 25px !important; text-align: justify !important;}             .border{width: 25% !important;}         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="background: rgb(221, 221, 221); font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <!-- Change Theme -->
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="text-align: center; vertical-align: middle; padding: 20px">
                      <!-- Change Logo Image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" />
                      <!-- Change Logo Image src as per your requirements -->
                  </td>
              </tr>
              <!-- header end-->
              <!-- Banner Image -->
              <tr>
                  <td style="padding:0px 10px;"><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/informative/banner.png" style="width: 100%; height: 100%; max-height: 361px; object-fit: cover;" /></td>
              </tr>
              <!-- Banner Image -->
              <!-- Product section -->
              <tr>
                  <td class="product-sec" style="background: #DBCBB0; padding: 32px 46px; text-align: center; margin: 0px 10px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="text-align: center;">
                                      <h2 style="text-transform: none;font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; margin: 0 auto;">QUARTERLY UPDATES</h2>

                                      <div style="border-bottom: 1px solid #252525; width: 80px; display: block; margin: 10px auto;"> </div>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin: 10px 0">
                                          <tbody>
                                              <tr>
                                                  <td>
                                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="padding: 10px; width: 100%;">
                                                          <tbody>
                                                              <tr>
                                                                  <td>
                                                                      <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 24px; text-align: center; ">Stay in the loop with the latest updates from our company. From exciting launches to impactful milestones, here’s everything you need to know about how we’ve grown and evolved over the
                                                                          last quarter.</p>
                                                                  </td>
                                                              </tr>
                                                          </tbody>
                                                      </table>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- product section -->
              <!-- Information Section -->
              <tr>
                  <td class="information-sec" style="background: #DBCBB0; padding: 15px; text-align: center; margin: 20px 10px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="text-align: center;">
                                      <h2 style="text-transform: none;font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; margin: 0 auto;">LATEST NEWS</h2>

                                      <div style="border-bottom: 1px solid #252525; width: 80px; display: block; margin: 10px auto;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Information Section -->
              <!-- Product Updates Section -->
              <tr>
                  <td class="information-sec" colspan="2" style="text-align: center; margin: 20px 10px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin-bottom: 15px;; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 65%; background: #ffffff;  text-align: left; vertical-align: middle;">
                                      <div style="padding:40px 16px; background: #DBCBB0;">
                                          <h2 style="text-transform: none; margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525;">LEADERSHIP ANNOUNCEMENT</h2>

                                          <div style="background: #252525; width: 60px;height: 1px; display: block; margin: 6px 0px 10px 0px"> </div>

                                          <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; ">We’re excited to welcome [New CEO Name] as our new CEO, now set to lead us into an exciting new chapter.</p>
                                      </div>
                                  </td>
                                  <td style="width: 35%; text-align: right; vertical-align: middle;">
                                      <div class="look-img"><img alt="look" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/informative/product1.png" style="width:100%; height: 100%; object-fit: contain;" /></div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Product Updates Section -->
              <!-- Policy Changes Section -->
              <tr>
                  <td class="information-sec" colspan="2" style="text-align: center; margin: 20px 10px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin-bottom: 15px; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 35%; text-align: right; vertical-align: middle;">
                                      <div class="look-img"><img alt="look" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/informative/product2.png" style="width:100%; height: 100%; object-fit: contain;" /></div>
                                  </td>
                                  <td style="width: 65%; background: #ffffff;  text-align: left; vertical-align: middle;">
                                      <div style="padding:40px 16px; background: #DBCBB0;">
                                          <h2 style="text-transform: none; margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525;">PRODUCT LAUNCH</h2>

                                          <div style="background: #252525; width: 60px;height: 1px; width: 60px; display: block; margin: 6px 0px 10px 0px"> </div>

                                          <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; ">We’re thrilled to introduce [Product Name], designed to make your experience even better.</p>
                                      </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Policy Changes Section -->
              <!-- Periodic Updates Section -->
              <tr>
                  <td class="information-sec" colspan="2" style="text-align: center; margin: 20px 10px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin-bottom: 15px; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 65%; background: #ffffff;  text-align: left; vertical-align: middle;">
                                      <div style="padding:40px 16px; background: #DBCBB0;">
                                          <h2 style="text-transform: none; margin: 0;font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525;">NEW MILESTONE</h2>

                                          <div style="background: #252525; width: 60px;height: 1px; display: block; margin: 6px 0px 10px 0px"> </div>

                                          <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; ">We’ve hit an incredible milestone — our company now serves over 2 million customers worldwide!</p>
                                      </div>
                                  </td>
                                  <td style="width: 35%; text-align: right; vertical-align: middle;">
                                      <div class="look-img"><img alt="look" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/informative/product3.png" style="width:100%; height: 100%; object-fit: contain;" /></div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Periodic Updates Section -->
              <!-- Shop Now-->
              <!-- Shop Now-->
              <tr>
                  <td>
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 100%; text-align: center; vertical-align: middle;">
                                      <a display_text_og="READ%20MORE" href="#" href_og="%23" style="font-family: Jost, Arial, sans-serif; font-size: 16px; font-weight: 400; text-transform: none; line-height: 24px; text-decoration: none; background: rgb(154, 119, 89); padding: 4px 34px; display: inline-block; text-align: center; max-width: 167px; color: rgb(255, 255, 255) !important;">READ MORE</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Footer Section -->
              <tr>
                  <td align="center" colspan="2" style="padding-top: 50px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width:100%; background: #543F2D; padding: 25px 0 25px;">
                          <tbody>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <!-- Add Links -->
                                          <!-- Download Android Section -->
                                          <tbody>
                                              <tr>
                                                  <td class="border" style="width:36%;">
                                                      <div style="display: block; border:1px solid #DBCBB0;"> </div>
                                                  </td>
                                                  <td style="padding: 10px 10px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 10px 10px; display: inline-block; ">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 10px 10px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/094eeb00e51f41b0a1ff5d845e6d3b2c.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td class="border" style="width:36%;">
                                                      <div style="display: block; border:1px solid #DBCBB0;"> </div>
                                                  </td>
                                              </tr>
                                              <!-- Download Android Section -->
                                              <!-- Add Links -->
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Footer Section -->
              <!-- FAQS start-->
              <tr>
                  <td align="center" colspan="2" style="margin-top: 10px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width:100%; background: #543F2D; padding: 25px 0 25px;">
                          <tbody>
                              <tr>
                                  <td style="text-align: center;">
                                      <h2 style="text-transform: none;font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; margin: 0 auto; color:#ffffff">FAQ&#39;s</h2>

                                      <div style="border-bottom: 1px solid #DBCBB0; width: 80px; display: block; margin: 10px auto;"> </div>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="faq-sec" style="padding: 10px 100px;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="background: #DBCBB0; padding: 10px; margin-bottom: 5px; display: block;">
                                                      <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: left; ">FAQ 1</p>

                                                      <p style="margin: 0; color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; "><strong data-renderer-mark="true">What does the change in leadership mean for customers?</strong></p>

                                                      <p style="margin: 0; color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; ">The new CEO brings fresh perspectives, ensuring a better experience for all customers</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="background: #DBCBB0; padding: 10px; margin-bottom: 5px; display: block;">
                                                      <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: left; ">FAQ 2</p>

                                                      <p style="margin: 0;  color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; "><strong data-renderer-mark="true">What makes [New Product Name] unique?</strong></p>

                                                      <p style="margin: 0; color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; ">[New Product Name] offers cutting-edge features designed to streamline your experience. Learn more about it on our website.</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="background: #DBCBB0; padding: 10px; margin-bottom: 5px; display: block;">
                                                      <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: left; ">FAQ 3</p>

                                                      <p style="margin: 0; color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; "><strong data-renderer-mark="true">How can I try out the new product?</strong></p>

                                                      <p style="margin: 0; color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; ">You can explore [New Product Name] by visiting our website or contacting our team for a demo.</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="background: #DBCBB0; padding: 10px; display: block;">
                                                      <p style="margin: 0; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: left; ">FAQ 4</p>

                                                      <p style="margin: 0; color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; "><strong data-renderer-mark="true">How can I learn more about these updates?</strong></p>

                                                      <p style="margin: 0; color: #494949; font-family: 'Jost', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: left; ">Simply click “READ MORE” to dive deeper into each update.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- FAQS end-->
              <tr>
                  <td style="padding: 20px 0;">
                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #494949;">To opt out of promotional emails like this,
                          <a href="#" style="color:#543F2D;font-weight:bold;text-decoration:none;">unsubscribe here</a>
                      </p>
                  </td>
              </tr>
          </tbody>
      </table>
      <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
  </body>

  </html>
  ```
</Accordion>

## Loyalty Points Update Template

These templates are designed to keep users informed about changes in their loyalty point balance, including newly earned and expiring points. By providing timely, personalized updates, this template plays a key role in driving continued engagement and redemption.

<Image align="center" alt="Sample Loyalty Points Expiry & Loyalty Points Balance Template" border={true} caption="Sample Loyalty Points Expiry & Loyalty Points Balance Template" src="https://files.readme.io/a457c4956a48241012937ce59ab0e2d90559fd644fe14d7326d0fd8d345dcf6d-Loyalty_Points_Update_HTML.png" width="75% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Notify users when new points have been added to their account.
  * Alert users about points that are about to expire soon.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html Loyalty Point Expiry
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Loyalty Point Expiry</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }             .loyalty-sec{                 padding: 30px !important;             }             .footer-content{                 padding: 0px 30px !important;             }             .expiry-para{                 padding: 10px 20px !important;             }             .main-heading{                 font-size: 30px !important;                 line-height: 40px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #F0EEF6; padding: 30px 0px 0px;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="background: #ffffff; text-align: center; vertical-align: middle; padding: 20px; margin: 0px 30px; display: block;">
                      <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /></td>
              </tr>
              <!-- header end-->
              <!-- Loyalty Point section -->
              <tr>
                  <td class="loyalty-sec" style="background: #ffffff; padding: 30px; text-align: center; border-top: 0.5px solid #979797; margin: 0px 30px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="text-align: center;">
                                      <h2 class="main-heading" style="text-transform: uppercase;font-family: 'Jost', Arial, sans-serif; font-size: 40px; font-weight: 300; line-height: 50px; margin: 0 auto; color:#000000;">YOUR POINTS WILL EXPIRE SOON!</h2>

                                      <p class="expiry-para" style="padding: 0px 80px; text-transform: none; color: #4f4f4f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; ">You have 150 loyalty points that are set to expire on February 15 2025. Shop now to redeem them and save big!</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Loyalty Point section -->
              <!-- Information Section -->
              <tr>
                  <td class="information-sec" style="border-top:3px solid #1DBF73;text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td><img alt="look" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Loyalty-Exp/loyalty.png" style="width:100%; height: 100%; object-fit: contain;" /></td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td style="background-color: #1DBF73; padding: 10px 30px; vertical-align: middle; text-align: left;">
                      <a href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; text-transform: uppercase; line-height: 28px; color: #ffffff !important; text-decoration: none; display: inline-block; text-align: left; width: 100%;">Redeem Now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Loyalty-Exp/Arrow.png" style="float:right; padding-top: 5px;" /></a>
                  </td>
              </tr>
              <!-- Information Section -->
              <!-- footer start-->
              <tr>
                  <td align="center" colspan="2">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width:100%; background: #ffffff; padding: 25px 0 25px;">
                          <tbody>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/7c0f383a34174b419048c105abef1c6d.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block; ">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9e433bfc71464f51ac6bf991cc15c61e.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/84960566b3bd48c49d86b17263d4cee8.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 100px">
                                                      <p style="color: #4f4f4f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin-bottom: 0px;">For assistance, connect with us on social media or reach out to our support team at
                                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                                      </p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 100px">
                                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">This is a system-generated email. Please do not reply.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
  </html>
  ```
  ```html Loyalty Points Balance
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Loyalty Point</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }             .loyalty-sec{                 padding: 30px !important;             }             .footer-content{                 padding: 0px 30px !important;             }             .main-heading{                 font-size: 30px !important;                 line-height: 40px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #F0EEF6; padding: 30px;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="background: #ffffff; text-align: center; vertical-align: middle; padding: 20px">
                      <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /></td>
              </tr>
              <!-- header end-->
              <!-- Loyalty Point section -->
              <tr>
                  <td class="loyalty-sec" style="background: #ffffff; padding: 30px 100px; text-align: center; border-top: 0.5px solid #979797;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="text-align: center;">
                                      <h2 class="main-heading" style="text-transform: uppercase;font-family: 'Jost', Arial, sans-serif; font-size: 40px; font-weight: 300; line-height: 57px; margin: 0 auto; color:#000000;">YOUR POINTS BALANCE</h2>

                                      <p style="margin-bottom: 20px; text-transform: none; color: #4f4f4f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; ">Here is your current loyalty points balance. Shop now to redeem them and save big!</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Loyalty Point section -->
              <!-- Information Section -->
              <tr>
                  <td class="information-sec" style="background: #1DBF73; padding: 15px; text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td>
                                      <h3 style="margin: 0px; font-style:italic;text-transform: none; color: #ffffff; font-family: 'Jost', Arial, sans-serif; font-size: 40px; font-weight: 400; line-height: 57px; text-align: center; ">150</h3>

                                      <p style="margin: 0px; text-transform: none; color: #ffffff; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 24px; text-align: center; ">Current Points Balance</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td class="information-sec" style="background: #ffffff; border:1px solid #1DBF73; margin-bottom: 20px; padding: 10px 25px; text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <h4 class="p-title" style="margin:0px; text-transform: uppercase; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 300; line-height: 20px; color: #393939; text-align: left;">Expiry Date</h4>
                                  </td>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 16px;font-weight: 500; line-height: 23px; text-align: right;">10/09/2024</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td style="background: #ffffff; padding: 20px 0;"> </td>
              </tr>
              <tr>
                  <td class="information-sec" style="background: #ffffff; border-top:0.5px solid #979797; padding: 40px 25px; text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 100%; text-align: center; vertical-align: middle;">
                                      <a display_text_og="REDEEM%20NOW" href="#" href_og="%23" style="font-family: Jost, Arial, sans-serif; font-size: 20px; font-weight: 400; text-transform: uppercase; line-height: 28px; text-decoration: none; background: rgb(29, 191, 115); padding: 9px 30px; display: inline-block; text-align: center; max-width: 182px; color: rgb(255, 255, 255) !important;">REDEEM NOW</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Information Section -->
              <!-- footer start-->
              <tr>
                  <td align="center" colspan="2">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background: #F0EEF6; padding: 25px 0 0px;">
                          <tbody>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/7c0f383a34174b419048c105abef1c6d.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block; ">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9e433bfc71464f51ac6bf991cc15c61e.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/84960566b3bd48c49d86b17263d4cee8.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 50px">
                                                      <p style="text-transform: none; color: #4f4f4f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin-bottom: 0px;">For assistance, connect with us on social media or reach out to our support team at
                                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                                      </p>

                                                      <p style="text-transform: none; color: #4f4f4f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin-bottom: 0px;"> </p>

                                                      <p style="text-transform: none; color: #4f4f4f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin-bottom: 0px;">This is a system-generated email. Please do not reply.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Newsletter Template

This recurring email template is used to share curated content such as blogs, product updates, or brand stories.

<Image align="center" alt="Sample Newstter Template" border={true} caption="Sample Newstter Template" src="https://files.readme.io/c9c1ca33c322799d0618933c8800ba0eef3fd29039ee56a4db8544d829feeee1-Newsletter_Template_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Keep users informed and engaged by providing valuable content in a consistent format.
  * Ideal for sharing thought leadership articles, community highlights, or monthly wrap-ups without a sales-heavy tone.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Newsletter</title>
      <link href="https://fonts.googleapis.com" rel="preconnect" />
      <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
      <link href="https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,100..900;1,100..900&amp;display=swap" rel="stylesheet" />
      <style type="text/css">
          /* *{             margin: 0;             padding: 0;         } */                  @media screen and (max-width: 480px) {             .main {                 max-width: 100% !important;             }             .container{                 max-width: 90% !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; cursor: auto;">
      <table align="center" cellpadding="0" cellspacing="0" style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;" width="100%">
          <!-- Main Product Section -->
          <tbody>
              <tr>
                  <td>
                      <table align="center" cellpadding="0" cellspacing="0" class="container" style="max-width: 88%; margin: 38px auto;" width="100%">
                          <!-- Logo -->
                          <tbody>
                              <tr>
                                  <td align="center" style="padding: 15px 0; background-color: #FFFFFF;"><img alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="max-width: 159px; max-height: 73px;" /></td>
                              </tr>
                              <!-- Banner Image -->
                              <tr>
                                  <td align="center" style="background-color: #FFFFFF;"><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/banner.png" style="max-height: 307px; width: 100%; height: auto; object-fit: cover;" /></td>
                              </tr>
                              <!-- Banner Info -->
                              <tr>
                                  <td style="padding: 32px 50px 15px; text-align: center; background-color: #FFFFFF;">
                                      <h1 style="font-size: 36px; font-weight: 400; line-height: 45px; color: #1E1E1E; text-transform: uppercase; margin-bottom: 10px; margin-top: 0;">WELCOME TO OUR NEWSLETTER</h1>

                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 24px; margin-top: 0;">Here’s what we’ve been up to this month! We’ve packed this newsletter with handy resources, updates on upcoming events, collaboration opportunities, and a whole lot more.</p>

                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="display: inline-block; padding: 8px 70px; font-size: 12px; font-weight: 400; line-height: 24px; color: rgb(255, 255, 255); text-decoration: none; text-transform: uppercase; background-color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                  </td>
                              </tr>
                              <!-- Product List -->
                              <tr>
                                  <td style="padding-top: 33px;">
                                      <h3 style=" margin-top: 0; text-align: center; font-size: 36px; font-weight: 400; line-height: 45px; text-transform: uppercase; padding: 30px 0 33px; margin: 0;background: #FFFFFF;">What&#39;s NEW</h3>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <table cellpadding="0" cellspacing="0" style="border-collapse: collapse;" width="100%">
                                          <!-- Product 1 -->
                                          <tbody>
                                              <tr>
                                                  <td style="width: 50%;"><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-1.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">New launches</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">Explore newly launched products from our collection. Click below to see what’s new. Use SAVE5 for a flat 5% off on any of these products.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                              </tr>
                                              <!-- Product 2 -->
                                              <tr>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">EVENTS</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">We&#39;ve organized three community meetups in January. Click below to see pictures and videos of these events.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                                  <td style="width: 50%;"><img alt="product-2" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-2.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                              </tr>
                                              <!-- Product 3 -->
                                              <tr>
                                                  <td style="width: 50%;"><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-3.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">Webinars</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">We’ve conducted 12+ webinars in January, attended by 1500+ members. Click below for a summary of insights shared.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                              </tr>
                                              <!-- Product 4 -->
                                              <tr>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">IN spotlight</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">In January, we had a new star product that won the hearts of our customers! Click below to read more.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                                  <td style="width: 50%;"><img alt="product-2" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-4.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                              </tr>
                                              <!-- Product 5 -->
                                              <tr>
                                                  <td style="width: 50%;"><img alt="product-2" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-5.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">SUCCESSES</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">We’re always happy to get feedback from our customers. Click below to read stories from happy customers.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                              </tr>
                                              <!-- Product 6 -->
                                              <tr>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">TOOLS</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">Here are some of the top productivity tools to streamline your workflow and save time. Click below to read more.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                                  <td style="width: 50%;"><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-6.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                              </tr>
                                              <!-- Product 7 -->
                                              <tr>
                                                  <td style="width: 50%;"><img alt="product-2" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-7.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">Latest trends</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">Stay ahead with our exclusive deep dive into the top trends shaping this industry. Click below to read more.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                              </tr>
                                              <!-- Product 8 -->
                                              <tr>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">trips & tricks</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">Click below for some handy tips and tricks shared by our community members, curated to help you level up.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                                  <td style="width: 50%;"><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-8.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                              </tr>
                                              <!-- Product 9 -->
                                              <tr>
                                                  <td style="width: 50%;"><img alt="product-2" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-9.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">resources</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">Need guidance? Browse our comprehensive library of articles, product guides, and tutorials. Click below to explore.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                              </tr>
                                              <!-- Product 10 -->
                                              <tr>
                                                  <td style="width: 50%; background-color: #FFFFFF; padding: 25px 30px;">
                                                      <h3 style=" margin-top: 0; font-size: 20px; font-weight: 400; line-height: 52px; color: #0D0D0D; text-transform: uppercase; margin-bottom: 5px;">next up!</h3>

                                                      <p style="margin-top:0; font-size: 14px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none; margin-bottom: 5px;">We’re hard at work to bring you the best! Here’s a preview of what we’re launching soon. Click below to read more.</p>

                                                      <a display_text_og="LEARN%20MORE" href="#" href_og="%23" style="text-transform: uppercase; font-size: 16px; font-weight: 300; line-height: 37.75px; text-decoration: none; color: rgb(28, 131, 138) !important;">LEARN MORE</a>
                                                  </td>
                                                  <td style="width: 50%;"><img alt="product-2" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Newsletter/product-10.png" style="max-width: 264px; height: auto; display: block;" /></td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <!-- Footer Section -->
                              <tr>
                                  <td style="padding: 45px 0 0; background-color: #F5F5F5;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="max-width: 80%; margin: 0 auto;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-bottom: 21px;">For assistance, connect with us on social media or reach out to our support team at
                                                      <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td>
                                                      <table align="center" cellpadding="0" cellspacing="0" style="padding: 0; margin-bottom: 29px; text-align: center;" width="100%">
                                                          <tbody>
                                                              <tr>
                                                                  <td style="display: inline-block; margin: 0 5px;">
                                                                      <a href="#" style="font-size: 14px; font-weight: 400; color: #1E1E1E !important; text-decoration: none;">Privacy</a>
                                                                  </td>
                                                                  <td style="display: inline-block; margin: 0 5px;">
                                                                      <a href="#" style="font-size: 14px; font-weight: 400; color: #1E1E1E !important; text-decoration: none;">Account</a>
                                                                  </td>
                                                              </tr>
                                                          </tbody>
                                                      </table>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                                          <tbody>
                                                              <tr>
                                                                  <td style="display: inline-block; padding: 5px 39px; border: 1px solid #919191;">
                                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 24px; height: 24px;"><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/37cf7640cb754509b9c3383d11c4d8c2.png" style="width: 100%; height: 100%;" /></a>
                                                                  </td>
                                                                  <td style="display: inline-block; padding: 5px 39px; border: 1px solid #919191;">
                                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 24px; height: 24px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fae961ed063e42448b3c5e8daab1e691.png" style="width: 100%; height: 100%;" /></a>
                                                                  </td>
                                                                  <td style="display: inline-block; padding: 5px 39px; border: 1px solid #919191;">
                                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 24px; height: 24px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/2ccc2bf548f94ba5b2417039082cd06c.png" style="width: 100%; height: 100%;" /></a>
                                                                  </td>
                                                              </tr>
                                                          </tbody>
                                                      </table>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top: 21px;">
                                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #919191;">To opt out of promotional emails like this,
                                                          <a href="#" style="color:#1C838A;text-decoration:none;font-weight:bold;">unsubscribe here</a>
                                                      </p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Order Lifecycle Updates Template

A set of transactional templates that provide customers with timely updates across the whole order journey, from placing the order to final delivery.

<Tabs>
  <Tab title="Order Confirmed">
    <Image align="center" border={true} src="https://files.readme.io/0b3a7b4376e461cb0bf467bdfeb6c97e111f4b9c80eaa10fb7cb17e176356aaf-Order_Confirmed_HTML.png" width="35% " />
  </Tab>

  <Tab title="Order Shipped">
    <Image align="center" border={true} src="https://files.readme.io/f1785a9a322e55a79f15e21844206cfb95dd3eea5420a0d5530f96320f5cea1a-Order_Shipped_HTML.png" width="40% " />
  </Tab>

  <Tab title="Order Delivered">
    <Image align="center" border={true} src="https://files.readme.io/b5f7eee1c562f0d22e3694d0d6cf78c51240090d840a307bd2ca10019e66ecd9-Order_Delivered_HTML.png" width="40% " />
  </Tab>
</Tabs>

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  Keeps customers informed and reassured throughout their post-purchase experience. This includes order confirmation, shipment tracking, and successful delivery notifications to reduce uncertainty and improve satisfaction.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html Order Confirmed
  <!DOCTYPE html>
  <html lang="en">

  <head>
      <title></title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }             .box-table{                 margin: 10px 15px !important;                 padding: 20px 0px !important;             }             .imgConfirmation{                 width: 50px !important;             }             .content-sec {                 padding: 0px 10px !important;                 margin-top: 10px !important;             }             .footer-content{                 padding: 0px 10px !important;             }             .expiry-para{                 padding: 0px 10px !important;                 margin: 10px 0px !important;             }             .main-heading{                 font-size: 24px !important;                 line-height: 30px !important;                 padding: 0px 10px !important;             }             .shipping{                 padding: 0px 20px !important;             }             .track-btn{                 max-width: auto !important;                 width: auto !important;                 font-size: 16px !important;                 line-height: 24px !important;                 padding: 5px 25px !important;             }             .order-detail {                 font-size: 16px !important;                 line-height: 20px !important;                 margin-bottom: 0px !important;             }             .quantity {                 font-size: 10px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #F0EEF6; padding: 30px 0px 0px;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="text-align: center; vertical-align: middle; padding: 20px; margin: 0px 30px; display: block;">
                      <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /></td>
              </tr>
              <!-- header end-->
              <tr>
                  <td>
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="box-table" role="presentation" style="padding: 50px 0px;box-shadow: 0px 1px 12px 0px #0000001A;margin: 0px 30px; display: block; background-color: #ffffff;;">
                          <!-- Content section -->
                          <tbody>
                              <tr>
                                  <td class="content-sec" style="background: #ffffff; padding: 0px 20px; text-align: center; display: block;margin-top: 30px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <h4 class="main-heading" style="text-transform: none;font-family: 'Jost', Arial, sans-serif; font-size: 26px; font-weight: 600; line-height: 37px; margin: 0 auto; color:#40403B;">Order confirmed</h4>

                                                      <h4 class="main-heading" style="text-transform: none;font-family: 'Jost', Arial, sans-serif; font-size: 26px; font-weight: 400; line-height: 37px; margin: 0 auto; color:#40403B;">We hope you enjoyed shopping with us</h4>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="border-bottom: 1px solid #FFC645; background: #ffffff; padding: 0px 80px 20px; text-align: center; display: block;margin-top: 0px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <p class="expiry-para" style="text-transform: none; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; ">We’re now working on getting your order ready.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="background: #ffffff; padding: 0px 20px; text-align: center; display: block;margin-top: 30px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <h2 class="main-heading" style="text-transform: none;font-family: 'Jost', Arial, sans-serif; font-size: 26px; font-weight: 600; line-height: 37px; margin: 0 auto; color:#40403B;">Estimated Delivery on <strong data-renderer-mark="true">Feb 15 2025</strong></h2>

                                                      <p class="expiry-para" style="margin-top: 10px;text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28px; text-align: center; ">Your order ID is <span style="font-weight: 600;">898774</span></p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="background: #ffffff; padding: 0px 80px; text-align: center; display: block;margin-top: 0px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <p class="expiry-para" style="text-transform: none; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; ">You’ll receive another email with tracking details once your order is shipped. Click below to view and make changes to your order.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="width: 100%; text-align: center; vertical-align: middle;">
                                                      <a class="track-btn" display_text_og="View%20and%20Manage%20Order" href="#" href_og="%23" style="font-family: Jost, Arial, sans-serif; font-size: 20px; font-weight: 400; text-transform: none; line-height: 28px; text-decoration: none; background: rgb(255, 198, 69); padding: 12px 34px; display: inline-block; text-align: center; max-width: 80%; width: 100%; color: rgb(30, 30, 30) !important;">View and Manage Order</a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="border-bottom: 1px solid #FFC645; background: #ffffff; padding: 0px 20px; text-align: center; display: block;margin-top: 30px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <h4 class="expiry-para" style="margin: 10px 0px;text-transform: none; color: #40403B; font-family: 'Jost', Arial, sans-serif; font-size: 22px; font-weight: 600; line-height: 37px; text-align: left; ">Items in Order</h4>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="background: #ffffff; padding: 0px 20px; text-align: center; display: block;margin-top: 30px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="width: 30%; vertical-align: top;"><img alt="look" class="imgConfirmation" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-placed/product.png" style="width:128px; height: 121px; object-fit: contain;" /></td>
                                                  <td style="width: 60%; vertical-align: top;">
                                                      <h4 class="order-detail" style="margin: 0px 0px 5px; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 500; line-height: 28px;text-align: left;">Nike sneakers</h4>

                                                      <p style="margin:0; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px;font-weight: 400; line-height: 22px; text-align: left;">Color: Black</p>

                                                      <p style="margin:0; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px;font-weight: 400; line-height: 22px; text-align: left;">Size: US M 10</p>

                                                      <h4 class="order-detail" style="margin: 0px 0px 10px; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28px;text-align: left;">$4000</h4>
                                                  </td>
                                                  <td style="width: 10%; vertical-align: top;">
                                                      <p class="quantity" style="margin: 10px 0px;text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 22px; text-align: left; ">QTY 1</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="border-bottom: 1px solid #FFC645; background: #ffffff; padding: 0px 20px; text-align: center; display: block;margin-top: 10px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="text-align: center;">
                                                      <h4 class="expiry-para" style="margin: 10px 0px;text-transform: none; color: #40403B; font-family: 'Jost', Arial, sans-serif; font-size: 22px; font-weight: 600; line-height: 37px; text-align: left; ">Billing Summary</h4>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="border-bottom: 0.5px solid #969696; background: #ffffff; margin: 0px 20px; text-align: center; display: block;margin-top: 10px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <p class="expiry-para" style="margin: 10px 0px;text-transform: none; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: left; ">Sub total</p>
                                                  </td>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <h4 style="margin: 10px 0px; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28px;text-align: right;">$4000</h4>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="border-bottom: 0.5px solid #969696; background: #ffffff; margin: 0px 20px; text-align: center; display: block;margin-top: 10px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <p class="expiry-para" style="margin: 10px 0px;text-transform: none; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: left; ">Tax</p>
                                                  </td>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <h4 style="margin: 10px 0px; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28px;text-align: right;">$200</h4>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="border-bottom: 1px dashed #000000; background: #ffffff; padding: 0px 20px; text-align: center; display: block;margin-top: 10px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="shipping" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <p style="margin: 10px 0px;text-transform: none; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: left; ">Shipping charges</p>
                                                  </td>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <h4 style="margin: 10px 0px; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28px;text-align: right;">$500</h4>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="content-sec" style="background: #ffffff; padding: 0px 20px; text-align: center; display: block;margin-top: 10px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="shipping" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                          <tbody>
                                              <tr>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <p class="expiry-para" style="margin: 10px 0px;text-transform: uppercase; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: left; ">Total</p>
                                                  </td>
                                                  <td style="width: 50%; vertical-align: middle;">
                                                      <h4 style="margin: 10px 0px; text-transform: none; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28px;text-align: right;">$4700</h4>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <!-- Content Point section -->
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer start-->
              <tr>
                  <td align="center" colspan="2">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="box-table" role="presentation" style="box-shadow: 0px 1px 12px 0px #0000001A; margin: 30px 30px 30px; display: block; background: #ffffff; padding: 25px 0 25px;">
                          <tbody>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 100px">
                                                      <p style="text-transform: none; color: #6f6f6f; font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center;">For assistance, connect with us on social media or reach out to our support team at
                                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                                      </p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/be621c25343741b1ac5640833e3b34f7.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block; ">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/53caa3fd24c5413a91a6db136577fcf7.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fa216fecba6741dea1d9d5452d498603.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="content-sec" style="border-top: 1px solid #FFC645; background: #ffffff; padding: 20px 20px 0px; text-align: center; display: block;margin-top: 10px;">
                                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                                                          <tbody>
                                                              <tr>
                                                                  <td style="padding: 0px 15px; display: inline-block;">
                                                                      <a href="#" style="vertical-align: middle;display: inline-block; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center;font-family: 'Jost', Arial, sans-serif;text-decoration: none;color:#1E1E1E; ">Privacy</a>
                                                                  </td>
                                                                  <td style="padding: 0px 15px; display: inline-block; ">
                                                                      <a href="#" style="vertical-align: middle;display: inline-block; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center;font-family: 'Jost', Arial, sans-serif;text-decoration: none;color:#1E1E1E;">Account</a>
                                                                  </td>
                                                              </tr>
                                                          </tbody>
                                                      </table>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="content-sec" style="border-top: 1px solid #FFC645; background: #ffffff; padding: 20px 20px 0px; text-align: center; display: block;margin-top: 20px;">
                                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">This is a system-generated email. Please do not reply.</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
  ```html Order Shipped
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Order Shipped</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }         @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }         @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }                  @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @font-face {             font-family: 'Poppins', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @media screen and (max-width: 480px) {             .container {                margin-bottom: 20px !important;             }                         .logo{                 width: 145px !important; height: 55px !important;             }             .cta{                 padding: 10px 25px !important; margin: 30px 0 !important; font-size: 16px !important; line-height: 20px !important;             }             .content-wrap{                 max-width: 90% !important;             }             .title{                 font-size: 22px !important; line-height: 28px !important;             }             .border-line{                 width: 40% !important;             }             .desc{                 font-size: 12px !important; line-height: 18px !important; margin: 0 0 30px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td align="center" style="display: block; padding: 12px 0; max-width: 90%; margin: 0 auto;">
                      <div class="logo-wrap">
                          <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 145px; height: 73px; object-fit: contain;" /></div>
                  </td>
              </tr>
              <!-- header end-->
              <tr>
                  <td style="text-align: center;">
                      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 92%; margin: 0 auto 20px; background: #FFFFFF;" width="100%">
                          <tbody>
                              <tr>
                                  <td align="center">
                                      <div class="content-wrap" style="margin: 0 auto; max-width: 85%;">
                                          <h2 class="title" style="font-family: 'Jost', Arial, sans-serif;font-size: 30px;font-weight: 500;line-height: 37px;text-align: center; color: #40403B; text-transform: none; margin: 43px 0 19px;">Order shipped</h2>

                                          <p class="desc" style="color: #6F6F6F;font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; margin: 0 auto; text-transform: none; max-width: 85%;">Great news — your order is on its way! You can track your order through the button below.</p>
                                      </div>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="center">
                                      <table border="0" cellpadding="0" cellspacing="0" class="order-table" role="presentation" style="max-width: 92.4%; margin: 60px auto 25px;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td align="center" style="width: 67px;vertical-align: top;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFFFFF; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 39px; height: 39px;"><img alt="icon-tick" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/icon-tick.png" style="width: 100%; height: 100%; object-fit: contain;" /></td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFC645; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFC645; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 39px; height: 39px;"><img alt="icon-tick" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/icon-tick.png" style="width: 100%; height: 100%; object-fit: contain;" /></td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #B2B2B2; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #B2B2B2; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 39px; height: 39px;"><img alt="icon-empty" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/icon-empty.png" style="width: 100%; height: 100%; object-fit: contain;" /></td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; border-top: 1px dashed #FFFFFF; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td align="center" colspan="3" style="vertical-align: top;">
                                                      <h3 class="o-title" style="margin: 10px 0 5px; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 22px; text-transform: none;">Order confirmed</h3>

                                                      <p class="o-date" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; margin: 0; line-height: 22px; color: #6F6F6F;">13-05-2024</p>
                                                  </td>
                                                  <td align="center" colspan="3" style="vertical-align: top;">
                                                      <h3 class="o-title" style="margin: 10px 0 5px; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 22px; text-transform: none;">Order shipped</h3>

                                                      <p class="o-date" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; margin: 0; line-height: 22px; color: #6F6F6F;">15-05-2024</p>
                                                  </td>
                                                  <td align="center" colspan="3" style="vertical-align: top;">
                                                      <h3 class="o-title" style="margin: 10px 0 5px; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 22px; text-transform: none;">Estimated delivery</h3>

                                                      <p class="o-date" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; margin: 0; line-height: 22px; color: #6F6F6F;">17-05-2024</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <table border="0" cellpadding="0" cellspacing="0" class="order-table" role="presentation" style="margin: 35px auto 0;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style=" text-align: left;">
                                                      <h2 class="sec-title" style="padding: 0 20px 10px;margin: 0 0 28px; font-family: 'Jost', Arial, sans-serif; font-size: 22px; font-weight: 600; line-height: 37px; text-transform: none; color: #40403B; border-bottom: 1px solid #FFC645;">Items in Order</h2>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td>
                                                      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style=" max-width: 95%; margin: 0 auto;" width="100%">
                                                          <tbody>
                                                              <tr>
                                                                  <td style="width: 25%; vertical-align: top;"><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-shipped/product-1.png" style="width: 100%; height: 100%; object-fit: cover; border: 1px solid #FFC645;"
                                                                      /></td>
                                                                  <td style="width: 65%; vertical-align: top; padding: 0 15px;">
                                                                      <h2 class="p-name" style="margin: 0 0 5px; text-transform: none; font-family: 'Jost',Arial, sans-serif; font-size: 20px; font-weight: 500; line-height: 28.9px; text-align: left; color: #000000;">Nike sneakers</h2>

                                                                      <p class="p-desc" style="margin: 0 0 5px; text-transform: none; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: left; color: #6F6F6F;">Color: Black</p>

                                                                      <p class="p-desc" style="margin: 0 0 5px; text-transform: none; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: left; color: #6F6F6F;">Size: US M 10</p>

                                                                      <p class="p-amt" style="margin: 0; font-family: 'Jost', Arial; font-size: 20px; font-weight: 400; line-height: 28.9px; text-align: left; color: #000000">$4000</p>
                                                                  </td>
                                                                  <td style="width: 10%; vertical-align: top;"><span class="qty" style="text-transform: uppercase; font-family: 'Jost', Arial, sans-serif; font-size: 16px;font-weight: 400; line-height: 22px; text-align: center; color: #000000;">Qty 1</span></td>
                                                              </tr>
                                                          </tbody>
                                                      </table>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <table border="0" cellpadding="0" cellspacing="0" class="order-table" role="presentation" style="margin: 35px auto 0;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style=" text-align: left;">
                                                      <h2 class="sec-title" style="padding: 0 20px 10px;margin: 0; font-family: 'Jost', Arial, sans-serif; font-size: 22px; font-weight: 600; line-height: 37px; text-transform: none; color: #40403B; border-bottom: 1px solid #FFC645;">Billing Summary</h2>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td>
                                                      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style=" max-width: 95%; margin: 0 auto;" width="100%">
                                                          <tbody>
                                                              <tr>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: left; border-bottom: 1px solid #969696;">
                                                                      <p class="p-subtotal" style="margin: 0; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; color: #6F6F6F; text-transform: none; padding: 16px 0;">Sub total</p>
                                                                  </td>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: right; border-bottom: 1px solid #969696;">
                                                                      <p class="p-amt" style="margin: 0; font-family: 'Jost', Arial, sans-serif;                                                     font-size: 20px; font-weight: 400; line-height: 28.9px; color: #000000; padding: 16px 0;">$4000</p>
                                                                  </td>
                                                              </tr>
                                                              <tr>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: left; border-bottom: 1px solid #969696;">
                                                                      <p class="p-subtotal" style="margin: 0; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; color: #6F6F6F; text-transform: none; padding: 16px 0;">Tax</p>
                                                                  </td>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: right; border-bottom: 1px solid #969696;">
                                                                      <p class="p-amt" style="margin: 0; font-family: 'Jost', Arial, sans-serif;                                                     font-size: 20px; font-weight: 400; line-height: 28.9px; color: #000000; padding: 16px 0;">$200</p>
                                                                  </td>
                                                              </tr>
                                                              <tr>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: left; border-bottom: 1px solid #000000;">
                                                                      <p class="p-subtotal" style="margin: 0; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; color: #6F6F6F; text-transform: none; padding: 16px 0;">Shipping charges</p>
                                                                  </td>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: right; border-bottom: 1px solid #000000;">
                                                                      <p class="p-amt" style="margin: 0; font-family: 'Jost', Arial, sans-serif;                                                     font-size: 20px; font-weight: 400; line-height: 28.9px; color: #000000; padding: 16px 0;">$500</p>
                                                                  </td>
                                                              </tr>
                                                              <tr>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: left;">
                                                                      <p class="p-subtotal" style="margin: 0; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; color: #6F6F6F; text-transform: uppercase; padding: 16px 0;">Total</p>
                                                                  </td>
                                                                  <td style="width: 50%; vertical-align: middle; text-align: right;">
                                                                      <p class="p-amt" style="margin: 0; font-family: 'Jost', Arial, sans-serif;                                                     font-size: 20px; font-weight: 400; line-height: 28.9px; color: #000000; padding: 16px 0;">$4700</p>
                                                                  </td>
                                                              </tr>
                                                          </tbody>
                                                      </table>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <div class="order-details" style="margin: 55px auto 68px; max-width: 80%;">
                                          <h3 class="o-title" style="margin: 0 0 10px; text-transform: none; color: #40403B; font-family: 'Jost'  Arial, sans-serif; font-size: 24px; font-weight: 600; line-height: 37px; text-align: center; ">Estimated Delivery on <strong data-renderer-mark="true">Feb 15 2025</strong></h3>

                                          <p class="o-desc" style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 28.9px; color: #6F6F6F;">Your Order ID is <span style="color: #000000; text-align: center;">898774</span></p>
                                          <button class="cta" style="background: #FFC645; border: 1px solid #FFC645; font-family: 'Jost', Arial, sans-serif; font-size: 20px;font-weight: 400;line-height: 28px;text-align: center; color: #1E1E1E !important; vertical-align: middle; width: 100%; padding: 12px; text-transform: none;">Track order</button>
                                      </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td style="text-align: center;">
                      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 92%; margin: 0 auto 30px; background: #FFFFFF;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <p style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #6F6F6F; text-align: center; max-width: 70%; margin: 30px auto 26px; text-transform: none;">For assistance, connect with us on social media or reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center; padding-bottom: 52px; border-bottom: 1px solid #FFC645;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/be621c25343741b1ac5640833e3b34f7.png" style="display: block; width: 34px; height: 34px;" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/53caa3fd24c5413a91a6db136577fcf7.png" style="display: block; width: 34px; height: 34px;" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fa216fecba6741dea1d9d5452d498603.png" style="display: block; width: 34px; height: 34px;" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: none;">This is a system-generated email. Please do not reply.</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
          </tbody>
      </table>
      <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
  </body>

  </html>
  ```
  ```html Order Delivered
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Order Delivered</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 600;         }                  @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\') format(\'woff\');             font-style: normal;             font-weight: 700;         }          @font-face {             font-family: \'Poppins\', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important; margin-bottom: 20px !important;             }                         .logo{                 width: 145px !important; height: 55px !important;             }             .cta{                 padding: 10px 25px !important; margin: 30px 0 !important; font-size: 16px !important; line-height: 20px !important;             }             .content-wrap{                 max-width: 90% !important;             }             .title{                 font-size: 22px !important; line-height: 28px !important;             }             .border-line{                 width: 40% !important;             }             .desc{                 font-size: 12px !important; line-height: 18px !important; margin: 0 0 30px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1198.0" data-new-gr-c-s-loaded="14.1198.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td align="center" style="display: block; padding: 12px 0; max-width: 90%; margin: 0 auto;">
                      <div class="logo-wrap">
                          <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 145px; height: 73px; object-fit: contain;" /></div>
                  </td>
              </tr>
              <!-- header end-->
              <tr>
                  <td style="text-align: center;">
                      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 92%; margin: 0 auto 20px; background: #FFFFFF; padding: 5px;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <!-- Change image src as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/banner.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                              </tr>
                              <tr>
                                  <td align="center">
                                      <div class="content-wrap" style="margin: 0 auto; max-width: 70%;">
                                          <h2 class="title" style="font-family: 'Jost', Arial, sans-serif;font-size: 30px;font-weight: 600;line-height: 37px;text-align: center; color: #40403B; text-transform: none; margin: 29px 0 21px;">Order delivered<span class="border-line" style="display: block; width: 72%; height: 1px; background: #D3A94D; margin: 25px auto 0;"> </span></h2>

                                          <p class="desc" style="color: #6F6F6F;font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; margin: 0 0 40px; text-transform: none;">We hope you love your new items! Continue shopping to discover more of your favorites.</p>
                                      </div>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="center">
                                      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 92.4%; margin: 0 auto;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td align="center" style="width: 67px;vertical-align: top;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFFFFF; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 39px; height: 39px;"><img alt="icon-tick" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/icon-tick.png" style="width: 100%; height: 100%; object-fit: contain;" /></td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFC645; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFC645; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 39px; height: 39px;"><img alt="icon-tick" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/icon-tick.png" style="width: 100%; height: 100%; object-fit: contain;" /></td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFC645; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; height: 1px; border-top: 1px dashed #FFC645; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                                  <td align="center" style="vertical-align: top; width: 39px; height: 39px;"><img alt="icon-tick" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/order-delivered/icon-tick.png" style="width: 100%; height: 100%; object-fit: contain;" /></td>
                                                  <td align="center" style="vertical-align: top; width: 67px;">
                                                      <div class="line" style="width: 100%; border-top: 1px dashed #FFFFFF; display: block; margin: 19px 0;"> </div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td align="center" colspan="3" style="vertical-align: top;">
                                                      <h3 class="o-title" style="margin: 10px 0 5px; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 22px; text-transform: none;">Order Confirmed</h3>

                                                      <p class="o-date" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; margin: 0; line-height: 22px; color: #6F6F6F;">13-05-2024</p>
                                                  </td>
                                                  <td align="center" colspan="3" style="vertical-align: top;">
                                                      <h3 class="o-title" style="margin: 10px 0 5px; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 22px; text-transform: none;">Order Shipped</h3>

                                                      <p class="o-date" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; margin: 0; line-height: 22px; color: #6F6F6F;">15-05-2024</p>
                                                  </td>
                                                  <td align="center" colspan="3" style="vertical-align: top;">
                                                      <h3 class="o-title" style="margin: 10px 0 5px; color: #000000; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 22px; text-transform: none;">Order Delivered</h3>

                                                      <p class="o-date" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; margin: 0; line-height: 22px; color: #6F6F6F;">17-05-2024</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td align="center" colspan="9">
                                                      <button class="cta" style="background: #FFC645; border: 1px solid #FFC645; font-family: 'Jost' Arial, sans-serif; font-size: 20px;font-weight: 400;line-height: 28px;text-align: center; color: #1E1E1E !important; vertical-align: middle; width: 100%; padding: 12px; text-transform: none; margin: 75px 0 45px;">Continue Shopping</button>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td style="text-align: center;">
                      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 92%; margin: 0 auto 30px; background: #FFFFFF;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <p style="font-family: \'Poppins\', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #6F6F6F; text-align: center; max-width: 70%; margin: 30px auto 26px; text-transform: none;">For assistance, connect with us on social media or reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center; padding-bottom: 52px; border-bottom: 1px solid #FFC645;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/be621c25343741b1ac5640833e3b34f7.png" style="display: block; width: 34px; height: 34px;" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/53caa3fd24c5413a91a6db136577fcf7.png" style="display: block; width: 34px; height: 34px;" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fa216fecba6741dea1d9d5452d498603.png" style="display: block; width: 34px; height: 34px;" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: none;">This is a system-generated email. Please do not reply.</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
          </tbody>
      </table>
      <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
  </body>

  </html>
  ```
</Accordion>

## Password Reset Template

A security-focused transactional email that helps users reset their passwords securely and quickly.

<Image align="center" alt="Sample Password Reset Template" border={true} caption="Sample Password Reset Template" src="https://files.readme.io/3866006424ffc74a98cae2a7ec5859b8c519df5937adbb62de028e39ce311072-Password_Reset_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  Sends a reset password link to users who have forgotten or initiated a reset request, ensuring account access is restored with minimal friction.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Password Reset</title>
      <style type="text/css">
          @media screen and (max-width: 480px) {         .header {           padding: 10px 0 !important;         }         .main-container {           padding: 0 10px !important;         }         .footer-container{           width: 95% !important;           padding: 0 10px !important;         }       }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1198.0" style="margin: 0px; padding: 0px; font-family: Jost, Arial, sans-serif; background-color: rgb(255, 255, 255); cursor: auto;">
      <table style="font-family: 'Jost', Arial, sans-serif; max-width: 600px; width: 100%; margin: 0 auto; background: #f5f5f5;">
          <!-- header -->
          <tbody>
              <tr>
                  <td align="center" class="header" style="padding: 30px 0;"><img alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: block; max-width: 159px; width: 100%; height: auto;" /></td>
              </tr>
              <!-- main content -->
              <tr>
                  <td class="main-container" style="padding: 0 24px;">
                      <table style="padding: 10px 10px 38px; background: #ffffff; width: 100%;">
                          <tbody>
                              <tr>
                                  <td align="center" style="padding-bottom: 22px;"><img alt="Image of a teal lock inside a teal ring on a light green background" height="319" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/password-reset/lock.png" style="width: 100%; height: auto;" width="532"
                                      /></td>
                              </tr>
                              <tr>
                                  <td style="color: #525c46; padding: 18px 0; text-align: center; font-size: 30px; font-weight: 600; line-height: 43.35px;">Reset Your Password</td>
                              </tr>
                              <tr>
                                  <td style="display: block;               max-width: 207px;               width: 40%;               background-color: #004a42;               margin: 0 auto;"> </td>
                              </tr>
                              <tr>
                                  <td>
                                      <div style="display: block; max-width: 207px; width: 40%; background-color: #004a42; margin: 0 auto;"> </div>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="text-align: center; padding: 22px 0 25px;">
                                      <p style="font-size: 14px; font-weight: 400; line-height: 22px; color: #909090; text-transform: none; margin: 0 auto; max-width: 386px;">We received a request to reset your password. If this was you, click the button below to reset it. If you didn’t make this request, please ignore this email.</p>

                                      <p style="font-size: 14px; font-weight: 400; line-height: 22px; color: #909090; text-transform: none; margin: 0 auto; max-width: 386px;"> </p>

                                      <p style="font-size: 14px; font-weight: 400; line-height: 22px; color: #909090; text-transform: none; margin: 0 auto; max-width: 386px;">For security, this link will expire in 2 hours.</p>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="center">
                                      <a href="#" style="background: #004a42; color: #fbfcfc; padding: 10px 0; text-decoration: none; display: inline-block; margin: 0 auto; border-radius: 5px; max-width: 465px; width: 100%; text-align: center;">Reset Password</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer -->
              <tr>
                  <td class="footer-container" style="text-align: center; margin: 42px 0 40px; padding: 0 24px; max-width: 552px; width:100%; display: inline-block;">
                      <table style="background: #fbfcfc; width: 100%; padding: 30px 10px 45px;">
                          <tbody>
                              <tr>
                                  <td style="text-align: center;">
                                      <p style="max-width: 386px; margin: 0 auto; color: #6f6f6f; font-size: 14px; font-weight: 400; line-height: 22px; text-transform: none;">For assistance, connect with us on social media or reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="display: block;               max-width: 386px;               background-color: #004a42;               margin: 34px auto 24px;               width: 71%;"> </td>
                              </tr>
                              <tr>
                                  <td align="center">
                                      <table>
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 8px;">
                                                      <a href="#"><img alt="Social Icon" height="34" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/be621c25343741b1ac5640833e3b34f7.png" width="34" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px;">
                                                      <a href="#"><img alt="Social Icon" height="34" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/53caa3fd24c5413a91a6db136577fcf7.png" width="34" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px;">
                                                      <a href="#"><img alt="Social Icon" height="34" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fa216fecba6741dea1d9d5452d498603.png" width="34" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="center" style="padding-top: 20px;">
                                      <table>
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 10px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; color: #1e1e1e; text-decoration: none;">Privacy</a>
                                                  </td>
                                                  <td style="padding: 0 10px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; color: #1e1e1e; text-decoration: none;">Account</a>
                                                  </td>
                                                  <td style="padding: 0 10px;">
                                                      <a display_text_og="Email%20Preferences" href="#" href_og="%23" style="font-size: 14px; font-weight: 400; line-height: 24px; color: rgb(30, 30, 30); text-decoration: none;">Email Preferences</a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="center" style="padding-top: 20px;">
                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">This is a system-generated email. Please do not reply.</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Promotional Template

A high-impact marketing email used to announce ongoing deals, highlight product collections, or showcase limited-time offers.

<Image align="center" alt="Sample Promotioanal Email Template" border={true} caption="Sample Promotional Email Template" src="https://files.readme.io/cf5f3dfc5d62e483db6d62e5d16182bf985ecbd41f621c31293191484681cb3b-Promotional_Email_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Announce a limited-time festive discount.
  * Promote newly launched products or collections.
  * Re-engage users with a category-specific deal.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Promotional</title>
      <link href="https://fonts.googleapis.com" rel="preconnect" />
      <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
      <link href="https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,100..900;1,100..900&amp;display=swap" rel="stylesheet" />
      <style type="text/css">
          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }              .main {                 max-width: 90% !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="text-align: center; position: relative; padding: 30px 0;">
                      <!-- Change Logo Image src as per your requirements --><img alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 159px; height: 73px; object-fit: cover;" />
                      <!-- Change Logo Image src as per your requirements -->
                  </td>
              </tr>
              <!-- header end-->
              <tr>
                  <td style="background: #DFDCD1; padding: 34px 0;">
                      <table border="0" cellpadding="0" cellspacing="0" style="max-width: 88%; margin: 0 auto;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <div class="img-wrap" style="max-width: 112px; max-height: 112px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/category-1.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>

                                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">Jackets</p>
                                  </td>
                                  <td>
                                      <div class="img-wrap" style="max-width: 112px; max-height: 112px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/category-2.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>

                                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">Shirts</p>
                                  </td>
                                  <td>
                                      <div class="img-wrap" style="max-width: 112px; max-height: 112px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/category-3.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>

                                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">Jeans</p>
                                  </td>
                                  <td>
                                      <div class="img-wrap" style="max-width: 112px; max-height: 112px; margin: 0 auto 10px;"><img alt="category image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/category-4.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>

                                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #464646; margin: 0;">T-shirts</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Banner Image -->
              <tr>
                  <td style="background: #FFFFFF;">
                      <table border="0" cellpadding="0" cellspacing="0" style="max-width: 88%; margin: 0 auto;" width="100%">
                          <tbody>
                              <tr>
                                  <td style="background: #DFDCD1"><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/banner.png" style="width: 100%; height: 100%; max-height: 641px; object-fit: cover;" /></td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Banner Image -->
              <tr>
                  <td style="background: #DFDCD1; padding: 25px 0 36px;">
                      <table border="0" cellpadding="0" cellspacing="0" style="max-width: 88%; margin: 0 auto;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <h2 style="font-family: 'Jost', Arial, sans-serif; font-size: 32px; font-weight: 300; text-transform: uppercase; line-height: 52px; color: #000000; margin: 0; padding-bottom: 8px;">FLASH SALE LIVE — DON’T MISS OUT!</h2>

                                      <p style="margin: 0; padding-bottom: 10px; font-family: 'Jost', Arial, sans-serif; text-transform: none; color: #464646; font-size: 10px; line-height: 20px; font-weight: 400;">Our flash sale is live — here’s your chance to avail the best of style at up to 50% off! Browse through items from our exclusive collection, where every piece of clothing tells a story. Go ahead, make a purchase, and
                                          make a proud statement wherever you go!</p>

                                      <a href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; text-transform: uppercase; line-height: 28px; color: #000000 !important; text-decoration: none; border: 1px solid #000000; padding: 7px; display: block; text-align: center; width: 100%;">Shop now</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- banner section -->
              <!-- looks section -->
              <tr>
                  <td style="padding: 66px 0 0;">
                      <table border="0" cellpadding="0" cellspacing="0" style="max-width: 88%; margin: 0 auto;" width="100%">
                          <tbody>
                              <tr>
                                  <td style="width: 50%; padding: 8px;"><img alt="looks image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/look-1.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                                  <td style="width: 50%; padding: 8px;"><img alt="looks image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/look-2.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                              </tr>
                              <tr>
                                  <td style="width: 50%; padding: 8px;"><img alt="looks image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/look-3.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                                  <td style="width: 50%; padding: 8px;"><img alt="looks image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/look-4.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                              </tr>
                              <tr>
                                  <td colspan="2" style="text-align: right;">
                                      <a href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; text-transform: uppercase; line-height: 28px; color: #000000 !important; text-decoration: none; border: 1px solid #000000; padding: 7px 22px; display: block; text-align: center; display: inline-block; margin:8px 8px 50px ; max-width: 153px;">Shop now</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- looks section -->
              <!-- product section -->
              <tr>
                  <td style=" background: #DFDCD1;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 90%; margin: 30px auto 50px; width: 100%;">
                          <tbody>
                              <tr>
                                  <td colspan="3">
                                      <h3 style="font-family: 'Jost', Arial, sans-serif;font-size: 32px;font-weight: 300;line-height: 52px; color: #000000; text-transform: uppercase; margin:0 0 10px;">PRODUCTS ON SALE</h3>

                                      <p style="font-family: 'Jost', Arial, sans-serif;font-size: 10px;font-weight: 400;line-height: 20px; color: #464646; text-transform: none; margin: 0 0 30px;">Browse through items from our exclusive collection.</p>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="vertical-align: top; width: 30%;">
                                      <!-- product card -->
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0 5px 10px; padding: 5px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="img-wrap">
                                                          <!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/product-1.png" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 60%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525; margin: 0;padding-right: 5px;">Elegent Bloom Top</h4>
                                                  </td>
                                                  <td style="width: 20%; vertical-align: middle;">
                                                      <p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 10px;font-weight: 300; line-height: 15px; text-align: right; font-style: italic;"><span class="rupee-sign">$</span>1500</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Flowy design perfect for casual outings or brunch dates.</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <a class="btn-link" href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 27px; text-transform: none; color: #0B0B0B !important; text-decoration: none; display: block; text-align: right;">Shop now <img alt="arrow" class="margin-left: 10px; max-width: 17px" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/arrow.png" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: middle; width: 30%;">
                                      <!-- product card -->
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0 5px 10px; padding: 5px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="img-wrap">
                                                          <!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/product-2.png" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 60%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525; margin: 0;padding-right: 5px;">Luxe Slik Shirt</h4>
                                                  </td>
                                                  <td style="width: 20%; vertical-align: middle;">
                                                      <p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 10px;font-weight: 300; line-height: 15px; text-align: right; font-style: italic;"><span class="rupee-sign">$</span>1500</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Premium silk shirt for a polished and sophisticated look.</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <a class="btn-link" href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 27px; text-transform: none; color: #0B0B0B !important; text-decoration: none; display: block; text-align: right;">Shop now <img alt="arrow" class="margin-left: 10px; max-width: 17px" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/arrow.png" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: middle; width: 30%;">
                                      <!-- product card -->
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0 5px 10px; padding: 5px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="img-wrap">
                                                          <!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/product-3.png" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 60%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525; margin: 0;padding-right: 5px;">Classic White Blouse</h4>
                                                  </td>
                                                  <td style="width: 20%; vertical-align: middle;">
                                                      <p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 10px;font-weight: 300; line-height: 15px; text-align: right; font-style: italic;"><span class="rupee-sign">$</span>1500</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Effortlessly chic, this is a versatile must-have for any occasion.</p>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <a class="btn-link" href="#" style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 27px; text-transform: none; color: #0B0B0B !important; text-decoration: none; display: block; text-align: right;">Shop now <img alt="arrow" class="margin-left: 10px; max-width: 17px" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/arrow.png" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td colspan="3" style="text-align: right;">
                                      <a display_text_og="VIEW%20ALL" href="#" href_og="%23" style="font-family: Jost, Arial, sans-serif; font-size: 14px; font-weight: 400; text-transform: uppercase; line-height: 20px; text-decoration: none; border: 1px solid rgb(0, 0, 0); padding: 4px 16px; display: inline-block; text-align: center; margin-top: 12px; color: rgb(0, 0, 0) !important;">VIEW ALL</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- product section -->
              <!-- review section -->
              <tr>
                  <td style=" background: #FFFFFF;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 90%; margin: 38px auto 0; width: 100%;">
                          <tbody>
                              <tr>
                                  <td colspan="3">
                                      <h3 style="font-family: 'Jost', Arial, sans-serif;font-size: 32px;font-weight: 300;line-height: 52px; color: #000000; text-transform: uppercase; margin:0 0 10px;">REVIEWS FROM CUSTOMERS</h3>

                                      <p style="font-family: 'Jost', Arial, sans-serif;font-size: 10px;font-weight: 400;line-height: 20px; color: #464646; text-transform: none; margin: 0 0 30px;">Hear what our customers have to say about our products</p>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="vertical-align: top; width: 30%; height: 100%;">
                                      <!-- review card -->
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #DFDCD1; margin: 0 5px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td style="vertical-align: middle; width: 20%;"><img alt="client" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/client-1.png" style="object-fit: contain; border-radius: 50%;" /></td>
                                                  <td style="vertical-align: middle; width: 80%;">
                                                      <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; margin:0 0 0 8px; line-height: 24px; color: #252525;">Ramesh Joshi</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <ul style="list-style: none; margin:0 0 7px; padding: 0;">
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="empty-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/empty-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                      </ul>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p style="margin: 0 0 14px; color: #464646; font-family: 'Jost', Arial, sans-serif;                                         font-size: 10px;font-weight: 400;line-height: 15px;text-align: left; text-transform: none; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 5; -webkit-box-orient: vertical; min-height: 75px;">Absolutely love the quality! The fit is perfect, and the fabric feels amazing. I’ll definitely be shopping here again!</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: top; width: 30%; height: 100%;">
                                      <!-- review card -->
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #DFDCD1; margin: 0 5px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td style="vertical-align: middle; width: 20%;"><img alt="client" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/client-2.png" style="object-fit: contain; border-radius: 50%;" /></td>
                                                  <td style="vertical-align: middle; width: 80%;">
                                                      <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; margin:0 0 0 8px; line-height: 24px; color: #252525;">Rina Roy</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <ul style="list-style: none; margin:0 0 7px; padding: 0;">
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="empty-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/empty-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="empty-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/empty-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                      </ul>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p style="margin: 0 0 14px; color: #464646; font-family: 'Jost', Arial, sans-serif;                                         font-size: 10px;font-weight: 400;line-height: 15px;text-align: left; text-transform: none; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 5; -webkit-box-orient: vertical; min-height: 75px;">Great selection and super fast delivery. The clothes look exactly like the pictures and fit beautifully. Highly recommend this brand!</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: top; width: 30%; height: 100%;">
                                      <!-- review card -->
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #DFDCD1; margin: 0 5px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td style="vertical-align: middle; width: 20%;"><img alt="client" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/client-3.png" style="object-fit: contain; border-radius: 50%;" /></td>
                                                  <td style="vertical-align: middle; width: 80%;">
                                                      <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; margin:0 0 0 8px; line-height: 24px; color: #252525;">Ritika Joshi</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <ul style="list-style: none; margin:0 0 7px; padding: 0;">
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                          <li style="width: 16px; height: 16px; display: inline-block;"><img alt="full-star" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Promotional/full-star.png" style="width: 100%; height: 100%; object-fit: contain;" /></li>
                                                      </ul>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p style="margin: 0 0 14px; color: #464646; font-family: 'Jost', Arial, sans-serif;                                         font-size: 10px;font-weight: 400;line-height: 15px;text-align: left; text-transform: none; overflow: hidden; text-overflow: ellipsis; display: -webkit-box; -webkit-line-clamp: 5; -webkit-box-orient: vertical; min-height: 75px;">I’m so impressed with the customer service and the attention to detail in the packaging. The products exceeded my expectations!</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td colspan="3">
                                      <p style="font-family: 'Jost', Arial, sans-serif;font-size: 12px;font-weight: 400;line-height: 20px; color: #464646; text-transform: none; margin: 33px 5px 30px;">Discover timeless style and exceptional quality with our exclusive collection, designed to inspire confidence and individuality. From chic everyday essentials to statement pieces, our collection blends comfort, elegance,
                                          and versatility. Embrace fashion that fits your lifestyle and celebrates your unique personality — because you deserve to look and feel your best.</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- review section -->
              <!-- footer start-->
              <tr>
                  <td align="center">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 90%; margin: 0 auto; background: #DFDCD1; padding: 25px 0 24px;">
                          <tbody>
                              <tr>
                                  <td>
                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; margin: 0 auto 26px; max-width: 70%;">For assistance, connect with us on social media or reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <!-- Privacy Policy -->
                              <tr>
                                  <td style="padding-bottom: 24px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration: none;">Privacy</a>
                                                  </td>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration: none;">Account</a>
                                                  </td>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration: none;">Unsubscribe</a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <!-- Privacy Policy -->
                              <!-- Add Links -->
                              <!-- Download Android Section -->
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 7px 40px; display: inline-block; border: 1px solid #ffffff;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 7px 40px; display: inline-block; border: 1px solid #ffffff;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 7px 40px; display: inline-block; border: 1px solid #ffffff;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 20px; height: 20px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/938da02c50734470bdcddd85a5217fc1.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <!-- Download Android Section -->
                              <!-- Add Links -->
                              <tr>
                                  <td>
                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">To opt out of promotional emails like this,
                                          <a href="#" style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
                                      </p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Referral Template

This growth marketing template is crafted to boost customer acquisition through referral programs.

<Image align="center" alt="Sample Referral Email Template" border={true} caption="Sample Referral Email Template" src="https://files.readme.io/a1f9bf30cfa2d42ad1601583469806bddb6ec51fadb9ffa91819893d8ab3b13d-Referral_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  Sends referral emails encouraging users to invite friends by offering incentives to referrers and referees.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](ddoc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Referral</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\') format(\'woff\');             font-style: normal;             font-weight: 400;         }         @font-face {             font-family: 'Jost', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Poppins', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 95% !important; margin-bottom: 20px !important; padding: 20px 10px !important;             }                         .logo{                 width: 145px !important; height: 55px !important;             }             .cta{                 padding: 10px 25px !important;             }             .sec-title{                 margin-bottom: 15px !important; font-size: 20px !important;              }             .b-desc{                 max-width: 100% !important;             }             .icon{                 width: 50px !important; height: 50px !important;             }             .content-wrap{                 margin-left: 10px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; background: rgb(5, 19, 32); cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #F5F5F5;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td align="center" style="display: block; padding: 12px 0; max-width: 90%; margin: 0 auto;">
                      <div class="logo-wrap">
                          <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 145px; height: 73px; object-fit: contain;" /></div>
                  </td>
              </tr>
              <!-- header end-->
              <tr>
                  <td style="text-align: center;">
                      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 90%; margin: 0 auto 30px; background: #FFFFFF; padding: 20px;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <!-- Change image src as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/banner.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                              </tr>
                              <tr>
                                  <td>
                                      <h2 style="font-family: Jost, Arial;font-size: 24px;font-weight: 300;line-height: 35px;text-align: center; color: #858585; text-transform: none; margin: 18px 0;"><span style="font-weight: 500; color: #0B848C; display: block;">REFER YOUR FRIENDS,</span> EARN REWARDS !</h2>

                                      <p style="color: #6F6F6F;font-family: 'Jost', Arial; font-size: 12px; font-weight: 400; line-height: 20.55px; text-align: center; margin: 0 0 18px;">Our referral program is simple. Invite your friends to sign up, and earn exciting rewards for every successful referral.</p>
                                      <button class="cta" style="background: #0B848C; border: 0.82px solid #0B848C; font-family: 'Jost', Arial;                             font-size: 16px;font-weight: 400;line-height: 16.44px;text-align: center; color: #FFFFFF; vertical-align: middle; width: 100%; padding: 12px; border-radius: 5px; text-transform: none;">Refer Now</button>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td align="center">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 90%; margin: 0 auto 31px; background: #FFFFFF; padding: 30px 20px;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <h3 class="sec-title" style="margin: 0 0 20px; font-family: 'Poppins', Arial;font-size: 22px;font-weight: 400;line-height: 16.44px; text-align: center; text-transform: none; color: #0B848C;">Here&#39;s What You Get</h3>

                                      <ul style="margin: 0; padding: 0; list-style: none;">
                                          <li style="padding: 24px 0; border-bottom: 1px solid #7B7B7B;">
                                              <div class="img-wrap" style="display: inline-block; width: 15%;"><img alt="ico1" class="icon" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/benfit-1.png" style="width: 60px; height: 60px; object-fit: contain;" /></div>

                                              <div class="content-wrap" style="display: inline-block; width: 80%;">
                                                  <h3 class="b-title" style="font-family: Jost, Arial; font-size: 16px; font-weight: 400; line-height: 22.19px; color: #1E1E1E; text-align: left; text-transform: none; margin: 0 0 2px;">FLAT 20% OFF</h3>

                                                  <p class="b-desc" style="font-family: Jost, Arial; font-size: 14px; font-weight: 400; line-height: 18.08px; text-align: left; color: #6F6F6F; margin: 0; max-width: 80%;">Both you and your friend will get a flat 20% discount code once they sign up.</p>
                                              </div>
                                          </li>
                                          <li style="padding: 24px 0; border-bottom: 1px solid #7B7B7B;">
                                              <div class="img-wrap" style="display: inline-block; width: 15%;"><img alt="ico1" class="icon" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/benfit-2.png" style="width: 60px; height: 60px; object-fit: contain;" /></div>

                                              <div class="content-wrap" style="display: inline-block; width: 80%;">
                                                  <h3 class="b-title" style="font-family: Jost, Arial; font-size: 16px; font-weight: 400; line-height: 22.19px; color: #1E1E1E; text-align: left; text-transform: none; margin: 0 0 2px;">SPECIAL ACCESS</h3>

                                                  <p class="b-desc" style="font-family: Jost, Arial; font-size: 14px; font-weight: 400; line-height: 18.08px; text-align: left; color: #6F6F6F; margin: 0; max-width: 75%;">Unlock exclusive collections and limited-edition items with every successful referral.</p>
                                              </div>
                                          </li>
                                          <li style="padding: 24px 0; border-bottom: 1px solid #7B7B7B;">
                                              <div class="img-wrap" style="display: inline-block; width: 15%;"><img alt="ico1" class="icon" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/benfit-3.png" style="width: 60px; height: 60px; object-fit: contain;" /></div>

                                              <div class="content-wrap" style="display: inline-block; width: 80%;">
                                                  <h3 class="b-title" style="font-family: Jost, Arial; font-size: 16px; font-weight: 400; line-height: 22.19px; color: #1E1E1E; text-align: left; text-transform: none; margin: 0 0 2px;">REFERRAL CREDITS</h3>

                                                  <p class="b-desc" style="font-family: Jost, Arial; font-size: 14px; font-weight: 400; line-height: 18.08px; text-align: left; color: #6F6F6F; margin: 0; max-width: 88%;">Earn credits with every successful referral. Redeem them to save on your next purchase.</p>
                                              </div>
                                          </li>
                                      </ul>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Referral copy link start-->
              <tr>
                  <td align="center">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 90%; margin: 0 auto 31px; background: #FFFFFF; padding: 30px 20px;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <h3 class="sec-title" style="margin: 0 0 26px; font-family: 'Poppins', Arial;font-size: 22px;font-weight: 400;line-height: 16.44px; text-align: center; text-transform: none; color: #0B848C;">Your Referral Link</h3>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <input disabled="disabled" style="border: 0.82px solid #0B848C; background-color: #F5F5F5; padding: 10px; font-family: 'Jost', Arial; border-radius: 5px; font-size: 16px; font-weight: 500; line-height: 22.19px; text-align: left; width: 95%; margin-bottom: 22px;"
                                      value="CLOTH@6374722#" />
                                      <button class="cta" style="background: #0B848C; border: 0.82px solid #0B848C; font-family: 'Jost', Arial;                             font-size: 16px;font-weight: 400;line-height: 16.44px;text-align: center; color: #FFFFFF; vertical-align: middle; width: 100%; padding: 12px; border-radius: 5px;"><img alt="logo" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/referral/icon-copy.png" style="width: 17px; height: 17px; object-fit: cover; margin-right: 5px;" /> Copy</button>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Referral copy link end-->
              <!-- start-->
              <tr>
                  <td align="center">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 90%; margin: 0 auto 31px; background: #FFFFFF; padding: 30px 20px;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <h3 class="sec-title" style="margin: 0 0 26px; font-family: 'Poppins', Arial;font-size: 22px;font-weight: 400;line-height: 16.44px; text-align: center; text-transform: none; color: #0B848C;">About Our Referral Program</h3>

                                      <p style="margin: 0; text-transform: none; color: #4F4F4F; font-family: 'Jost', Arial;                             font-size: 12px;font-weight: 400;line-height: 19px;text-align: center;">Our referral program is our way of saying thank you for spreading the word. Invite your friends to join us, and enjoy exclusive rewards for every successful referral. There’s no limit to how much you can earn, so go
                                          ahead and start referring now!</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- end-->
              <!-- footer start-->
              <tr>
                  <td align="center">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 90%; margin: 0 auto 10px; background: #FFFFFF; padding: 30px 20px 33px;" width="100%">
                          <tbody>
                              <tr>
                                  <td>
                                      <h3 class="sec-title" style="margin: 0 0 26px; font-family: 'Poppins', Arial;font-size: 22px;font-weight: 400;line-height: 16.44px; text-align: center; text-transform: none; color: #0B848C;">Share Your Referral Link</h3>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="display: inline-block; width: 30%">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 100%; height: 33px;">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/a6727b3615374d8b851ca91fe6b8b1ff.png" style="width: 100%; height: 100%; object-fit: contain;" /></a>
                                                  </td>
                                                  <td style="padding: 0 16px; display: inline-block; width: 30%">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 100%; height: 33px;">
                                                          <!-- Change image src as per your requirements --><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/5871f7fb88f74a9bbfb1f11b4100143a.png" style="width: 100%; height: 100%;object-fit: contain;" /></a>
                                                  </td>
                                                  <td style="padding: 0; display: inline-block; width: 30%">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 100%; height: 33px;">
                                                          <!-- Change image src as per your requirements --><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3b10f8de61954c88a374ee2687beb7dd.png" style="width: 100%; height: 100%; object-fit: contain;" /></a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td>
                                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">To opt out of promotional emails like this,
                                                          <a href="#" style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
                                                      </p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Show Recommendations Template

This personalized content email template is designed to showcase relevant video and music or suggest content based on user engagement and interests. It is available in both dark and light modes for aesthetic preference.

<Image align="center" alt="Sample Show Recommendations - Light & Dark Background Template" border={true} caption="Sample Show Recommendations - Light & Dark Background Template" src="https://files.readme.io/c4ccd5b6848ece16bb2e2967d9c264b7bf9d3766c87a1b4925a2046882751449-Show_Recommendations_-_White__Black.png" width="65% " />

<Accordion title="Expand to know more about the template.">
  ## Use Case Examples

  * Suggest items based on browsing, cart, or purchase history
  * Recommend articles, videos, or learning modules based on prior engagement or interests.
  * Promote complementary or premium products to increase average order value
  * Engage users post-transaction with related product or content recommendations.
  * Bring users back by showcasing trending or personalized items based on past behavior.
  * Tailor deals or discounts based on recommended categories or affinity tags.
  * Delivers curated video, show, or episode suggestions to users to enhance discovery, engagement, and viewership based on recent behavior.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb#update-social-media-links-and-download-links)

  ### Template Code

  ```html Light Background
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Show Recommendation</title>
      <style type="text/css">
          @font-face {             font-family: 'Poppins';             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Light.woff\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Poppins';             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Poppins';             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Medium.woff\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             } 			.heading h2{ 				font-size: 18px !important; 				line-height: 24px !important; 			}             .borderSpan {                 width: 20% !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" style="background: rgb(221, 221, 221); font-family: Poppins, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="text-align: center; position: relative;">
                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                          <tbody>
                              <tr>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                                  <td style="text-align: center; vertical-align: middle; padding: 20px">
                                      <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /></td>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- header end-->
              <!-- banner section -->
              <tr>
                  <td><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/manager-running-from-detailed-group-employees.png" style="width: 100%; height: 100%; max-height: 361px; object-fit: cover;" /></td>
              </tr>
              <!-- banner section -->
              <!-- new episod section -->
              <tr>
                  <td class="info-sec" style="text-align: center; padding: 40px 0px 20px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td class="borderSpan" style="width: 15%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                                  <td class="heading" style="text-align: center;">
                                      <h2 style="text-transform: uppercase; font-family: 'Poppins', Arial, sans-serif; font-size: 24px; font-weight: 400; line-height: 40px; margin: 0 auto;">CATCH UP WITH YOUR FAVORITES</h2>
                                  </td>
                                  <td class="borderSpan" style="width: 15%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td class="info-sec" style="text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 100%;padding: 0px 20px;">
                                      <p style="margin: 0; text-transform: none; color: #6f6f6f; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 25px; text-align: center; ">The wait is over! New episodes of <em data-renderer-mark="true">Black Mirror</em>, <em data-renderer-mark="true">Suits</em>, <em data-renderer-mark="true">Stranger Things</em>, and more are now streaming.</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td class="info-sec" style="text-align: center;padding: 20px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: auto; text-align: center; vertical-align: middle;">
                                      <a class="btn-link" href="#" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; text-transform: none; line-height: 25px; color: #FFFFFF; text-decoration: none; background: #F04444; padding: 6px 7px; display: inline-block; text-align: center; border-radius: 20px;"><img alt="youtube" class="btn-img" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/youtube.png" style="vertical-align: middle;" /> View All</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- New Episod End-->
              <!-- Weekly Recoomendatiom Start-->
              <tr>
                  <td class="info-sec" style="text-align: center;padding: 40px 0px 20px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td class="borderSpan" style="width: 18%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                                  <td class="heading" style="text-align: center;">
                                      <h2 style="text-transform: uppercase; font-family: 'Poppins', Arial, sans-serif; font-size: 24px; font-weight: 400; line-height: 40px; margin: 0 auto;">MORE SHOWS YOU’LL LIKE</h2>
                                  </td>
                                  <td class="borderSpan" style="width: 18%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td>
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width: 100%; margin-top: 20px;">
                          <tbody>
                              <tr>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0px 0px 10px 10px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/dragons-fantasy-artificial-intelligence-image.png" style="width: 100%; height: 100%; object-fit: cover;"
                                                          /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #000000; margin: 8px 0;padding-right: 5px;">Breaking Bad</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">A teacher turns to crime in desperate times</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0px 10px 10px 0px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/view-soccer-player-before-match.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #000000; margin: 5px 0;padding-right: 5px;">The Crown</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">The life and reign of Queen Elizabeth II</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0px 0px 10px 10px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/door-leading-magical-world.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #000000; margin: 8px 0;padding-right: 5px;">Brooklyn Nine-Nine</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">Hilarious detectives solve crimes</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #FFFFFF; margin: 0px 10px 10px 0px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/door-leading-magical.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #000000; margin: 5px 0;padding-right: 5px;">White Collar</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">A con artist and FBI agent team up</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td class="info-btn" style="padding: 25px 20px 40px 20px; width:100%; text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 100%; text-align: center; vertical-align: middle;">
                                      <a class="btn-link" href="#" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; text-transform: none; line-height: 25px; color: #FFFFFF; text-decoration: none; background: #d33c3c; padding: 7px 33px; display: inline-block; text-align: center; border-radius: 20px;">View All</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Weekly Recoomendatiom Start-->
              <!-- footer start-->
              <tr>
                  <td align="center" colspan="2">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width:100%; background: #ffffff; padding: 25px 0 25px;">
                          <tbody>
                              <tr>
                                  <td style="padding: 30px 0px; border-top: 2px solid #d33c3c; border-bottom: 2px solid #d33c3c;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/46e890761aa9484488a1d4b5b7e5e90a.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block; ">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/1ba99ae8ff9a4646a043bc4572c74c85.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9fd609ff93f44ae98273362f7509d619.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 30px">
                                                      <p style="text-transform: none; color: #4f4f4f; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 25px; text-align: center; margin-bottom: 0px;">For assistance, connect with us on social media or reach out to our support team at
                                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                                      </p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="padding:10px 10px 0px; text-align:center;">
                                      <p style="font-family: 'Poppins', Arial, sans-serif; text-transform: none; font-size: 14px; font-weight: 400; line-height: 20px; color: #4f4f4f; margin: 0; ">To opt out of promotional emails like this,
                                          <a href="#" style="font-weight:bold;text-decoration:none; color:#d33c3c; margin: 0;">unsubscribe here</a>
                                      </p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
  ```html Dark Background
  <!doctype html="">
  <html lang="en">

  <head>
      <title></title>
      <style type="text/css">
          @font-face {             font-family: 'Poppins', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Light.woff\') format(\'woff\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Poppins', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Regular.woff\') format(\'woff\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Poppins', Arial;             src: url(\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Fonts/Poppins-Medium.woff\') format(\'woff\');             font-style: normal;             font-weight: 500;         }          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }    .heading h2{     font-size: 18px !important;     line-height: 24px !important;    }             .borderSpan {                 width: 20% !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" style="background: rgb(0, 0, 0); font-family: Poppins, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #000;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="text-align: center; position: relative;">
                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                          <tbody>
                              <tr>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                                  <td style="text-align: center; vertical-align: middle; padding: 20px">
                                      <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/6b88dce76ef74ca5b9b17cc0a1dfcd13.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /></td>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- header end-->
              <!-- banner section -->
              <tr>
                  <td><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/manager-running-from-detailed-group-employees.png" style="width: 100%; height: 100%; max-height: 361px; object-fit: cover;" /></td>
              </tr>
              <!-- banner section -->
              <!-- new episod section -->
              <tr>
                  <td class="info-sec" style="text-align: center; padding: 40px 0px 20px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td class="borderSpan" style="width: 15%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                                  <td class="heading" style="text-align: center;">
                                      <h2 style="color:#fff;text-transform: uppercase; font-family: 'Poppins', Arial, sans-serif; font-size: 24px; font-weight: 400; line-height: 40px; margin: 0 auto;">CATCH UP WITH YOUR FAVORITEs</h2>
                                  </td>
                                  <td class="borderSpan" style="width: 15%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td class="info-sec" style="text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 100%;padding: 0px 20px;">
                                      <p style="color:#fff;margin: 0; text-transform: none;  font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 25px; text-align: center; ">The wait is over! New episodes of <em data-renderer-mark="true">Black Mirror</em>, <em data-renderer-mark="true">Suits</em>, <em data-renderer-mark="true">Stranger Things</em>, and more are now streaming.</p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td class="info-sec" style="text-align: center;padding: 20px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: auto; text-align: center; vertical-align: middle;">
                                      <a class="btn-link" href="#" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; text-transform: none; line-height: 25px; color: #FFFFFF; text-decoration: none; background: #F04444; padding: 6px 7px; display: inline-block; text-align: center; border-radius: 20px;"><img alt="youtube" class="btn-img" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/youtube.png" style="vertical-align: middle;" /> View All</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- New Episod End-->
              <!-- Weekly Recoomendatiom Start-->
              <tr>
                  <td class="info-sec" style="text-align: center;padding: 40px 0px 20px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td class="borderSpan" style="width: 18%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                                  <td class="heading" style="text-align: center;">
                                      <h2 style="color:#fff;text-transform: uppercase; font-family: 'Poppins', Arial, sans-serif; font-size: 24px; font-weight: 400; line-height: 40px; margin: 0 auto;">MORE SHOWS YOU’LL LIKE</h2>
                                  </td>
                                  <td class="borderSpan" style="width: 18%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #F04444;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td>
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width: 100%; margin-top: 20px;">
                          <tbody>
                              <tr>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #000; margin: 0px 0px 10px 10px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/dragons-fantasy-artificial-intelligence-image.png" style="width: 100%; height: 100%; object-fit: cover;"
                                                          /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #fff; margin: 8px 0;padding-right: 5px;">Breaking Bad</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">A teacher turns to crime in desperate times</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #000; margin: 0px 10px 10px 0px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/view-soccer-player-before-match.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #fff; margin: 5px 0;padding-right: 5px;">The Crown</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">The life and reign of Queen Elizabeth II</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #000; margin: 0px 0px 10px 10px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/door-leading-magical-world.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #fff; margin: 8px 0;padding-right: 5px;">Brooklyn Nine-Nine</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">Hilarious detectives solve crimes</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                                  <td style="vertical-align: top; width: 50%;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="background-color: #000; margin: 0px 10px 10px 0px; padding: 10px;">
                                          <tbody>
                                              <tr>
                                                  <td colspan="2">
                                                      <div class="product-img-wrap" style="width:100%; "><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations/door-leading-magical.png" style="width: 100%; height: 100%; object-fit: cover;" /></div>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td style="width: 100%; margin-bottom: 2px; vertical-align: middle;">
                                                      <h4 class="p-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 15px; color: #fff; margin: 5px 0;padding-right: 5px;">White Collar</h4>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td colspan="2">
                                                      <p class="desc" style="font-family: 'Poppins', Arial, sans-serif;text-transform: none; font-size: 10px; font-weight: 400; line-height: 15px; color: #6f6f6f; margin: 0; ">A con artist and FBI agent team up</p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td class="info-btn" style="padding: 25px 20px 40px 20px; width:100%; text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; margin: 0 auto; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="width: 100%; text-align: center; vertical-align: middle;">
                                      <a class="btn-link" href="#" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; text-transform: none; line-height: 25px; color: #FFFFFF; text-decoration: none; background: #d33c3c; padding: 7px 33px; display: inline-block; text-align: center; border-radius: 20px;">View All</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- Weekly Recoomendatiom Start-->
              <!-- footer start-->
              <tr>
                  <td align="center" colspan="2">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="width:100%; background: #000; padding: 25px 0 25px;">
                          <tbody>
                              <tr>
                                  <td style="padding: 30px 0px; border-top: 2px solid #fff; border-bottom: 2px solid #fff;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block; ">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 15px 15px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 30px; height: 30px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/c6684e1db05c4ce4b7783b6181e11c89.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                              <tr>
                                                  <td class="footer-content" style="padding:0px 30px">
                                                      <p style="text-transform: none; color: #fff; font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 25px; text-align: center; margin-bottom: 0px;">For assistance, connect with us on social media or reach out to our support team at
                                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #FFFFFF" title="support@example.com">support@example.com</a>
                                                      </p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="padding:10px 10px 0px; text-align:center;">
                                      <p style="font-family: 'Poppins', Arial, sans-serif; text-transform: none; font-size: 14px; font-weight: 400; line-height: 20px; color: #fff; margin: 0; ">To opt out of promotional emails like this,
                                          <a href="#" style="font-weight:bold;text-decoration:none; color:#d33c3c; margin: 0;">unsubscribe here</a>
                                      </p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
  </html>
  ```
</Accordion>

## Product Listing Template

This product-focused promotional template showcases productsby category —men, Women, and Kids—in a visual grid layout with distinct CTAs.

<Image align="center" alt="Sample Product Lkisting Template" border={true} caption="Sample Product Listing Template" src="https://files.readme.io/1e411d87dc1b962b681cf3cbb075653004921dad4926f132717fd5bc482c97fc-Product_Listing_HTML.png" width="25% " />

<br />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Promote seasonal or new arrivals across different product categories.
  * Highlight interest-based collections (for example, Men, Women, Kids, Pets).
  * Encourage exploration through curated visual sections such as Trending Now, Recommended for You, or Back in Stock.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>What&#39;s in the store</title>
      <link href="https://fonts.googleapis.com" rel="preconnect" />
      <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
      <link href="https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,100..900;1,100..900&amp;display=swap" rel="stylesheet" />
      <style type="text/css">
          @media screen and (max-width: 480px) {             .main {                 max-width: 95% !important;                 margin: 0 auto 20px !important;             }             .product-title{                 margin: 0 10px 15px !important;             }             .shop-cta{                 padding: 5px 10px !important;             }             .order-wrap{                 padding: 15px 20px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" style="margin: 0px; padding: 0px; font-family: Jost, Arial, sans-serif; background-color: rgb(119, 67, 67); cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" style="font-family:'Jost', Arial, sans-serif; max-width: 600px; margin: 0 auto; background: #FFFFFF;" width="100%">
          <tbody>
              <tr>
                  <td align="center" style="padding: 17px 0;"><img alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: block; max-width: 159px; width: 100%; height: auto;" /></td>
              </tr>
              <tr>
                  <td align="center" style="background-color: #d66437; padding: 38px 25px 25px;">
                      <h2 style="margin: 0; font-size: 36px; font-weight: 400; line-height: 45px; color: #FFFFFF; text-transform: uppercase;">WHAT’S NEW IN STORE</h2>

                      <p style="margin: 10px 0 0; font-size: 14px; font-weight: 400; line-height: 22px; color: #FFFFFF; text-transform: none;">Shop from the latest styles and trends</p>
                  </td>
              </tr>
              <tr>
                  <td align="center" style="background-color: #d66437;"><img alt="Banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/banner-image.png" style="display: block; max-width: 600px; width: 100%; height: auto;" /></td>
              </tr>
              <tr>
                  <td align="center" class="order-wrap" style="background-color: #d66437; padding: 15px 35px;">
                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                          <tbody>
                              <tr>
                                  <td align="left" style="font-size: 14px; font-weight: 300; line-height: 20px; color: #FFFFFF;">Get <span style="font-weight: 500;">FREE Delivery</span> on all orders</td>
                                  <td align="right">
                                      <a class="shop-cta" href="#" style="max-width: 125px; display: inline-block; padding: 8px 30px; font-size: 12px; font-weight: 400; line-height: 24px; color: #000000; background-color: #FFFFFF; text-align: center; text-transform: uppercase; text-decoration: none;">Shop Now</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- product section  -->
              <tr>
                  <td align="center" style="padding: 40px 0 34px;">
                      <h3 style="margin: 0; font-size: 32px; font-weight: 400; line-height: 42px; color: #0d0d0d; text-transform: uppercase;">NEW PRODUCTS LAUNCHED</h3>

                      <p style="margin: 10px 0 0; font-size: 10px; font-weight: 400; line-height: 20px; color: #909090; text-transform: none;">Explore newly launched products from our collection.</p>
                  </td>
              </tr>
              <!-- mens product -->
              <tr>
                  <td align="center">
                      <table border="0" cellpadding="0" cellspacing="0" class="main" style="width: 100%; max-width: 85%; margin: 0 auto 30px;" width="100%">
                          <tbody>
                              <tr>
                                  <td colspan="2">
                                      <h2 class="product-title" style="margin: 0 10px 24px; font-family:'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #000000; text-transform: uppercase;">Men</h2>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product-1.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product-2.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product-3.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/men-product-4.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- mens product -->
              <!-- women product -->
              <tr>
                  <td align="center">
                      <table border="0" cellpadding="0" cellspacing="0" class="main" style="width: 100%; max-width: 85%; margin: 0 auto 30px;" width="100%">
                          <tbody>
                              <tr>
                                  <td colspan="2">
                                      <h2 class="product-title" style="margin: 0 10px 24px; font-family:'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #000000; text-transform: uppercase;">Women</h2>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-product-1.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-product-2.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-product-3.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/women-product-4.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- women product -->
              <!-- kids product -->
              <tr>
                  <td align="center">
                      <table border="0" cellpadding="0" cellspacing="0" class="main" style="width: 100%; max-width: 85%; margin: 0 auto 30px;" width="100%">
                          <tbody>
                              <tr>
                                  <td colspan="2">
                                      <h2 class="product-title" style="margin: 0 10px 24px; font-family:'Jost', Arial, sans-serif; font-size: 20px; font-weight: 400; line-height: 24px; color: #000000; text-transform: uppercase;">Kids</h2>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product-1.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product-2.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                              </tr>
                              <tr>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product-3.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                                  <td align="right" style="padding: 0 10px 29px;" width="50%"><img alt="Product Image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/kid-product-4.png" style="display: block; max-width: 238px; width: 100%; height: auto;" />
                                      <a href="#" style="font-size: 22px; font-weight: 300; line-height: 37px; color: #D66437; text-decoration: none; margin-top: 5px; display: inline-block;">Shop now <img alt="arrow" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInSore/icon-arrow.png" style="max-width: 30px; height: 100%;" /></a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- kids product -->
              <!-- product section  -->
              <!-- footer start  -->
              <tr>
                  <td align="center" style="border-top: 0.5px solid #D66437; padding: 39px 0; text-align: center;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0">
                          <tbody>
                              <tr>
                                  <td style="padding: 0 8px; display: inline-block;">
                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/31a2d71dbe3e4579bcfa0d74dfc3e34d.png" style="display: block; width: 34px; height: 34px;" /></a>
                                  </td>
                                  <td style="padding: 0 8px; display: inline-block;">
                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/28b65b9647964152a2a5f6e816e50bf9.png" style="display: block; width: 34px; height: 34px;" /></a>
                                  </td>
                                  <td style="padding: 0 8px; display: inline-block;">
                                      <a href="#"><img alt="Social Icon" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3ae087af1f3544b0885c0a3ec31c2419.png" style="display: block; width: 34px; height: 34px;" /></a>
                                  </td>
                              </tr>
                              <tr>
                                  <td colspan="3">
                                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #939393; text-align: center; max-width: 80%; margin: 34px auto 27px;">For assistance, connect with us on social media or reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <tr>
                                  <td colspan="3" style="border-top: 0.5px solid #979797; padding-top: 24px;padding-bottom:24px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393 !important; text-decoration: none;">Privacy</a>
                                                  </td>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393 !important; text-decoration: none;">Account</a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td colspan="3" style="border-top: 0.5px solid #979797; padding-top: 24px;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 5px;">
                                                      <p class="f-desc" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393; max-width: 80%; margin: 0 auto;">To opt out of promotional emails like this,
                                                          <a href="#" style="color:#939393;text-decoration:none;font-weight:bold">unsubscribe here</a>
                                                      </p>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
          </tbody>
      </table>
      <!-- footer end  -->
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Winback Email Template

This re-engagement email template is tailored to bring back inactive users who have not interacted recently with your brand or app.

<Image align="center" alt="Sample Winback Email Template" border={true} caption="Sample Winback Email Template" src="https://files.readme.io/5cb660d31245cc7ff0a9c2c11186ddc7fe3f00a8793c7d0d4282a893a75edfea-Winback_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  Encourages churned or inactive users to return by offering a compelling incentive such as a discount or limited-time offer, paired with personalized product recommendations.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>WinBack</title>
      <link href="https://fonts.googleapis.com" rel="preconnect" />
      <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
      <link href="https://fonts.googleapis.com/css2?family=Jost:ital,wght@0,100..900;1,100..900&amp;display=swap" rel="stylesheet" />
      <style type="text/css">
          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }              .content {                 max-width: 90% !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: Jost, Arial, sans-serif; font-weight: 400; margin: 0px; padding: 0px; background: rgb(221, 221, 221); cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #ffffff;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td align="center" style="display: block; padding: 26px 0; max-width: 78%; margin: 0 auto;border-bottom: 1px solid #DDB67C;">
                      <div class="logo-wrap">
                          <!-- Change image src as per your requirements --><img alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="width: 159px; height: 73px; object-fit: cover;" /></div>
                  </td>
              </tr>
              <!-- header end-->
              <tr>
                  <td style="text-align: center;">
                      <h1 class="banner-title" style="font-family: Jost, Arial; font-size: 50px; font-weight: 400; line-height: 70px; color: #525C46; text-transform: uppercase; margin: 25px 0 28px;">WE MISS YOU!</h1>

                      <div class="banner-img">
                          <!-- Change image src as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-banner.png" style="width: 100%; height: 100%; max-height: 663px; object-fit: cover;" /></div>
                  </td>
              </tr>
              <tr>
                  <td align="center" style="display: block; padding: 30px 0 64px; max-width: 78%; margin: 0 auto;">
                      <h3 style="color: #525C46; font-family: 'Jost', Arial, sans-serif; font-size: 60px; font-weight: 400; line-height: 86px; text-transform: uppercase; margin: 0 0 17px;">30% OFF ON ALL PRODUCTS!</h3>

                      <p style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 20px;color:#909090; text-align: center; margin: 0; margin-bottom: 31px;">Take advantage of this exclusive offer just for you and enjoy 30% off your next purchase. It’s the perfect time to treat yourself to something special!</p>

                      <a display_text_og="Shop%20Now" href="#" href_og="%23" style="background-color: rgb(172, 135, 99); font-family: Jost, Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; border-radius: 20px; text-decoration: none; max-width: 171px; padding: 10px 40px; color: rgb(255, 255, 255) !important;">Shop Now</a>
                  </td>
              </tr>
              <tr>
                  <td>
                      <div style="margin: 0 auto; width: 100%;">
                          <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
                              <tbody>
                                  <tr>
                                      <td style="width: 33%; vertical-align: top;">
                                          <!-- product card -->
                                          <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin-bottom: 15px; padding: 0 5px;">
                                              <tbody>
                                                  <tr>
                                                      <td colspan="2">
                                                          <div class="img-wrap">
                                                              <!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-1.png" style="width: -webkit-fill-available" /></div>
                                                      </td>
                                                  </tr>
                                                  <tr>
                                                      <td style="width: 60%; margin-bottom: 2px; vertical-align: top;">
                                                          <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525; margin: 0;padding-right: 5px;">Radiance Boost Serum</h4>
                                                      </td>
                                                      <td style="width: 20%; vertical-align: top;">
                                                          <p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height: 24px; text-align: right;"><span class="rupee-sign">$</span>1500</p>
                                                      </td>
                                                  </tr>
                                                  <tr>
                                                      <td colspan="2">
                                                          <p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Brighten and hydrate your skin with this powerful, glow-enhancing serum.</p>
                                                      </td>
                                                  </tr>
                                              </tbody>
                                          </table>
                                      </td>
                                      <td style="width: 33%; vertical-align: top;">
                                          <!-- product card -->
                                          <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin-bottom: 15px; padding: 0 5px;">
                                              <tbody>
                                                  <tr>
                                                      <td colspan="2">
                                                          <div class="img-wrap">
                                                              <!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-1.png" style="width: -webkit-fill-available" /></div>
                                                      </td>
                                                  </tr>
                                                  <tr>
                                                      <td style="width: 60%; margin-bottom: 2px; vertical-align: top;">
                                                          <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525; margin: 0;padding-right: 5px;">Nourishing Repair Creeam</h4>
                                                      </td>
                                                      <td style="width: 20%; vertical-align: top;">
                                                          <p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height: 24px; text-align: right;"><span class="rupee-sign">$</span>1500</p>
                                                      </td>
                                                  </tr>
                                                  <tr>
                                                      <td colspan="2">
                                                          <p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Rejuvenate and repair your skin with this rich, soothing cream.</p>
                                                      </td>
                                                  </tr>
                                              </tbody>
                                          </table>
                                      </td>
                                      <td style="width: 33%; vertical-align: top;">
                                          <!-- product card -->
                                          <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="margin-bottom: 15px; padding: 0 5px;">
                                              <tbody>
                                                  <tr>
                                                      <td colspan="2">
                                                          <div class="img-wrap">
                                                              <!-- Change image src as per your requirements --><img alt="product" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Winback/product-1.png" style="width: -webkit-fill-available" /></div>
                                                      </td>
                                                  </tr>
                                                  <tr>
                                                      <td style="width: 60%; margin-bottom: 2px; vertical-align: top;">
                                                          <h4 style="font-family: 'Jost', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #252525; margin: 0;padding-right: 5px;">Pure Glow Face Mask</h4>
                                                      </td>
                                                      <td style="width: 20%; vertical-align: top;">
                                                          <p style="margin:0; color: #252525; font-family: 'Jost', Arial, sans-serif; font-size: 12px;font-weight: 300; line-height: 24px; text-align: right;"><span class="rupee-sign">$</span>1500</p>
                                                      </td>
                                                  </tr>
                                                  <tr>
                                                      <td colspan="2">
                                                          <p class="desc" style="font-family: 'Jost', Arial, sans-serif;text-transform: none; font-size: 8px; font-weight: 400; line-height: 13px; color: #909090; margin: 0; ">Deep cleanse and refresh with this revitalizing, skin-loving face mask.</p>
                                                      </td>
                                                  </tr>
                                              </tbody>
                                          </table>
                                      </td>
                                  </tr>
                              </tbody>
                          </table>
                      </div>
                  </td>
              </tr>
              <tr>
                  <td>
                      <div style="max-width: 90%; margin: 0 auto; width: 100%; text-align: right;">
                          <a class="btn-link" display_text_og="View%20All" href="#" href_og="%23" style="font-family: Jost, Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 15px; text-transform: none; text-decoration: none; color: rgb(172, 135, 99) !important;">View All</a>
                      </div>
                  </td>
              </tr>
              <!-- footer start-->
              <tr>
                  <td align="center" style="padding: 30px 0;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style=" max-width: 78%; margin: 0 auto;">
                          <tbody>
                              <tr>
                                  <td style="border-top: 1px solid #DDB67C; padding: 19px 0;">
                                      <table align="center" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9bd25df479a646f7bdbc487361af4e73.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/4caf5891eb8a4831a41d4894a47af5da.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 0 8px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/5f782083c6c446ba832acd09adecb140.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="border-top: 1px solid #DDB67C;">
                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #909090; margin: 19px 0 21px;">For assistance, connect with us on social media or reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation">
                                          <tbody>
                                              <tr>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration: none;">Privacy</a>
                                                  </td>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration: none;">Account</a>
                                                  </td>
                                                  <td style="padding: 0 5px;">
                                                      <a href="#" style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E !important; text-decoration: none;">Unsubscribe</a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="border-top: 1px solid #DDB67C;">
                                      <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #1E1E1E; padding-top:10px;">To opt out of promotional emails like this,
                                          <a href="#" style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
                                      </p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Subscription Renewal Reminder Template

This confirmation or promotional email template is used to acknowledge new subscriptions or upsell subscription-based services.

<Image align="center" alt="Sample Subscription FRenewal Reminder Template" border={true} caption="Sample Subscription Renewal Reminder Template" src="https://files.readme.io/49d165aab9c413c00f0ce66cdb32f0db944fc50676c79d291f99187be4c1a8b1-Subscription_Renewal_Email_Template.png" width="25% " />

<Accordion title="My Accordion Title">
  ### Use Case Examples

  Confirms a successful subscription or entices users to upgrade by highlighting plan benefits and encouraging exploration of exclusive features.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Subscription Renewal</title>
      <style type="text/css">
          @font-face {             font-family: 'Jost', Arial;             src: url(\\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Light.ttf\\') format(\\'woff\\');             font-style: normal;             font-weight: 300;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Regular.ttf\\') format(\\'woff\\');             font-style: normal;             font-weight: 400;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Medium.ttf\\') format(\\'woff\\');             font-style: normal;             font-weight: 500;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-SemiBold.ttf\\') format(\\'woff\\');             font-style: normal;             font-weight: 600;         }          @font-face {             font-family: 'Jost', Arial;             src: url(\\'https://devopsden.s3.ap-south-1.amazonaws.com/Attributics/Jost/Jost-Bold.ttf\\') format(\\'woff\\');             font-style: normal;             font-weight: 700;         }                  @media screen and (max-width: 480px) {             .main {                 max-width: 100% !important;             }                        .header-wrap{                 padding: 15px 0 !important;             }             .logo {                 width: 130px !important;                 height: 50px !important;             }             .benefit-wrap{                 max-width: 100% !important;                 padding: 30px 10px !important;             }             .banner-title{                 font-size: 28px !important;                 line-height: 30px !important;             }             .banner-subtitle{                 font-size: 32px !important;                 line-height: 36px !important;                 margin: 15px 0 !important;             }             .banner-desc{                 line-height: 20px !important;             }             .amt{                 font-size: 22px !important;                 line-height: 24px !important;             }             .no-year{                 font-size: 13px !important;                 line-height: 16px !important;             }             .list{                 font-size: 12px !important;                 line-height: 18px !important;             }             .sec-title{                 margin: 0 0 30px !important;                 font-size: 18px !important;             }             .line{                 width: 26% !important;             }             .link{                 font-size: 8px !important;                 line-height: 12px !important;             }             .link img{                 width: 5px !important;                 height: 5px !important;             }             .cta{                 padding: 7px 14px !important;                 font-size: 12px !important;                 line-height: 18px !important;             }             .content-spacing{                 padding: 30px 25px 50px !important;             }         }          @media screen and (max-width: 360px) {             .line{                 width: 18% !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="margin: 0px; padding: 0px; cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; font-family: 'Jost', Arial, sans-serif; font-weight: 400;" width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td class="header-wrap" style="text-align: center; position: relative; padding: 20px 0;">
                      <!-- Change image src as per your requirements --><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 150px; height: 80px; object-fit: contain;" /></td>
              </tr>
              <!-- header end-->
              <!-- banner section -->
              <tr>
                  <td style=" background: #FF5252;"><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Subscription/banner.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
              </tr>
              <tr>
                  <td style="background: #FF5252; padding: 5px 20px 10px;">
                      <h3 style="margin:0; font-family: 'Jost', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 27px; text-align: center; color: #FFFFFF; text-transform: uppercase;">YOUR PLAN ENDS ON FEB 15 2025</h3>
                  </td>
              </tr>
              <!-- banner section -->
              <tr>
                  <td>
                      <table border="0" cellpadding="0" cellspacing="0" class="main" style="max-width: 95%; margin: 0 auto;" width="100%">
                          <tbody>
                              <tr>
                                  <td class="content-spacing" style="background: #FFFFFF; padding: 30px 36px 50px; text-align: center;">
                                      <h2 class="banner-title" style="margin:0; font-size: 30px;font-weight: 600;line-height: 34px; text-transform: none;color: #000000;">Hi Emily,</h2>

                                      <h3 class="banner-subtitle" style="color: #5F5F5F;  font-size: 40px; font-weight: 400; line-height: 58px; margin: 0 0 13px;">Renew your subscription</h3>

                                      <p class="banner-desc" style="color: #4F4F4F; text-transform: none; font-size: 14px;font-weight: 400;line-height: 27px;">Don’t let your plan expire! Continue enjoying uninterrupted access to free delivery and priority support. Renew your subscription now!</p>

                                      <a class="cta" href="#" style="display: inline-block; text-transform: uppercase; text-decoration: none; padding: 7px 20px; background: #FF5252;font-size: 14px; font-weight: 400; line-height: 27px; text-align: center; color: #FFFFFF !important; box-shadow: 0px 4px 4px 0px #00000040;">Renew now</a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td>
                      <table border="0" cellpadding="0" cellspacing="0" class="main" style="max-width: 95%; margin: 0 auto; background: #FFFFFF;" width="100%">
                          <tbody>
                              <tr>
                                  <td><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Subscription/benifit-img.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td>
                      <table border="0" cellpadding="0" cellspacing="0" class="benefit-wrap" style="max-width:95%; margin: 0 auto 40px; background: #FFFFFF; padding: 50px 0  60px;" width="100%">
                          <tbody>
                              <tr>
                                  <td colspan="3">
                                      <h2 class="sec-title" style="text-transform: uppercase; color: #000000; margin: 0 0 50px; font-size: 20px; font-weight: 400;  line-height: 20px; text-align: center;">want to switch plans?</h2>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="card" style="padding: 0 10px; width: 33%;">
                                      <h3 class="amt" style="font-size: 28px; font-weight: 500; line-height: 27px; color: rgb(0, 0, 0); margin: 0px 0px 10px;">$99/ month</h3>

                                      <p class="no-year" style="font-size: 18px; font-weight: 400; line-height: 27px; color: #000000; text-transform: uppercase;">silver</p>

                                      <ul class="list" style="list-style: none; margin: 0; padding: 0; color: #6F6C6C; font-size: 14px; font-weight: 400; line-height: 27px;">
                                          <li class="item" style="margin-bottom: 5px;">- Free delivery on orders above $50</li>
                                          <li class="item" style="margin-bottom: 5px;">- Early access to sales</li>
                                          <li class="item" style="margin-bottom: 5px;">- Flat 10% off</li>
                                      </ul>

                                      <a class="link" href="#" style="font-size: 14px; font-weight: 400; line-height: 20px; text-transform: uppercase; color: #FF5252 !important; text-decoration: none; margin-top: 10px;display: inline-block;">Renew now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Subscription/arrow.png" style="width: 15px; height: 10px;" /></a>
                                  </td>
                                  <td class="card" style="padding: 0 10px; width: 33%;">
                                      <h2 class="amt" style="font-size: 28px; font-weight: 500; line-height: 27px;color: #000000; margin: 0 0 10px;">$199/ month</h2>

                                      <p class="no-year" style="font-size: 18px; font-weight: 400; line-height: 27px; color: #000000; text-transform: uppercase;">gold</p>

                                      <ul class="list" style="list-style: none; margin: 0; padding: 0; color: #6F6C6C; font-size: 14px; font-weight: 400; line-height: 27px;">
                                          <li class="item" style="margin-bottom: 5px;">- Free delivery on orders above $25</li>
                                          <li class="item" style="margin-bottom: 5px;">- Early access to sales</li>
                                          <li class="item" style="margin-bottom: 5px;">- Flat 15% off</li>
                                      </ul>

                                      <a class="link" href="#" style="font-size: 14px; font-weight: 400; line-height: 20px; text-transform: uppercase; color: #FF5252 !important; text-decoration: none; margin-top: 10px;display: inline-block;">REnew now <img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Subscription/arrow.png" style="width: 15px; height: 10px;" /></a>
                                  </td>
                                  <td class="card" style="padding: 0 10px; width: 33%;">
                                      <h2 class="amt" style="font-size: 28px; font-weight: 500; line-height: 27px;color: #000000; margin: 0 0 10px;">$299/ month</h2>

                                      <p class="no-year" style="font-size: 18px; font-weight: 400; line-height: 27px; color: #000000; text-transform: uppercase;">premium</p>

                                      <ul class="list" style="list-style: none; margin: 0; padding: 0; color: #6F6C6C; font-size: 14px; font-weight: 400; line-height: 27px;">
                                          <li class="item" style="margin-bottom: 5px;">- Free delivery on all orders</li>
                                          <li class="item" style="margin-bottom: 5px;">- Free one-day delivery</li>
                                          <li class="item" style="margin-bottom: 5px;">- Flat 30% off</li>
                                      </ul>

                                      <a class="link" display_text_og="RENIVEW%20NOW" href="#" href_og="%23" style="font-size: 14px; font-weight: 400; line-height: 20px; text-transform: uppercase; text-decoration: none; margin-top: 10px; display: inline-block; color: rgb(255, 82, 82) !important;">RENEW NOW</a>

                                      <a class="link" href="#" style="font-size: 14px; font-weight: 400; line-height: 20px; text-transform: uppercase; color: #FF5252 !important; text-decoration: none; margin-top: 10px;display: inline-block;"><img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Subscription/arrow.png" style="width: 15px; height: 10px;" /></a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer start-->
              <tr>
                  <td align="center" style="border-top: 9px solid #FF5252; padding-top: 40px;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" class="footer-conatiner" role="presentation" style="max-width: 95%; margin: 0 auto; background: #FF5252; padding: 37px 0 39px; ">
                          <tbody>
                              <tr>
                                  <td style="padding: 0;">
                                      <table align="center" border="0" cellpadding="0" cellspacing="0" style="text-align: center;" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td class="line" style="width: 35%; height: 1px; background: #FFFFFF; display: inline-block; vertical-align: middle;"> </td>
                                                  <td style="padding: 0 14px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 25px; height: 25px; ">
                                                          <!-- Change image src as per your requirements --><img alt="instagram" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3c09a826b3cd4920aa1230c7df32f91b.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 0 14px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 25px; height: 25px;"><img alt="facebook" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/18c1b92ff17443f38388d771deef565a.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td style="padding: 0 14px; display: inline-block;">
                                                      <a href="#" style="vertical-align: middle;display: inline-block; width: 25px; height: 25px;"><img alt="x" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/a971a978e8544cbfb0a0f3456c21463e.png" style="width: 100%; height: 100%;" /></a>
                                                  </td>
                                                  <td class="line" style="width: 35%; height: 1px; background: #FFFFFF; display: inline-block; vertical-align: middle;"> </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <p style="font-size: 14px; font-weight: 400; line-height: 27px; text-align: center; color: #FFFFFF; margin: 31px auto 0; max-width: 73%; text-transform: none;">For assistance, connect with us on social media or reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" style="color: #FFFFFF;" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <tr>
                                  <td>
                                      <p style="font-size: 14px; font-weight: 400; line-height: 27px; text-align: center; color: #FFFFFF; margin: 31px auto 0; max-width: 73%; text-transform: none;">To opt out of promotional emails like this,
                                          <a href="#" style="color:#fff;font-weight:bold;text-decoration:none;">unsubscribe here</a>
                                      </p>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- footer end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Scratch Card Template

This is an interactive email template designed to gamify the user experience by letting them "scratch" to reveal a reward, such as a coupon, discount, or points.

<Image align="center" alt="Sample Scratch Card Template" border={true} caption="Sample Scratch Card Template" src="https://files.readme.io/24e9bc9f41472d95c1db40a20c5b28651cfce5332851f800232fcea0b779782e-Scratch_Card_HTML.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Engage users during festive or seasonal campaigns with surprise offers.
  * Reactivate dormant users by giving them a chance to win a reward.
  * Reward loyal customers with a fun, interactive coupon reveal.
  * Launch a limited-time “scratch-to-win” contest to drive urgency and clicks.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html="">
  <html lang="en">

  <head>
      <title>Scratch Card</title>
      <link href="https://fonts.googleapis.com" rel="preconnect" />
      <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
      <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&amp;display=swap" rel="stylesheet" />
      <style type="text/css">
          @media screen and (max-width: 480px) {             .container {                 max-width: 100% !important;             }             .heading{                 font-size: 38px !important;                 line-height: 60px !important;             }             .coupon{                 font-size: 24px !important;                 line-height: 60px !important;             }             .coupon-code{                 font-size: 32px !important;                 line-height: 46px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="font-family: 'Poppins', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
      <table border="0" cellpadding="0" cellspacing="0" class="container" role="presentation" style="max-width: 600px; margin: 0 auto; background: url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/bg.png);background-repeat: no-repeat; background-position: center; "
      width="100%">
          <!-- header start-->
          <tbody>
              <tr>
                  <td style="text-align: center; vertical-align: middle; padding: 40px;">
                      <!-- Change image src as per your requirements -->
                      <div class="logo" style="background: url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/logobg.png);background-repeat: no-repeat; background-position: center;"><img alt="Logo" class="logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" /></div>
                  </td>
              </tr>
              <!-- header end-->
              <!-- scrtach card start-->
              <tr>
                  <td class="product-sec" style="text-align: center; padding:0px 40px 40px 40px; display: block;">
                      <table align="center" border="0" cellpadding="0" cellspacing="0" role="presentation" style="max-width: 100%; width: 100%;">
                          <tbody>
                              <tr>
                                  <td style="text-align: center;">
                                      <h2 class="heading" style="color:#ffffff; font-family: 'Poppins', Arial, sans-serif; font-size: 45px; font-weight: 700; line-height: 68px; margin: 0 auto; padding-bottom: 20px;">Mid-Season Sale</h2>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="padding:0px 10px;"><img alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/offer.png" style="width: 100%; height: 100%; object-fit: cover;" /></td>
                              </tr>
                              <tr>
                                  <td style="text-align: center;">
                                      <p class="coupon" style="color:#ffffff; font-family: 'Poppins', Arial, sans-serif; font-size: 34px; font-weight: 600; line-height: 80px; margin: 0 auto; text-transform: uppercase; line-height: 44px;">Scratch to see code</p>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="text-align: center; padding-top: 20px;">
                                      <a href="https://in1.dashboard.clevertap.com/redirect-to-login.html" style="display: inline-block; max-width: 90%; max-height: 150px; margin: 0 auto;"><img alt="Scratch card" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/Property%201%3DComponent%2068.png" style="width: 100%; height: 100%; object-fit: contain;" /></a>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <!-- scrtach card end-->
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

## Welcome Mailer Template

A warm onboarding email template greets new users, introduces your brand, and guides them towards their first action or purchase. These templates highlight core benefits and offer a smooth entry into your product or service experience.

<Image align="center" alt="Sample Welcome Mailer Tempaltes" border={true} caption="Sample Welcome Mailer Templates" src="https://files.readme.io/2e474cae87b50fdc4ee57e01a596acebbc0617e48be7f189ebc6013d79575f20-Welcome_Email_1__2_HTML.png" width="65% " />

<Accordion title="My Accordion Title" icon="fa-info-circle">
  ### Use Case Examples

  * Introduces new subscribers to the brand
  * Highlights key benefits of your product and encourages first engagement or purchases.

  ### Template Customization Options

  * [Replace the Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#call-to-actions-ctas)
  * [Update Links in the Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change the Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update the Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media Links and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html Variant 1
  <!doctype html="">
  <html lang="en">

  <head>
      <title></title>
      <link href="https://fonts.googleapis.com" rel="preconnect" />
      <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
      <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&amp;display=swap" rel="stylesheet" />
      <style type="text/css">
          * { 			margin: 0; 			padding: 0; 		}  		@media only screen and (max-width:480px) { 			.title { 				font-size: 26px !important; 				line-height: 36px !important; 				margin-top: 25px !important; 			}  			.sub-title { 				margin-top: 10px !important; 			}  			.f-desc { 				line-height: 20px; 			}  			.detail-block .d-desc { 				max-width: 90% !important; 			} 		}
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="cursor: auto;">
      <table border="0" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 100%; max-width: 600px; margin: 0 auto; background: #ffffff;" width="100%">
          <tbody>
              <tr>
                  <td style=" padding: 17px 30px; border-bottom: 0.5px solid #979797; text-align: right;">
                      <a class="btn" href="#" style="font-family:Poppins, Arial, sans-serif; padding: 5px 15px; background: #1DBF73; border-radius: 10px; font-size: 12px; line-height: 24px; vertical-align: middle; color: #000 !important; text-decoration: none; display: inline-block; font-weight: 400;">Get 30% OFF →</a>
                  </td>
              </tr>
              <tr>
                  <td style=" text-align: center; border-bottom: 0.5px solid #979797; position: relative;">
                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                          <tbody>
                              <tr>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #1DBF73;"> </div>
                                  </td>
                                  <td style="width: auto; text-align: center; vertical-align: middle;">
                                      <!-- Change Logo Image src as per your requirements --><img alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; max-width: 146px; height: auto; background: #ffffff; padding: 0 10px; vertical-align: middle;"
                                      />
                                      <!-- Change Logo Image src as per your requirements -->
                                  </td>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #1DBF73;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td>
                      <h2 class="title" style=" font-family: Poppins, Arial, sans-serif; font-size: 36px; line-height: 45px; text-align: center; text-transform: uppercase; color: #000000; margin: 29px 30px 0;"><span class="cm-light" style="font-family: Poppins, Arial, sans-serif; font-weight: 300; display: block;">WELCOME!</span> WE’RE EXCITED TO HAVE YOU WITH US</h2>

                      <p class="sub-title" style="font-family: Poppins, Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 32px; text-align: center; margin: 20px 30px 40px; color: #4F4F4F;">Get ready to discover what we have in store for you.</p>
                  </td>
              </tr>
              <tr>
                  <td style="text-align: center;">
                      <div class="banner-img-wrap">
                          <!-- Change Banner Image src as per your requirements --><img alt="banner" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Screenshot%202024-09-03%20at%2011.54.02%E2%80%AFPM.png" style="width: 100%; height:100%;" />
                          <!-- Change Banner Image src as per your requirements -->
                      </div>
                  </td>
              </tr>
              <tr>
                  <td class="detail-block" style="padding: 70px 20px 30px; margin-bottom: 30px; text-align: center; background-color: #ffffff;">
                      <h3 class="d-title" style="font-family:Poppins, Arial, sans-serif; font-size: 32px; font-weight: 400; line-height: 52px; text-align: center; margin-bottom: 18px; text-transform: uppercase; color: #0D0D0D;">LET’S GET STARTED</h3>

                      <p class="d-desc" style="font-family:Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 30px; text-align: center; margin: 0 auto 24px; max-width: 70%; color: #4F4F4F;">Welcome aboard! Your journey with us starts now, and we&#39;re here to make it count. Get started by exploring our website to know more about what we stand for. Stay on top of what’s new, get access to exclusive deals, and much more.</p>

                      <a class="btn-cta" display_text_og="Learn%20More" href="#" href_og="%23" style="padding: 7px 43px; max-width: 182px; font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 20px; text-align: center; background: rgb(29, 191, 115); outline: none; border: none; text-decoration: none; color: rgb(13, 13, 13) !important;">Learn More</a>

                      <div class="img-wrap" style="max-height: 368px; border-radius: 20px; margin-top: 50px;">
                          <!-- Change image src as per your requirements --><img alt="product img" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/pro-1.png" style="border-radius: 20px;" /></div>
                  </td>
              </tr>
              <tr>
                  <td class="detail-block" style="padding: 70px 20px 30px; margin-bottom: 30px; text-align: center; background-color: #F0EEF6;">
                      <h3 class="d-title" poppins="" style="font-family:">WHAT YOU CAN EXPECT</h3>

                      <p class="d-desc" style="font-family:Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 30px; text-align: center; margin: 0 auto 24px; max-width: 70%; color: #4F4F4F;">As a member of our community, you&#39;re on your way to unlocking a host of benefits tailored just for you. Expect personalized content, early access to new features, exclusive discounts, and expert insights that will help you stay
                          ahead of the curve.</p>

                      <a class="btn-cta" display_text_og="Learn%20More" href="#" href_og="%23" style="padding: 7px 43px; max-width: 182px; font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 20px; text-align: center; background: rgb(29, 191, 115); outline: none; border: none; text-decoration: none; color: rgb(13, 13, 13) !important;">Learn More</a>

                      <div class="img-wrap" style="max-height: 368px; border-radius: 20px; margin-top: 50px;">
                          <!-- Change image src as per your requirements --><img alt="product img" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/pro-2.png" style="border-radius: 20px;" /></div>
                  </td>
              </tr>
              <tr>
                  <td style="padding-top: 36px;">
                      <table border="0" cellpadding="0" cellspacing="0" class="footer" style="background: #F7F7F7;" width="100%">
                          <tbody>
                              <tr>
                                  <td colspan="5">
                                      <h2 class="footer-title" style="font-family: Poppins, Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 32px; text-align: center; color: #0D0D0D; text-transform: uppercase; margin:20px 0;">download OUR APP</h2>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="width: 30%; vertical-align: center; color: #979797">
                                      <div style="border-top: 1px solid #979797;"> </div>
                                  </td>
                                  <td style="width: auto; text-align: center; vertical-align: bottom;">
                                      <a class="btn-link" href="#" style="margin: 0 10px;">
                                          <!-- Change image src as per your requirements --><img alt="Download on Android" class="btn-img" src="https://d2xdgxd31vfz2r.cloudfront.net/1645780864/assets/6a5367d7266744b5a2b3f9d42a2d1757.png" style="background: #F7F7F7; position: relative; z-index: 1; height: 45px"
                                          /></a>
                                  </td>
                                  <td style="width: 5%; vertical-align: center;">
                                      <div style="border-top: 1px solid #979797"> </div>
                                  </td>
                                  <td style="width: auto; text-align: center; vertical-align: bottom; color: #979797">
                                      <a class="btn-link" href="#" style="margin: 0 10px;">
                                          <!-- Change image src as per your requirements --><img alt="Download on Apple" class="btn-img" src="https://d2xdgxd31vfz2r.cloudfront.net/1645780864/assets/2b9962fdc2dc4ce5a20bde593965d5d4.png" style="background: #F7F7F7; position: relative; z-index: 1; height: 45px"
                                          /></a>
                                  </td>
                                  <td style="width: 30%; vertical-align: center; color: #979797">
                                      <div style="border-top: 1px solid #979797"> </div>
                                  </td>
                              </tr>
                              <tr>
                                  <td colspan="5">
                                      <p class="f-desc" style="font-family:Poppins, Arial, sans-serif; padding: 22px 0 33px; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393; max-width: 80%; margin: 0 auto;">For assistance, reach out to our support team at
                                          <a data-renderer-mark="true" data-testid="link-with-safety" href="support@example.com" title="support@example.com">support@example.com</a>
                                      </p>
                                  </td>
                              </tr>
                              <tr class="f-wrap">
                                  <td colspan="5">
                                      <ul class="f-nav-list" style="padding: 19px 0; list-style: none; text-align: center; border-top: 1px solid #979797">
                                          <li class="f-nav-item" style=" margin: 0 5px;display: inline-block;">
                                              <a class="f-nav-link" href="#" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Contact Us</a>
                                          </li>
                                          <li class="f-nav-item" style=" margin: 0 5px; display: inline-block;">
                                              <a class="f-nav-link" href="#" style="font-family: Poppins, Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Terms of Use</a>
                                          </li>
                                          <li class="f-nav-item" style=" margin: 0 5px; display: inline-block;">
                                              <a class="f-nav-link" href="#" style="font-family: Poppins, Arial, sans-serif; font-size: 14px;  font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Privacy Policy</a>
                                          </li>
                                      </ul>
                                  </td>
                              </tr>
                              <!-- Unsubscribe Section-->
                              <tr class="f-wrap">
                                  <td colspan="5">
                                      <hr style="border: none; border-top: 1px solid #939393; margin: 0 auto; max-width: 100%;" />
                                      <p class="f-desc" style="font-family:Poppins, Arial, sans-serif; padding: 22px 0 33px; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393; max-width: 80%; margin: 0 auto;">To opt out of promotional emails like this,
                                          <a href="#" style="color:#1DBF73;text-decoration:none;font-weight:bold">unsubscribe here</a>
                                      </p>
                                  </td>
                              </tr>
                              <!-- Unsubscribe Section-->
                          </tbody>
                      </table>
                  </td>
              </tr>
          </tbody>
      </table>
      <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>
  </body>

  </html>
  ```
  ```html Variant 2
  <!DOCTYPE html>
  <html lang="en">

  <head>
      <title></title>
      <link href="https://fonts.googleapis.com" rel="preconnect" />
      <link crossorigin="" href="https://fonts.gstatic.com" rel="preconnect" />
      <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&amp;display=swap" rel="stylesheet" />
      <style type="text/css">
          * {             margin: 0;             padding: 0;         }          @media only screen and (max-width:480px) {             .title {                 font-size: 26px !important;                 line-height: 36px !important;                 margin-top: 25px !important;             }              .sub-title {                 margin-top: 10px !important;             }              .bg-wrap {                 padding-top: 40px !important;             }              .product-card {                 padding-bottom: 40px !important;             }         }
      </style>
  </head>

  <body data-gr-ext-installed="" data-new-gr-c-s-check-loaded="14.1242.0" data-new-gr-c-s-loaded="14.1242.0" style="cursor: auto;">
      <!-- Change Theme-->
      <table border="0" cellpadding="0" cellspacing="0" style="border-collapse: collapse; width: 100%; max-width: 600px; margin: 0 auto; background: #ffffff;" width="100%">
          <tbody>
              <tr>
                  <td style=" padding: 17px 30px; border-bottom: 0.5px solid #979797; text-align: right;">
                      <a class="btn" href="#" style="font-family:'Poppins', Arial, sans-serif; padding: 5px 15px; background: #1DBF73; border-radius: 10px; font-size: 12px; line-height: 24px; vertical-align: middle; color: #000 !important; text-decoration: none; display: inline-block; font-weight: 400;">Get 30% OFF →</a>
                  </td>
              </tr>
              <tr>
                  <!-- Header Section-->
                  <td style=" text-align: center; border-bottom: 0.5px solid #979797; position: relative;">
                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                          <tbody>
                              <tr>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #1DBF73;"> </div>
                                  </td>
                                  <td style="width: auto; text-align: center; vertical-align: middle;">
                                      <!-- “Logo Image” --><img alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" style="display: inline-block; max-width: 146px; height: auto; background: #ffffff; padding: 0 10px; vertical-align: middle;"
                                      />
                                      <!-- “Logo Image” -->
                                  </td>
                                  <td style="width: 50%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #1DBF73;"> </div>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
                  <!-- Header Section-->
              </tr>
              <tr>
                  <td>
                      <h2 class="title" style=" font-family: 'Poppins', Arial, sans-serif; font-size: 36px; line-height: 45px; text-align: center; text-transform: uppercase; color: #000000; margin: 29px 30px 0;"><span class="cm-light" style="font-family: 'Poppins', Arial, sans-serif; font-weight: 300; display: block;">WELCOME!</span> WE&#39;RE EXCITED TO HAVE YOU WITH US</h2>

                      <p class="sub-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 16px; font-weight: 400; line-height: 32px; text-align: center; margin: 20px 30px 40px; color: #4F4F4F;">Get ready to discover what we have in store for you.</p>
                  </td>
              </tr>
              <tr>
                  <td class="bg-wrap" style="padding-top: 46px; background: #F0EEF6;">
                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                          <tbody>
                              <tr>
                                  <td class="product-card" style="padding-bottom: 70px;">
                                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                                          <tbody>
                                              <tr>
                                                  <!-- First Product Image -->
                                                  <td class="product-image" style="width: 40%;"><img alt="product image pexels 1" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/pexels-1_1.png" style="width: 100%; height: 100%;" /></td>
                                                  <!-- First Product Image -->
                                                  <td class="product-detail" style="width: 60%; padding: 0 30px; vertical-align: middle;">
                                                      <h3 class="product-name" style="font-family: 'Poppins', Arial, sans-serif; font-size: 24px; font-weight: 400; line-height: 35px; color: #0D0D0D; margin-bottom: 10px; text-transform: uppercase;">LET&#39;S GET STARTED!</h3>

                                                      <p class="product-desc" style="font-family: 'Poppins', Arial, sans-serif; margin-bottom: 18px; font-size: 14px; font-weight: 400; line-height: 30px; color: #4f4f4f;">Welcome aboard! Your journey with us starts now, and we&#39;re here to make it count. Get started by exploring our website to know more about what we stand for. Stay on top of what&#39;s new, get access
                                                          to exclusive deals, and much more.</p>

                                                      <a class="btn" href="#" style="font-family:'Poppins', Arial, sans-serif; padding: 5px 15px; background: #1DBF73; border-radius: 10px; font-size: 12px; line-height: 24px; vertical-align: middle; color: #000 !important; text-decoration: none; display: inline-block; font-weight: 400;">Learn More</a>
                                                  </td>
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                              <tr>
                                  <td class="product-card" style="padding-bottom: 70px;">
                                      <table border="0" cellpadding="0" cellspacing="0" width="100%">
                                          <tbody>
                                              <tr>
                                                  <td class="product-detail" style="width: 60%; padding: 0 30px; vertical-align: middle;">
                                                      <h3 class="product-name" style="font-family: 'Poppins', Arial, sans-serif; font-size: 24px; font-weight: 400; line-height: 35px; color: #0D0D0D; margin-bottom: 10px; text-transform: uppercase;">WHAT YOU CAN EXPECT</h3>

                                                      <p class="product-desc" style="font-family: 'Poppins', Arial, sans-serif; margin-bottom: 18px; font-size: 14px; font-weight: 400; line-height: 30px; color: #4f4f4f;">As a member of our community, you&#39;re on your way to unlocking a host of benefits tailored just for you. Expect personalized content, early access to new features, exclusive discounts, and expert
                                                          insights that will help you stay ahead of the curve.</p>
                                                      <!-- Add Links -->

                                                      <a class="btn" href="#" style="font-family:'Poppins', Arial, sans-serif; padding: 5px 15px; background: #1DBF73; border-radius: 10px; font-size: 12px; line-height: 24px; vertical-align: middle; color: #000 !important; text-decoration: none; display: inline-block; font-weight: 400;">Learn More</a>
                                                      <!-- Add Links -->
                                                  </td>
                                                  <!-- Second Product Image -->
                                                  <td class="product-image" style="text-align: right; width: 40%;"><img alt="product image pexels 2" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/pexels-2_1.png" style="width: 100%; height: 100%;" /></td>
                                                  <!-- Second Product Image -->
                                              </tr>
                                          </tbody>
                                      </table>
                                  </td>
                              </tr>
                          </tbody>
                      </table>
                  </td>
              </tr>
              <tr>
                  <td style="padding-top: 54px;">
                      <table border="0" cellpadding="0" cellspacing="0" class="footer" style="background: #F7F7F7;" width="100%">
                          <tbody>
                              <tr>
                                  <td colspan="5">
                                      <h2 class="footer-title" style="font-family: 'Poppins', Arial, sans-serif; font-size: 18px; font-weight: 400; line-height: 32px; text-align: center; color: #0D0D0D; text-transform: uppercase; margin:20px 0;">DOWNLOAD OUR APP</h2>
                                  </td>
                              </tr>
                              <tr>
                                  <td style="width: 30%; vertical-align: middle; color: #979797">
                                      <div style="border-top: 1px solid #979797;"> </div>
                                  </td>
                                  <!-- Download Andoid Section-->
                                  <td style="width: auto; text-align: center; vertical-align: middle;">
                                      <a class="btn-link" href="#" style="margin: 0 10px;"><img alt="Download on Android" class="btn-img" src="https://d2xdgxd31vfz2r.cloudfront.net/1645780864/assets/6a5367d7266744b5a2b3f9d42a2d1757.png" style="background: #F7F7F7; position: relative; z-index: 1; height: 45px"
                                          /></a>
                                  </td>
                                  <!-- Download Andoid Section-->
                                  <td style="width: 5%; vertical-align: middle;">
                                      <div style="border-top: 1px solid #979797"> </div>
                                  </td>
                                  <!-- Download Apple Section-->
                                  <td style="width: auto; text-align: center; vertical-align: middle; color: #979797">
                                      <a class="btn-link" href="#" style="margin: 0 10px;"><img alt="Download on Apple" class="btn-img" src="https://d2xdgxd31vfz2r.cloudfront.net/1645780864/assets/2b9962fdc2dc4ce5a20bde593965d5d4.png" style="background: #F7F7F7; position: relative; z-index: 1; height: 45px"
                                          /></a>
                                  </td>
                                  <!-- Download Apple Section-->
                                  <td style="width: 30%; vertical-align: middle; color: #979797">
                                      <div style="border-top: 1px solid #979797"> </div>
                                  </td>
                              </tr>
                              <tr>
                                  <td colspan="5">
                                      <p class="f-desc" style="font-family:'Poppins', Arial, sans-serif; padding: 22px 0 33px; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393; max-width: 80%; margin: 0 auto;">For assistance, reach out to our support team at support@example.com</p>
                                  </td>
                              </tr>
                              <!-- Footer Section-->
                              <tr class="f-wrap">
                                  <td colspan="5">
                                      <ul class="f-nav-list" style="padding: 19px 0; list-style: none; text-align: center; border-top: 1px solid #979797">
                                          <li class="f-nav-item" style=" margin: 0 5px;display: inline-block;">
                                              <!-- Contact Us-->
                                              <a class="f-nav-link" href="#" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Contact Us</a>
                                              <!-- Contact Us-->
                                          </li>
                                          <li class="f-nav-item" style=" margin: 0 5px; display: inline-block;">
                                              <!-- Terms-->
                                              <a class="f-nav-link" href="#" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Terms of Use</a>
                                              <!-- Terms-->
                                          </li>
                                          <li class="f-nav-item" style=" margin: 0 5px; display: inline-block;">
                                              <!-- Privacy Policy-->
                                              <a class="f-nav-link" href="#" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px;  font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Privacy Policy</a>
                                              <!-- Privacy Policy-->
                                          </li>
                                      </ul>
                                  </td>
                              </tr>
                              <!-- Footer Section-->
                              <!-- Unsubscribe Section-->
                              <tr class="f-wrap">
                                  <td colspan="5">
                                      <hr style="border: none; border-top: 1px solid #939393; margin: 0 auto; max-width: 100%;" />
                                      <p class="f-desc" style="font-family:'Poppins', Arial, sans-serif; padding: 22px 0 33px; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #939393; max-width: 80%; margin: 0 auto;">To opt out of promotional emails like this,
                                          <a href="#" style="color:#1DBF73;text-decoration:none;font-weight:bold">unsubscribe here</a>
                                      </p>
                                  </td>
                              </tr>
                              <!-- Unsubscribe Section-->
                          </tbody>
                      </table>
                  </td>
              </tr>
          </tbody>
      </table>
  </body>
  <grammarly-desktop-integration data-grammarly-shadow-root="true"></grammarly-desktop-integration>

  </html>
  ```
</Accordion>

# AMP Templates

## Product Listing Template

This AMP template is designed to promote a curated selection of new arrivals, trending products, or personalized recommendations — all within an interactive AMP-powered layout. With in-mail CTAs, users can explore your latest offerings directly from their inbox, creating a seamless browsing experience.

<Image align="center" alt="Sample Product Listing Template" border={true} caption="Sample Product Listing Template" src="https://files.readme.io/3b422b68a566885f81d76d61157af681abbe2dad80105ae3e64ac39af27731cd-Product_Listing_AMP.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Highlight newly launched or trending products from your catalog.
  * Personalize the product showcase based on the user’s recent activity or preferences.
  * Run weekly or monthly What’s New campaigns for returning users.
  * Drive conversions by enabling users to click through to product pages without friction.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>body{visibility:hidden}</style>
  <style amp-custom>
  *{
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  }
  img{
  width: 100%;
  height: 100%;
  object-fit: cover;
  }
  .main {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: 0 auto;
  background: #FFFFFF;
  }
  @media only screen and (max-width: 400px) {
  body .main {
  max-width: 95%;
  }
  }
  .logo-wrap{
  padding: 17px 0;
  }
  .logo-wrap .img-wrap{
  max-width: 159px;
  max-height: 73px;
  margin: 0 auto;
  } 
  .footer{
  border-top: 0.5px solid #D66437;
  }
  .media-logo-list{
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  gap: 16px;
  margin: 39px 0 34px;
  }
  .media-logo-list .logo-item{
  width: 34px;
  height: 34px;
  }
  .media-logo-list .logo-item .logo-link{
  width: 100%;
  height: 100%;
  display: inline-block;
  } 
  .f-desc{
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  color: #939393;
  text-align: center; 
  max-width: 80%;
  margin: 0 auto 27px;
  }
  .f-nav-list{
  padding: 27px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  border-top: 0.5px solid #979797;
  }
  .f-nav-list .f-nav-item {
  margin: 0 5px;
  }
  .f-nav-list .f-nav-item .f-nav-link{
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  text-align: center;
  color: #939393;
  text-decoration: none; 
  }
  .banner {
  background: #d66437; 
  }
  .banner .top-wrap{
  padding: 38px 25px 25px;
  }
  .banner .title {
  margin-bottom: 10px;
  font-size: 36px;
  font-weight: 400;
  line-height: 45px;
  text-align: center;
  color: #fff;
  text-transform: uppercase;
  }
  .banner .desc {
  font-size: 14px;
  font-weight: 400;
  line-height: 22px;
  color: #fff;
  text-align: center;
  text-transform: none;
  }
  .banner .img-wrap {
  max-height: 377px;
  width: 100%;
  }
  .banner .cta-wrap {
  padding: 15px 35px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  }
  .banner .cta-desc {
  font-size: 14px;
  font-weight: 300;
  line-height: 20px;
  color: #fff;
  width: 50%;
  }
  .banner .cta-desc .cm-bold {
  font-weight: 500;
  }
  .banner .cta-btn {
  padding: 5px 35px;
  font-size: 12px;
  font-weight: 400;
  line-height: 24px;
  color: #000;
  text-align: center;
  text-transform: uppercase;
  max-width: 125px;
  background: #FFFFFF;
  outline: none;
  border: none;
  text-decoration: none; 
  }
  .product-wrap {
  padding: 40px 0 20px;
  max-width: 85%;
  margin: 0 auto;
  }
  .product-wrap .title {
  color: #0d0d0d;
  font-size: 32px;
  font-weight: 400;
  line-height: 52px;
  text-align: center;
  margin-bottom: 10px;
  }
  .product-wrap .desc {
  color: #909090;
  font-size: 10px;
  font-weight: 400;
  line-height: 20px;
  text-transform: none;
  text-align: center;
  margin-bottom: 28px;
  }
  .product-category{
  display: flex;
  justify-content: space-between;
  padding: 18px 0;
  }
  .category-wrap{
  width: 60%;
  }
  .category-search{
  text-align: right;
  width: 40%;
  }
  .product-list {
  padding: 0;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 15px;
  flex-wrap: wrap;
  list-style: none;
  }
  .product-list .product-item {
  width: 48%;
  margin-bottom: 15px;
  }
  .product-card .img-wrap {
  max-width: 238px;
  max-height: 238px;
  margin-bottom: 10px;
  }
  .product-card .p-link {
  font-size: 22px;
  font-weight: 300;
  line-height: 37px;
  text-decoration: none;
  color: #D66437;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  gap: 20px;
  }
  .product-card .p-link .icon {
  width: 30px;
  height: 14px;
  }
  .category-title{
  font-size: 20px;
  font-weight: 400;
  line-height: 24px;
  text-align: left;
  text-transform: uppercase;
  }
  .hide {
  display: none;
  }
  .show {
  display: block;
  }
  .custom-select{
  padding: 5px 12px;
  background: #FFFFFF;
  border: 1px solid #252525;
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  text-align: left;
  }
  .custom-select option{
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  text-align: left;
  padding: 5px 11px;
  }
  .custom-select option:disabled{display: none;}
  .custom-select option:hover,
  .custom-select option:focus,
  .custom-select option:active,
  .custom-select option:checked{ 
  color: #000000 ; background: #FFFFFF;
  }
  @media only screen and (max-width: 480px) {
  .logo-wrap .img-wrap {
  max-width: 130px;
  max-height: 60px;
  } 
  .banner .top-wrap {
  padding: 30px 25px 20px;
  }
  .banner .title {
  font-size: 28px;
  line-height: 38px;
  }
  .banner .cta-wrap {
  padding: 15px 25px;
  }
  .banner .cta-btn {
  padding: 5px 10px;
  }
  .product-list{
  gap: 10px
  }
  .product-list .product-item{
  margin-bottom: 20px;
  }
  .product-wrap{
  max-width: 100%;
  padding: 40px 10px 20px;
  }
  .product-wrap .title {
  font-size: 22px;
  line-height: 28px;
  }
  .product-wrap .desc{
  margin-bottom: 20px;
  }
  .product-card .p-link {
  font-size: 18px;
  line-height: 28px;
  gap: 10px;
  }
  .product-card .p-link .icon {
  width: 20px;
  height: 10px;
  }
  .media-logo-list {
  gap: 12px;
  margin: 29px 0 24px;
  }
  .f-nav-list {
  padding: 20px 0;
  }
  .f-desc{
  line-height: 20px;
  }
  }
  @media only screen and (max-width: 300px) {
  .product-wrap {
  padding: 40px 5px 20px;
  }
  }
  </style>
  </head>
  <body>
  <amp-state id="selectedCategory">
  <script type="application/json">
  {
  "value": "men"
  }
  </script>
  </amp-state>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo" width="159" height="73" />
  </div>
  </div>
  </header>
  <div class="banner">
  <div class="top-wrap">
  <h2 class="title">WHAT’S NEW IN STORE</h2>
  <p class="desc">Shop from the latest styles and trends</p>
  </div>
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/banner-image.png" alt="Banner" width="600" height="377"></amp-img>
  </div>
  <div class="cta-wrap">
  <p class="cta-desc">Get <span class="cm-bold">FREE Delivery</span> on all orders</p>
  <div class="cta-"> </div>
  <a href="https://www.google.co.in/" class="cta-btn">Shop Now</a>
  </div>
  </div>
  <div class="container">
  <div class="product-wrap">
  <h3 class="title">NEW PRODUCTS LAUNCHED</h3>
  <p class="desc">Explore newly launched products from our collection.</p>
  <div class="product-category">
  <div class="category-wrap">
  <h2 class="category-title" [text]="selectedCategory.value">men</h2>
  </div>
  <div class="category-search">
  <select class="custom-select" on="change:AMP.setState({selectedCategory: {value: event.value}})">
  <option value="explore" disabled selected [selected]="selectedCategory == 'explore'">Explore</option>
  <option value="men" [selected]="selectedCategory == 'men'">Men</option>
  <option value="women" [selected]="selectedCategory == 'women'">Women</option>
  <option value="kids" [selected]="selectedCategory == 'kids'">Kids</option>
  </select>
  </div>
  </div>
  <div class="category show" [class]="(selectedCategory.value == 'men') ? 'category show' : 'category hide'">
  <ul class="product-list">
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-1.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-2.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-3.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-4.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-5.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-6.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-7.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/men-product-8.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  </ul>
  </div>
  <div class="category hide" [class]="(selectedCategory.value == 'women') ? 'category show' : 'category hide'">
  <ul class="product-list">
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-1.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-2.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-3.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-4.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-5.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-6.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-7.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/women-product-8.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  </ul>
  </div>
  <div class="category hide" [class]="(selectedCategory.value == 'kids') ? 'category show' : 'category hide'">
  <ul class="product-list">
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/kid-product-1.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/kid-product-2.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/kid-product-3.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  <li class="product-item">
  <div class="product-card">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/kid-product-4.png" alt="Product Image" width="238" height="238"></amp-img>
  </div>
  <a href="https://www.google.co.in/" class="p-link">
  Shop now 
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/WhatsInStore-AMP/icon-arrow.png" alt="arrow-icon" class="icon" width="30" height="14"></amp-img>
  </a>
  </div>
  </li>
  </ul>
  </div>
  </div>
  </div>
  <footer class="footer">
  <ul class="media-logo-list">
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/31a2d71dbe3e4579bcfa0d74dfc3e34d.png" alt="instagram" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/28b65b9647964152a2a5f6e816e50bf9.png" alt="facebook" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/3ae087af1f3544b0885c0a3ec31c2419.png" alt="x" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  </ul>
  <p class="f-desc">For assistance, connect with us on social media or reach out to our support team at support@example.com </p>
  <ul class="f-nav-list">
  <li class="f-nav-item">
  <a href="https://www.google.co.in/" class="f-nav-link">Privacy</a>
  </li>
  <li class="f-nav-item">
  <a href="https://www.google.co.in/" class="f-nav-link">Account</a>
  </li>
  <li class="f-nav-item">
  <a href="https://www.google.co.in/" class="f-nav-link">Unsubscribe</a>
  </li>
  </ul>
  <p class="f-desc">To opt out of promotional emails like this, <a href="https://google.com" style="text-decoration:none;color:#D66437;font-weight:bold">unsubscribe here</a></p>
  </footer>
  </div>
  </body>
  </html>
  ```
</Accordion>

## Cart Abandonment Template

This AMP email template is designed to help recover lost sales by reminding users about the products left in their shopping carts. With interactive AMP elements, users can view product details, scroll through images, and proceed to checkout, all within the email.

<Image align="center" alt="Sample Cart Abandonment Template" border={true} caption="Sample Cart Abandonment Template" src="https://files.readme.io/95c18a7f9796b0566237c22f74af769ad410f5296f3b67f7d67b720b672e82c3-Cart_Anandonment_AMP.png" width="25% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Recover lost revenue by reminding users about items left in their shopping cart.
  * Re-engage users with personalized product suggestions based on past purchases or browsing behavior.
  * Promote urgency with limited-time offers or low stock alerts tied to abandoned items.
  * Enhance the shopping experience by allowing users to interact with product carousels or resume checkout directly within the email

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)

  ### Template Code

  ```html
  <!doctype html>
  <html ⚡4email>
  <head>
      <meta charset="utf-8">
      <script async src="https://cdn.ampproject.org/v0.js"></script>
      <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
      <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
      <style amp4email-boilerplate>
          body {
              visibility: hidden
          }
      </style>
      <style amp-custom>
          * {
              margin: 0;
              padding: 0;
          }
          ul,
          li {
              list-style: none;
          }
          /* Change Theme */
          body {
              font-family: "Helvetica", arial, sans-serif;
              font-weight: 400;
              background-color: rgb(248, 250, 252);
          }
          /* Change Theme */
          img {
              width: 100%;
              height: 100%;
              object-fit: contain;
          }
          amp-img {
              position: relative;
          }
          .main {
              position: relative;
              width: 100%;
              max-width: 600px;
              overflow: hidden;
              margin: 0 auto;
              background: #FFFFFF;
          }
          .container {
              max-width: 85%;
              margin: 0 auto;
          }
          @media only screen and (max-width: 400px) {
              .container,
              .main {
                  max-width: 95%;
              }
          }
          .cp-header {
              padding: 0 30px;
          }
          .cp-header.typ-shadow {
              box-shadow: 0px 4px 4px 0px #00000040;
          }
          .logo-wrap {
              display: flex;
              justify-content: space-between;
              align-items: center;
          }
          .logo-wrap .img-wrap {
              width: 127px;
              height: 58px;
              margin: 8.5px 0;
          }
          .nav-list {
              list-style: none;
              display: flex;
              align-items: center;
          }
          .nav-list .nav-item {
              padding: 25px 19px;
              border-left: 0.5px solid #919191;
              display: flex;
              align-items: center;
          }
          .nav-list .nav-item:last-child {
              padding-right: 0;
          }
          .cart-icon {
              border: 0;
              outline: 0;
              position: relative;
              background-color: transparent;
          }
          .cart-icon.active .dot {
              display: inline-block;
          }
          .dot {
              width: 6px;
              height: 6px;
              background: #FF533F;
              border-radius: 50%;
              display: none;
              position: absolute;
              top: 2px;
              right: 0px;
              z-index: 1;
          }
          .call-icon {
              width: 20px;
              height: 20px;
              margin-right: 5px;
          }
          .icon-text {
              font-size: 14px;
              font-weight: 400;
              line-height: 24px;
              text-align: center;
              color: #464646;
          }
          .cp-banner {
              width: 100%;
              max-height: 361px;
              margin-bottom: 22px;
          }
          .cp-footer {
              margin-top: 50px;
              background: #1E1E1E;
              padding: 32px 0 34px;
          }
          .media-logo-list {
              display: flex;
              justify-content: center;
              align-items: center;
              margin-bottom: 20px;
          }
          .media-logo-list .logo-item {
              padding: 6px 32px;
              border: 1px solid #FFFFFF;
          }
          .media-logo-list .logo-item .logo-link {
              display: inline-block;
          }
          .media-logo {
              width: 20px;
              height: 20px;
              display: inline-block;
          }
          .f-desc {
              font-size: 14px;
              font-weight: 400;
              line-height: 20px;
              text-align: center;
              color: #FFFFFF;
              margin: 0 auto;
              max-width: 84%;
              text-transform: capitalize;
          }
          .bs-sec {
              padding: 28px 0;
          }
          .bs-sec.typ-product {
              background: #F1F1F1;
          }
          .bs-sec .sec-title {
              padding: 0 26px 12px;
              text-transform: capitalize;
              font-size: 20px;
              font-weight: 400;
              line-height: 24px;
              text-align: center;
              position: relative;
              width: max-content;
              margin: 0 auto;
          }
          .bs-sec .sec-title.typ-2 {
              margin: 0;
              padding: 0 0 2px;
          }
          /* .bs-sec .sec-title.typ-2:after{
              display: none;
          } */
          .lyt-grid {
              display: flex;
              justify-content: space-between;
              align-items: flex-start;
              gap: 15px;
              margin-top: 20px;
          }
          .lyt-grid .grid-item {
              width: 33%;
          }
          .product-card {
              padding: 5px;
              position: relative;
              background: #FFFFFF;
          }
          .product-card .img-wrap {
              max-height: 177px;
              max-width: 150px;
              margin: 0 auto;
              overflow: hidden;
          }
          .product-card .p-cart-icon {
              background: #FFFFFF;
              padding: 3px 5px;
              border: 0;
              outline: 0;
              position: absolute;
              top: 5px;
              right: 5px;
              cursor: pointer;
          }
          .product-card .p-wrap {
              display: flex;
              justify-content: space-between;
              align-items: baseline;
              margin: 5px 0;
          }
          .product-card .p-title {
              width: 60%;
              font-size: 14px;
              font-weight: 400;
              line-height: 18px;
              color: #252525;
              padding-right: 5px;
          }
          .product-card .p-amt {
              color: #252525;
              font-size: 12px;
              font-weight: 300;
              line-height: 15px;
              text-align: right;
              font-style: italic;
          }
          .product-card .rupee-sign {
              font-size: 10px;
          }
          .product-card .p-desc {
              text-transform: capitalize;
              font-size: 8px;
              font-weight: 400;
              line-height: 13px;
              color: #909090;
              overflow: hidden;
              text-overflow: ellipsis;
              -webkit-line-clamp: 2;
              display: -webkit-box;
              -webkit-box-orient: vertical;
          }
          .btn-wrap {
              text-align: right;
          }
          .shop-cta {
              font-size: 12px;
              font-weight: 400;
              text-transform: capitalize;
              line-height: 15px;
              color: #000000;
              text-decoration: none;
              display: inline-block;
              text-align: center;
              margin-top: 15px;
          }
          .catalog-card {
              margin-top: 30px;
          }
          .catalog-card .catalog-img {
              max-width: 506px;
              max-height: 316px;
              position: relative;
          }
          .catalog-card .offer-band {
              background: #1e1e1e;
              text-align: center;
              padding: 7px 20px;
              font-size: 12px;
              font-weight: 400;
              line-height: 13px;
              letter-spacing: 0.25em;
              position: absolute;
              top: 0;
              left: 0;
              z-index: 1;
              width: 92%;
              color: #fff;
          }
          .catalog-card .cart-wrap {
              position: absolute;
              bottom: 0;
              right: 0;
              padding: 8px 10px;
              background: #fff;
              z-index: 1;
          }
          .catalog-card .cart-wrap .count {
              position: absolute;
              top: 8px;
              right: 8px;
              width: 11px;
              height: 11px;
              background: #FF533F;
              border-radius: 50%;
              color: #FFFFFF;
              font-size: 7px;
              font-weight: 400;
              line-height: 11px;
              text-align: center;
              z-index: 1;
          }
          .catalog-card .catalog-body {
              background: #f1f1f1;
              padding: 12px 14px 10px;
          }
          .catalog-card .c-wrap {
              display: flex;
              justify-content: space-between;
              align-items: flex-start;
          }
          .catalog-card .c-title {
              margin-bottom: 5px;
              font-size: 20px;
              font-weight: 400;
              line-height: 24px;
              color: #252525;
              width: 50%;
          }
          .catalog-card .c-amt {
              font-size: 22px;
              font-style: italic;
              font-weight: 400;
              line-height: 15px;
              text-align: right;
          }
          .catalog-card .rupee-sign {
              font-size: 10px;
          }
          .catalog-card .c-desc {
              font-size: 10px;
              font-weight: 400;
              line-height: 13px;
              color: #545454;
              width: 40%;
              text-transform: capitalize;
          }
          .catalog-card .btn-wrap {
              width: 60%;
              display: flex;
              justify-content: flex-end;
          }
          .catalog-card .catalog-cta {
              font-size: 14px;
              font-weight: 400;
              text-transform: uppercase;
              line-height: 20px;
              color: #FFFFFF;
              text-decoration: none;
              background: #000000;
              padding: 4px 34px;
              display: inline-block;
              text-align: center;
              max-width: 167px;
              border: none;
              margin-left: 10px;
              cursor: pointer;
          }
          .product-count {
              display: flex;
              align-items: center;
              justify-content: space-between;
              padding: 6px;
              background: #FFF;
              width: 60px;
          }
          .product-count .product-count-sign {
              background: transparent;
              border: 0;
              outline: none;
              cursor: pointer;
          }
          .product-count-value {
              font-size: 12px;
              font-weight: 400;
              line-height: 15px;
              text-align: center;
          }
          .input {
              border: 0.5px solid #000000;
              padding: 7px 10px;
              font-family: "Helvetica", arial, sans-serif;
              font-size: 16px;
              font-weight: 400;
              line-height: 24px;
              color: #000000;
              width: -webkit-fill-available;
          }
          .input::-webkit-input-placeholder,
          .input::-moz-placeholder,
          .input:-ms-input-placeholder,
          .input:-moz-placeholder {
              color: #919191;
          }
          @media only screen and (max-width: 480px) {
              .cp-header {
                  max-width: 100%;
                  padding: 0 10px;
              }
              .logo-wrap .img-wrap {
                  width: 101px;
                  height: 48px;
                  margin: 5.5px 0;
              }
              .nav-list .nav-item {
                  padding: 15px 10px;
              }
              .call-icon {
                  width: 18px;
                  height: 18px;
              }
              .icon-text {
                  font-size: 12px;
                  line-height: 20px;
              }
              .lyt-grid {
                  gap: 5px;
              }
              .product-card .p-title {
                  font-size: 12px;
                  line-height: 16px;
              }
              .product-card .p-amt {
                  font-size: 10px;
                  line-height: 16px;
              }
              .bs-sec .sec-title {
                  padding: 0 20px 12px;
                  font-size: 18px;
                  line-height: 20px;
              }
              .catalog-card .catalog-cta {
                  font-size: 10px;
                  line-height: 14px;
                  padding: 5px;
              }
          }
          .form-list {
              margin-top: 20px;
              display: flex;
              flex-wrap: wrap;
              justify-content: space-between;
              gap: 10px;
          }
          .form-item {
              width: 49%;
              position: relative;
              padding-bottom: 20px;
          }
          .form-item.typ-full {
              width: 100%;
          }
          [visible-when-invalid]{
              display: block;
          }
          .error-msg{
              font-size: 10px;  
              display: none;   
              position: absolute;
              bottom: 0; left: 0;       
          }
          .error-msg.visible{
              display: block;   
          }
          .field-wrap {
              display: block;
              position: relative;
              padding-left: 25px;
              margin-bottom: 10px;
              cursor: pointer;
              -webkit-user-select: none;
              -moz-user-select: none;
              -ms-user-select: none;
              user-select: none;
              font-size: 16px;
              font-weight: 400;
              line-height: 24px;
          }
          .field-wrap input {
              position: absolute;
              opacity: 0;
              cursor: pointer;
          }
          .checkmark {
              position: absolute;
              top: 50%;
              transform: translateY(-50%);
              left: 0;
              height: 17px;
              width: 17px;
              background-color: #0B0B0B;
              border-radius: 50%;
          }
          .field-wrap input:checked~.checkmark {
              background-color: #0B0B0B;
          }
          .checkmark:after {
              content: "";
              position: absolute;            
              display: block;
          }
          .field-wrap input:checked~.checkmark:after {
             display: none;
          }
          .field-wrap .checkmark:after {
              top: 2px;
              left: 2px;
              width: 13px;
              height: 13px;
              border-radius: 50%;
              background: #FFFFFF;
          }
          .mt-32 {
              margin-top: 32px;
          }
          .form-btn {
              font-size: 20px;
              font-weight: 400;
              line-height: 24px;
              text-align: center;
              width: 100%;
              background: #252525;
              border: 0;
              outline: none;
              color: #FFF;
              padding: 10px;
              cursor: pointer;
          }
          .tab-3 {
              position: relative;
          }
          .modal-overlay {
              width: 100%;
              height: 100%;
              background-color: #000000;
              padding: 100px 0;
          }
          .modal {
              width: 75%;
              margin: 40px auto;
              z-index: 12;
              background: #FFF;
              padding: 70px 30px;
              position: relative;
          }
          .close {
              width: 27px;
              height: 27px;
              display: inline-block;
              text-align: center;
              background: #000000;
              font-size: 13px;
              color: #FFFFFF;
              line-height: 27px;
              border-radius: 50%;
              position: absolute;
              top: 6px;
              right: 6px;
              cursor: pointer;
          }
          .m-title {
              font-size: 20px;
              font-weight: 400;
              line-height: 24px;
              text-align: center;
              margin-bottom: 20px;
              color: #000000;
              text-transform: uppercase;
          }
          .m-desc {
              font-size: 14px;
              font-weight: 400;
              line-height: 20px;
              text-align: center;
              color: #545454;
              text-transform: capitalize;
              max-width: 70%;
              margin: 0 auto;
          }
          .product-list {
              margin: 16px 0;
          }
          .product-list .product-item {
              display: flex;
              justify-content: space-between;
              padding: 16px 0;
              border-bottom: 1px solid #919191;
          }
          .product-list .product-item:last-child {
              border: 0;
              padding-bottom: 0;
          }
          .lhs {
              width: 80%;
          }
          .rhs {
              width: 20%;
              display: flex;
              flex-direction: column;
              justify-content: space-between;
              align-items: flex-end;
          }
          .product-item .p-name {
              font-size: 16px;
              font-weight: 400;
              line-height: 24px;
              color: #000000;
              margin-bottom: 6px;
          }
          .product-item .p-desc {
              font-size: 10px;
              font-weight: 400;
              line-height: 13px;
              color: #545454;
              margin-bottom: 6px;
          }
          .product-item .p-quality {
              font-size: 16px;
              font-weight: 400;
              line-height: 24px;
              color: #000000;
          }
          .product-item .delete-icon {
              background: transparent;
              outline: none;
              border: 0;
          }
          .product-item .p-amt {
              font-size: 22px;
              font-style: italic;
              font-weight: 300;
              line-height: 24px;
              color: #000000;
          }
          .product-item .p-total {
              font-size: 20px;
              font-weight: 400;
              line-height: 24px;
              color: #000000;
          }
          .typ-bottom-padding-zero {
              padding-bottom: 0;
          }
          .disabled {
              pointer-events: none;
              cursor: not-allowed;
              opacity: 0.7;
          }
          @media only screen and (max-width: 480px) {
              .catalog-card .offer-band {
                  padding: 7px;
                  font-size: 10px;
                  line-height: 10px;
                  width: 96%;
              }
              .catalog-card .c-title {
                  font-size: 16px;
                  line-height: 18px;
              }
              .catalog-card .c-amt {
                  font-size: 18px;
                  line-height: 20px;
              }
              .catalog-card .c-desc {
                  margin-bottom: 7px;
              }
              .catalog-card .c-wrap {
                  flex-wrap: wrap;
              }
              .catalog-card .btn-wrap,
              .catalog-card .c-desc {
                  width: 100%;
              }
              .form-item {
                  width: 100%;
              }
              .lhs,
              .rhs {
                  width: 50%;
              }
              .product-item .p-total,
              .product-item .p-amt {
                  font-size: 18px;
                  line-height: 20px;
              }
          }
      </style>
  </head>
  <body>
      <div class="main">
          <div id="ProductCatalogform" on="tap:AMP.setState({productCatalog01: {fuuid: 01 }})" role="tab" tabindex="1"
              class="amp-html-block widget-container">
              <form class="form-container" method="post" id="productCatalog01Form" enctype="multipart/form-data"
                  action-xhr="https://example.com" custom-validation-reporting="show-all-on-submit" on="submit:AMP.setState({
                      productCatalog01: {
                          currentStep: productCatalog01.currentStep == 2 : productCatalog01.currentStep + 1, 
                          submitting: true,
                          editAddress: false
                      }
                  });
                  submit-success:AMP.setState({
                      productCatalog01: {
                          submitting: false, 
                          paymentUrl: productCatalog01.paymentUrl || event.response.url
                      }
                  });">
                  <input hidden id="fuuid" name="fuuid" [value]="01" />
                  <input hidden name="catalogType" value="STATIC" />
                  <input hidden name="discountCouponCode" value="" />
                  <amp-state id="productCatalog01">
                      <script type="application/json">
                          {
                              "first_name": "",
                              "last_name": "",
                              "address": "",
                              "landmark": "",
                              "city": "",
                              "country": "",
                              "pincode": "",
                              "phoneNumber": "",
                              "email": "",
                              "payment_mode": "",
                              "isFirstNameValid": false,
                              "isLastNameValid": false,
                              "isPhoneNumberValid": false,
                              "isEmailValid": false,
                              "isPincodeValid": false,
                              "isCityValid": false,
                              "editAddress": false,        
                              "paymentUrl": "",
                              "product1": {
                                  "id": 1,
                                  "qty": 0,
                                  "title": "Mystic Elixir",
                                  "price": 1500,
                                  "selectedVariantId": 0,
                                  "addedToCart": false,
                                  "variantId": 101,
                                  "variantTitle": "Default Title",
                                  "comparePrice": "null",
                                  "variants": {
                                      "101": {
                                          "id": 101,
                                          "price": 1500,
                                          "title": "Default Title",
                                          "comparePrice": "null"
                                      }
                                  }
                              },
                              "product2": {
                                  "id": 2,
                                  "qty": 0,
                                  "title": "Opulent Essence",
                                  "price": 1500,
                                  "selectedVariantId": 0,
                                  "addedToCart": false,
                                  "variantId": 102,
                                  "variantTitle": "Default Title",
                                  "comparePrice": "null",
                                  "variants": {
                                      "102": {
                                          "id": 102,
                                          "price": 1500,
                                          "title": "Default Title",
                                          "comparePrice": "null"
                                      }
                                  }
                              },
                              "product3": {
                                  "id": 3,
                                  "qty": 0,
                                  "title": "Product Name 3",
                                  "price": 1500,
                                  "selectedVariantId": 0,
                                  "addedToCart": false,
                                  "variantId": 103,
                                  "variantTitle": "Default Title",
                                  "comparePrice": "null",
                                  "variants": {
                                      "103": {
                                          "id": 103,
                                          "price": 1500,
                                          "title": "Default Title",
                                          "comparePrice": "null"
                                      }
                                  }
                              },
                              "product4": {
                                  "id": 4,
                                  "qty": 0,
                                  "title": "Product Name 4",
                                  "price": 1500,
                                  "selectedVariantId": 0,
                                  "addedToCart": false,
                                  "variantId": 104,
                                  "variantTitle": "Default Title",
                                  "comparePrice": "null",
                                  "variants": {
                                      "104": {
                                          "id": 104,
                                          "price": 1500,
                                          "title": "Default Title",
                                          "comparePrice": "null"
                                      }
                                  }
                              },
                              "product5": {
                                  "id": 5,
                                  "qty": 0,
                                  "title": "Product Name 5",
                                  "price": 1500,
                                  "selectedVariantId": 0,
                                  "addedToCart": false,
                                  "variantId": 105,
                                  "variantTitle": "Default Title",
                                  "comparePrice": "null",
                                  "variants": {
                                      "105": {
                                          "id": 105,
                                          "price": 1500,
                                          "title": "Default Title",
                                          "comparePrice": "null"
                                      }
                                  }
                              },
                              "currentStep": 1
                          }
                      </script>
                  </amp-state>
                  <!-- <h1 [text]="productCatalog01.currentStep"></h1> -->
                  <header class="cp-header typ-shadow" [hidden]="productCatalog01.currentStep == 3">
                      <div class="logo-wrap">
                          <div class="img-wrap">
                              <!-- Change Logo -->
                              <amp-img layout="responsive"
                                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo.png"
                                  alt="Logo" width="127" height="58" />
                              <!-- Change Logo -->
                          </div>
                          <ul class="nav-list">
                              <li class="nav-item">
                                  <div class="cart-icon checkout-button"
                                      [class]="productCatalog01.currentStep == 2 ? 'cart-icon active' : 'cart-icon'"
                                      on="tap:AMP.setState({
                                          productCatalog01 : {
                                          currentStep:  2 ,
                                          editAddress: true,
                                          }
                                      })"
                                      >
                                      <amp-img layout="fixed"
                                          src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                          alt="cart-icon" class="icon" width="22" height="22" />
                                      <span class="dot"></span>
                                  </div>
                              </li>
                              <li class="nav-item">
                                  <span class="icon-wrap">
                                      <amp-img class="call-icon" layout="responsive"
                                          src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/call-icon.png"
                                          alt="call icon" width="20" height="20" />
                                  </span>
                                  <p class="icon-text">9878725637</p>
                              </li>
                          </ul>
                      </div>
                  </header>
                  <div class="step1" [hidden]="productCatalog01.currentStep != 1">
                      <div class="bs-sec typ-look">
                          <div class="sec-head">
                              <h3 class="sec-title">PRODUCTS</h3>
                          </div>
                          <div class="sec-body">
                              <div class="container">
                                  <div class="catalog-card">
                                      <div class="catalog-img">
                                          <h3 class="offer-band">Get 20% off for your first purchase.</h3>
                                          <!-- Change Product Image -->
                                          <amp-img
                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-1.png"
                                              layout="responsive" alt="look" width="506" height="316" />
                                          <!-- Change Product Image -->
                                          <span class="cart-wrap">
                                              <span class="count" hidden [hidden]="productCatalog01.product1.qty <= 0"
                                                  [text]="productCatalog01.product1.qty"></span>
                                              <amp-img layout="fixed"
                                                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                  alt="cart-icon" class="icon" width="27" height="27" />
                                          </span>
                                      </div>
                                      <div class="catalog-body">
                                          <div class="c-wrap">
                                              <h3 class="c-title">Mystic Elixir</h3>
                                              <p class="c-amt">
                                                  <span class="rupee-sign">₹</span>
                                                  <span class="amount"
                                                      [text]="(productCatalog01.product1.qty*productCatalog01.product1.price).toFixed(2)">1500.00</span>
                                              </p>
                                              <input hidden name='101'
                                                  [value]="productCatalog01.product1.variantId == 101 ? productCatalog01.product1.qty:1" />
                                          </div>
                                          <div class="c-wrap">
                                              <p class="c-desc">is simply dummy text of the new age fashion industry.</p>
                                              <div class="btn-wrap">
                                                  <div class="product-count">
                                                      <div class="product-count-sign" tabindex="1" role on="tap:AMP.setState({
                                                          productCatalog01 : {
                                                              product1: {
                                                                  qty: productCatalog01.product1.qty > 0 ? productCatalog01.product1.qty - 1 : 0
                                                              }
                                                          }
                                                      })">
                                                          <amp-img layout="fixed"
                                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/minsu-icon.png"
                                                              alt="minus-icon" class="icon" width="13" height="13" />
                                                      </div>
                                                      <div class="product-count-value"
                                                          [text]="productCatalog01.product1.qty">0</div>
                                                      <div class="product-count-sign" tabindex="1" on="tap:AMP.setState({
                                                              productCatalog01 :{
                                                                  product1: {
                                                                      qty: productCatalog01.product1.qty < 5 ? productCatalog01.product1.qty + 1 : 5
                                                                  }
                                                              }
                                                          })">
                                                          <amp-img layout="fixed"
                                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/plus-icon.png"
                                                              alt="plus-icon" class="icon" width="13" height="13" />
                                                      </div>
                                                  </div>
                                                  <!-- Change CTA -->
                                                  <button type="button" class="catalog-cta"
                                                      on="tap:AMP.setState({productCatalog01 :{product1: {addedToCart:true}}})">
                                                      ADD TO CART
                                                  </button>
                                                            <!-- Change CTA -->
                                              </div>
                                          </div>
                                      </div>
                                  </div>
                                  <!-- Second product card -->
                                  <div class="catalog-card">
                                      <div class="catalog-img">
                                          <h3 class="offer-band">Get 20% off for your first purchase.</h3>
                                          <amp-img
                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/look-2.png"
                                              layout="responsive" alt="look" width="506" height="316" />
                                          <span class="cart-wrap">
                                              <span class="count" hidden [hidden]="productCatalog01.product2.qty <= 0"
                                                  [text]="productCatalog01.product2.qty"></span>
                                              <amp-img layout="fixed"
                                                  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                  alt="cart-icon" class="icon" width="27" height="27" />
                                          </span>
                                      </div>
                                      <div class="catalog-body">
                                          <div class="c-wrap">
                                              <h3 class="c-title">Opulent Essence</h3>
                                              <p class="c-amt">
                                                  <span class="rupee-sign">₹</span>
                                                  <span class="amount"
                                                      [text]="(productCatalog01.product2.qty*productCatalog01.product2.price).toFixed(2)">1500</span>
                                              </p>
                                              <input hidden name='102'
                                                  [value]="productCatalog01.product2.variantId == 102 ? productCatalog01.product2.qty:1" />
                                          </div>
                                          <div class="c-wrap">
                                              <p class="c-desc">is simply dummy text of the new age fashion industry.</p>
                                              <div class="btn-wrap">
                                                  <div class="product-count">
                                                      <div class="product-count-sign" tabindex="1" role on="tap:AMP.setState({
                                                              productCatalog01 : {
                                                                  product2: {
                                                                      qty: productCatalog01.product2.qty > 0 ? productCatalog01.product2.qty - 1 : 0
                                                                  }
                                                              }
                                                          })">
                                                          <amp-img layout="fixed"
                                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/minsu-icon.png"
                                                              alt="minus-icon" class="icon" width="13" height="13" />
                                                      </div>
                                                      <div class="product-count-value"
                                                          [text]="productCatalog01.product2.qty">0</div>
                                                      <div class="product-count-sign" tabindex="1" on="tap:AMP.setState({
                                                              productCatalog01 :{
                                                                  product2: {
                                                                      qty: productCatalog01.product2.qty < 5 ? productCatalog01.product2.qty + 1 : 5
                                                                  }
                                                              }
                                                          })">
                                                          <amp-img layout="fixed"
                                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/plus-icon.png"
                                                              alt="plus-icon" class="icon" width="13" height="13" />
                                                      </div>
                                                  </div>
                                                  <button type="button" class="catalog-cta"
                                                      on="tap:AMP.setState({productCatalog01 :{product2: {addedToCart:true}}})">
                                                      ADD TO CART
                                                  </button>
                                              </div>
                                          </div>
                                      </div>
                                  </div>
                                  <input hidden name="amount" [value]='(
                                      (productCatalog01.product1.qty * productCatalog01.product1.price) +
                                      (productCatalog01.product2.qty * productCatalog01.product2.price) +
                                      (productCatalog01.product3.qty * productCatalog01.product3.price) +
                                      (productCatalog01.product4.qty * productCatalog01.product4.price) +
                                      (productCatalog01.product5.qty * productCatalog01.product5.price)
                                  ).toFixed(2)' />
                              </div>
                          </div>
                      </div>
                      <!-- product section -->
                      <div class="bs-sec typ-product">
                          <div class="sec-head">
                              <h3 class="sec-title">Product Suggestions</h3>
                          </div>
                          <div class="sec-body">
                              <div class="container">
                                  <ul class="lyt-grid">
                                      <li class="grid-item">
                                          <div class="product-card">
                                              <div class="img-wrap">
                                                  <!-- Change image src as per your requirements -->
                                                  <amp-img layout="responsive"
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-3.png"
                                                      alt="product" width="150" height="177" />
                                              </div>
                                              <button type="button" class="p-cart-icon"
                                                  on="tap:AMP.setState({productCatalog01 :{product3: {addedToCart:true, qty:1}}})">
                                                  <amp-img layout="fixed"
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                      alt="cart-icon" class="icon" width="13" height="13"></amp-img>
                                              </button>
                                              <div class="product-info">
                                                  <div class="p-wrap">
                                                      <h3 class="p-title">Product name</h3>
                                                      <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                  </div>
                                                  <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                  </p>
                                              </div>
                                          </div>
                                      </li>
                                      <li class="grid-item">
                                          <div class="product-card">
                                              <div class="img-wrap">
                                                  <!-- Change image src as per your requirements -->
                                                  <amp-img layout="responsive"
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-2.png"
                                                      alt="product" width="150" height="177" />
                                              </div>
                                              <button type="button" class="p-cart-icon"
                                                  on="tap:AMP.setState({productCatalog01 :{product4: {addedToCart:true, qty:1}}})">
                                                  <amp-img layout="fixed"
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                      alt="cart-icon" class="icon" width="13" height="13" />
                                              </button>
                                              <div class="product-info">
                                                  <div class="p-wrap">
                                                      <h3 class="p-title">Product name</h3>
                                                      <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                  </div>
                                                  <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                  </p>
                                              </div>
                                          </div>
                                      </li>
                                      <li class="grid-item">
                                          <div class="product-card">
                                              <div class="img-wrap">
                                                  <!-- Change image src as per your requirements -->
                                                  <amp-img layout="responsive"
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/product-1.png"
                                                      alt="product" width="150" height="177" />
                                              </div>
                                              <button type="button" class="p-cart-icon"
                                                  on="tap:AMP.setState({productCatalog01 :{product5: {addedToCart:true, qty:1}}})">
                                                  <amp-img layout="fixed"
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/icon-cart.png"
                                                      alt="cart-icon" class="icon" width="13" height="13" />
                                              </button>
                                              <div class="product-info">
                                                  <div class="p-wrap">
                                                      <h3 class="p-title">Product name</h3>
                                                      <p class="p-amt"><span class="rupee-sign">₹</span>1500</p>
                                                  </div>
                                                  <p class="p-desc">Is simply dummy text of the new age fashion industry.
                                                  </p>
                                              </div>
                                          </div>
                                      </li>
                                  </ul>
                                  <div class="btn-wrap">
                                      <a href="https://google.com" class="shop-cta">Shop now
                                          <amp-img layout="fixed"
                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/arrow.png"
                                              alt="arrow" width="17" height="10"
                                              style="margin-left: 10px; max-width: 17px" />
                                      </a>
                                  </div>
                              </div>
                          </div>
                      </div>
                      <!-- product section -->
                      <!-- footer section -->
                      <footer class="cp-footer">
                          <div class="container">
                              <ul class="media-logo-list">
                                  <li class="logo-item">
                                      <a href="https://www.google.co.in/" class="logo-link">
                                          <amp-img layout="responsive"
                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-insta.png"
                                              alt="instagram" class="media-logo" width="20" height="20"></amp-img>
                                      </a>
                                  </li>
                                  <li class="logo-item">
                                      <a href="https://www.google.co.in/" class="logo-link">
                                          <amp-img layout="responsive"
                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-facebook.png"
                                              alt="facebook" class="media-logo" width="20" height="20"></amp-img>
                                      </a>
                                  </li>
                                  <li class="logo-item">
                                      <a href="https://www.google.co.in/" class="logo-link">
                                          <amp-img layout="responsive"
                                              src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Cart-Abandonment-HTML/logo-x.png"
                                              alt="x" class="media-logo" width="20" height="20"></amp-img>
                                      </a>
                                  </li>
                              </ul>
                              <p class="f-desc">is simply dummy text of the printing and typesetting industry. Lorem Ipsum
                                  has
                                  been the industry's standard dummy </p>
                                  <p class="f-desc" style="margin-top: 20px;">To stop receiving these emails, <a href="https://www.google.com" style="color:#ffff;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
                          </div>
                      </footer>
                      <!-- footer section -->
                  </div>
                  <div class="step2" hidden [hidden]="productCatalog01.currentStep != 2">
                      <div class="container">
                          <div class="bs-sec typ-bottom-padding-zero" [hidden]="
                              (productCatalog01.product1.qty <= 0 &&
                              productCatalog01.product2.qty <= 0 &&
                              productCatalog01.product3.qty <= 0 &&
                              productCatalog01.product4.qty <= 0 &&
                              productCatalog01.product5.qty <= 0)
                                      ">
                              <div class="sec-head">
                                  <h3 class="sec-title typ-2">PRODUCTS</h3>
                              </div>
                              <div class="sec-body">
                                  <ul class="product-list">
                                      <li class="product-item" [hidden]="productCatalog01.product1.qty == 0">
                                          <div class="lhs">
                                              <h3 class="p-name" [text]="productCatalog01.product1.title">Mystic Elixir
                                              </h3>
                                              <p class="p-desc"> is simply dummy text of the new age fashion industry.</p>
                                              <p class="p-quality">Qty : <span
                                                      [text]="productCatalog01.product1.qty"></span></p>
                                          </div>
                                          <div class="rhs">
                                              <button class="delete-icon" on="tap:AMP.setState({
                                                      productCatalog01 :{
                                                          product1: {addedToCart:false, qty:0}
                                                      }
                                                  })">
                                                  <amp-img
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                      width="24" height="24" layout="fixed" alt="delete-icon">
                                                  </amp-img>
                                              </button>
                                              <p class="p-amt">₹ <span
                                                      [text]="(productCatalog01.product1.qty*productCatalog01.product1.price).toFixed(2)"></span>
                                              </p>
                                          </div>
                                      </li>
                                      <li class="product-item" [hidden]="productCatalog01.product2.qty == 0">
                                          <div class="lhs">
                                              <h3 class="p-name" [text]="productCatalog01.product2.title">Mystic Elixir
                                              </h3>
                                              <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                              <p class="p-quality">Qty : <span
                                                      [text]="productCatalog01.product2.qty"></span></p>
                                          </div>
                                          <div class="rhs">
                                              <button class="delete-icon" on="tap:AMP.setState({
                                                      productCatalog01 :{
                                                          product2: {addedToCart:false, qty:0}
                                                      }
                                                  })">
                                                  <amp-img
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                      width="24" height="24" layout="fixed" alt="delete-icon">
                                                  </amp-img>
                                              </button>
                                              <p class="p-amt">₹ <span
                                                      [text]="(productCatalog01.product2.qty*productCatalog01.product2.price).toFixed(2)"></span>
                                              </p>
                                          </div>
                                      </li>
                                      <li class="product-item" [hidden]="productCatalog01.product3.qty == 0">
                                          <div class="lhs">
                                              <h3 class="p-name" [text]="productCatalog01.product3.title">Product Name
                                              </h3>
                                              <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                              <p class="p-quality">Qty : <span
                                                      [text]="productCatalog01.product3.qty"></span></p>
                                          </div>
                                          <div class="rhs">
                                              <button class="delete-icon" on="tap:AMP.setState({
                                                      productCatalog01 :{
                                                          product3: {addedToCart:false, qty:0}
                                                      }
                                                  })">
                                                  <amp-img
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                      width="24" height="24" layout="fixed" alt="delete-icon">
                                                  </amp-img>
                                              </button>
                                              <p class="p-amt">₹ <span
                                                      [text]="(productCatalog01.product3.qty*productCatalog01.product3.price).toFixed(2)"></span>
                                              </p>
                                          </div>
                                      </li>
                                      <li class="product-item" [hidden]="productCatalog01.product4.qty == 0">
                                          <div class="lhs">
                                              <h3 class="p-name" [text]="productCatalog01.product4.title">Product Name
                                              </h3>
                                              <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                              <p class="p-quality">Qty : <span
                                                      [text]="productCatalog01.product4.qty"></span></p>
                                          </div>
                                          <div class="rhs">
                                              <button class="delete-icon" on="tap:AMP.setState({
                                                      productCatalog01 :{
                                                          product4: {addedToCart:false, qty:0}
                                                      }
                                                  })">
                                                  <amp-img
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                      width="24" height="24" layout="fixed" alt="delete-icon">
                                                  </amp-img>
                                              </button>
                                              <p class="p-amt">₹ <span
                                                      [text]="(productCatalog01.product4.qty*productCatalog01.product4.price).toFixed(2)"></span>
                                              </p>
                                          </div>
                                      </li>
                                      <li class="product-item" [hidden]="productCatalog01.product5.qty == 0">
                                          <div class="lhs">
                                              <h3 class="p-name" [text]="productCatalog01.product5.title">Product Name
                                              </h3>
                                              <p class="p-desc">is simply dummy text of the new age fashion industry.</p>
                                              <p class="p-quality">Qty : <span
                                                      [text]="productCatalog01.product5.qty"></span></p>
                                          </div>
                                          <div class="rhs">
                                              <button class="delete-icon" on="tap:AMP.setState({
                                                      productCatalog01 :{
                                                          product5: {addedToCart:false, qty:0}
                                                      }
                                                  })">
                                                  <amp-img
                                                      src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/delete-icon.png"
                                                      width="24" height="24" layout="fixed" alt="delete-icon">
                                                  </amp-img>
                                              </button>
                                              <p class="p-amt">₹ <span
                                                      [text]="(productCatalog01.product5.qty*productCatalog01.product5.price).toFixed(2)"></span>
                                              </p>
                                          </div>
                                      </li>
                                      <li class="product-item typ-final">
                                          <div class="lhs">
                                              <h3 class="p-total">Amount Total</h3>
                                          </div>
                                          <div class="rhs">
                                              <p class="p-amt p-total-amt">₹
                                                  <span [text]="(
                                                      (
                                                          (productCatalog01.product1.qty * productCatalog01.product1.price) +
                                                          (productCatalog01.product2.qty * productCatalog01.product2.price) +
                                                          (productCatalog01.product3.qty * productCatalog01.product3.price) +
                                                          (productCatalog01.product4.qty * productCatalog01.product4.price) +
                                                          (productCatalog01.product5.qty * productCatalog01.product5.price)
                                                      ) * (100 - 0) / 100
                                                  ).toFixed(2) + ' '">0</span>
                                              </p>
                                          </div>
                                      </li>
                                  </ul>
                              </div>
                          </div>
                          <div class="bs-sec">
                              <div class="sec-head ">
                                  <h3 class="sec-title typ-2">ADD DETAILS</h3>
                              </div>
                              <div class="sec-body">
                                  <ul class="form-list">
                                      <!-- First Name -->
                                      <li class="form-item">
                                          <input id="productCatalog01-first_name" required on="
                                              change:AMP.setState({
                                                  productCatalog01: { first_name: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { first_name_invalid: event.target.validity.valueMissing }
                                              })
                                          " type="text" name="first_name" class="input" placeholder="First name" [value]="productCatalog01.first_name" [aria-invalid]="formValidation.first_name_invalid" aria-describedby="productCatalog01.first_name">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-first_name" id="productCatalog01.first_name">
                                              First name is required.
                                          </div>
                                      </li>
                                      <!-- Last Name -->
                                      <li class="form-item">
                                          <input id="productCatalog01-last_name" required on="
                                              change:AMP.setState({
                                                  productCatalog01: { last_name: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { last_name_invalid: event.target.validity.valueMissing }
                                              })
                                          " type="text" name="last_name" class="input" placeholder="Last name" [value]="productCatalog01.last_name" [aria-invalid]="formValidation.last_name_invalid" aria-describedby="formValidation.last_name_invalid">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-last_name" id="formValidation.last_name_invalid">
                                              Last name is required.
                                          </div>
                                      </li>
                                      <!-- Phone Number -->
                                      <li class="form-item">
                                          <input id="productCatalog01-phoneNumber" required [pattern]="productCatalog01.currentStep==2 ? '\\d{10}' : '*'" on="
                                              change:AMP.setState({
                                                  productCatalog01: { phoneNumber: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { phoneNumber_invalid: event.target.validity.valueMissing || event.target.validity.patternMismatch }
                                              })
                                          " maxlength="10" type="text" name="phoneNumber" class="input" placeholder="Phone Number" [value]="productCatalog01.phoneNumber" pattern="\d{10}" [aria-invalid]="formValidation.phoneNumber_invalid" aria-describedby="productCatalog01.phoneNumber">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-phoneNumber" id="productCatalog01.phoneNumber">
                                              Phone number is required.
                                          </div>
                                          <div class="error-msg" visible-when-invalid="patternMismatch" validation-for="productCatalog01-phoneNumber">
                                              Please enter a valid phone number.
                                          </div>
                                      </li>
                                      <!-- Email -->
                                      <li class="form-item">
                                          <input id="productCatalog01-email" required type="email" on="
                                              change:AMP.setState({
                                                  productCatalog01: { email: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { email_invalid: event.target.validity.valueMissing || event.target.validity.typeMismatch }
                                              })
                                          " name="email" class="input" placeholder="E-mail" [value]="productCatalog01.email" [aria-invalid]="formValidation.email_invalid" aria-describedby="productCatalog01.email">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-email" id="productCatalog01.email">
                                              Email is required.
                                          </div>
                                          <div class="error-msg" visible-when-invalid="patternMismatch" validation-for="productCatalog01-email">
                                              Please enter a valid Email.
                                          </div>
                                      </li>
                                      <!-- Address -->
                                      <li class="form-item typ-full">
                                          <input id="productCatalog01-address" required on="
                                              change:AMP.setState({
                                                  productCatalog01: { address: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { address_invalid: event.target.validity.valueMissing }
                                              })
                                          " name="address" class="input" placeholder="Address" [value]="productCatalog01.address" [aria-invalid]="formValidation.address_invalid" aria-describedby="productCatalog01.address">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-address" id="productCatalog01.address">
                                              Address is required.
                                          </div>
                                      </li>
                                      <!-- Landmark -->
                                      <li class="form-item">
                                          <input id="productCatalog01-landmark" required on="
                                              change:AMP.setState({
                                                  productCatalog01: { landmark: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { landmark_invalid: event.target.validity.valueMissing }
                                              })
                                          " name="landmark" class="input" placeholder="Landmark" [value]="productCatalog01.landmark" [aria-invalid]="formValidation.landmark_invalid" aria-describedby="productCatalog01.landmark">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-landmark" id="productCatalog01.landmark">
                                              Landmark is required.
                                          </div>
                                      </li>
                                      <!-- Pincode -->
                                      <li class="form-item">
                                          <input id="productCatalog01-pincode" required on="
                                              change:AMP.setState({
                                                  productCatalog01: { pincode: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { pincode_invalid: event.target.validity.valueMissing }
                                              })
                                          " name="pincode" class="input" placeholder="Pincode" [value]="productCatalog01.pincode" maxlength="6" type="number" [aria-invalid]="formValidation.pincode_invalid" aria-describedby="productCatalog01.pincode">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-pincode" id="productCatalog01.pincode">
                                              Pincode is required.
                                          </div>
                                      </li>
                                      <!-- City -->
                                      <li class="form-item">
                                          <input id="productCatalog01-city" required on="
                                              change:AMP.setState({
                                                  productCatalog01: { city: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { city_invalid: event.target.validity.valueMissing }
                                              })
                                          " type="text" name="city" class="input" placeholder="City" [value]="productCatalog01.city" [aria-invalid]="formValidation.city_invalid" aria-describedby="productCatalog01.city">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-city" id="productCatalog01.city">
                                              City is required.
                                          </div>
                                      </li>
                                      <!-- State -->
                                      <li class="form-item">
                                          <input id="productCatalog01-state" required on="
                                              change:AMP.setState({
                                                  productCatalog01: { state: event.value }
                                              });
                                              tap:AMP.setState({
                                                  formValidation: { state_invalid: event.target.validity.valueMissing }
                                              })
                                          " type="text" name="state" class="input" placeholder="State" [value]="productCatalog01.state" [aria-invalid]="formValidation.state_invalid" aria-describedby="productCatalog01.state">
                                          <div class="error-msg" visible-when-invalid="valueMissing" validation-for="productCatalog01-state" id="productCatalog01.state">
                                              State is required.
                                          </div>
                                      </li>
                                      <!-- Payment Mode -->
                                      <li class="form-item typ-full mt-32">
                                          <label for="cod" class="field-wrap">
                                              <input type="radio" checked="checked" id="cod" name="payment" required on="
                                                  change:AMP.setState({
                                                      productCatalog01: { payment_mode: 'cod' }
                                                  })
                                              " [value]="productCatalog01.payment_mode" class="user-valid valid" value="">
                                              <span class="checkmark"></span>
                                              Cash on Delivery
                                          </label>
                                          <label class="field-wrap" for="online">
                                              <input type="radio" id="online" name="payment" on="
                                                  change:AMP.setState({
                                                      productCatalog01: { payment_mode: 'online' }
                                                  })
                                              " [value]="productCatalog01.payment_mode" class="user-valid valid" value="">
                                              <span class="checkmark"></span>
                                              Online
                                          </label>
                                      </li>
                                      <!-- Submit Button -->
                                      <li class="form-item typ-full">
                                          <button class="form-btn" on="
                                              tap:AMP.setState({
                                                  formValidation: {
                                                      first_name_invalid: !productCatalog01.first_name,
                                                      last_name_invalid: !productCatalog01.last_name,
                                                      phoneNumber_invalid: !productCatalog01.phoneNumber || !/^\d{10}$/.test(productCatalog01.phoneNumber),
                                                      email_invalid: !productCatalog01.email,
                                                      address_invalid: !productCatalog01.address,
                                                      landmark_invalid: !productCatalog01.landmark,
                                                      pincode_invalid: !productCatalog01.pincode,
                                                      city_invalid: !productCatalog01.city,
                                                      state_invalid: !productCatalog01.state,
                                                  },
                                                  productCatalog01: { currentStep: 3 }
                                              })
                                          ">
                                              Next
                                          </button>
                                      </li>
                                  </ul>
                              </div>
                          </div>
                      </div>
                  </div>
                  <div class="step3" hidden [hidden]="productCatalog01.currentStep != 3">
                      <div class="modal-overlay">
                          <div class="modal">
                              <div class="modal-content">
                                  <div class="modal-head">
                                      <span class="close">x</span>
                                  </div>
                                  <div class="modal-body">
                                      <h3 class="m-title">THANKS for shopping</h3>
                                      <p class="m-desc">
                                          is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                                          been the
                                          industry's standard dummy text ever since the 1500s
                                      </p>
                                  </div>
                              </div>
                          </div>
                      </div>
                  </div>
                  <div class="step4" hidden submit-error>
                      <div class="modal-overlay">
                          <div class="modal hidden">
                              <div class="modal-content">
                                  <div class="modal-head">
                                      <span class="close">x</span>
                                  </div>
                                  <div class="modal-body">
                                      <h3 class="m-title">Error</h3>
                                      <p class="m-desc">
                                          is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                                          been the
                                          industry's standard dummy text ever since the 1500s
                                      </p>
                                  </div>
                              </div>
                          </div>
                      </div>
                  </div>
              </form>
          </div>
      </div>
  </body>
  </html>
  ```
</Accordion>

## Scratch Card for Discount Template

This AMP template delivers a gamified experience within the email itself. It allows users to interact with a digital scratch card to reveal a hidden offer, discount, or reward, creating a sense of anticipation and delight. This interactive approach helps increase user engagement, click-through rates, and overall campaign excitement.

<Image align="center" alt="Sample Scratch Card for Disvount Template" border={true} caption="Sample Scratch Card for Discount Template" src="https://files.readme.io/6c1580151c3f71e5c0e240e27b725ed9654d7fd990fbecae359e9c3217b6a57a-Scratch_Card_for_Discount_AMP.png" width="35% " />

<Accordion title="Expand to know more about the template.">
  ### Use Case Examples

  * Launch surprise reward campaigns to boost conversions.
  * Drive festive or seasonal promotions with a gamified touch.
  * Encourage user engagement with loyalty program perks.
  * Re-engage inactive users with a “Scratch To Unlock” coupon or deal.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)

  ### Template Code

  ```html
  <!doctype html>
    <html ⚡4email data-css-strict>
    <head>
    <meta charset="utf-8">
    <script async src="https://cdn.ampproject.org/v0.js"></script>
    <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script> 
    <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script> 
    <style amp4email-boilerplate> body { visibility: hidden } </style>
    <style amp-custom> * { margin: 0; padding: 0; }
    body { font-family: "Helvetica", arial, sans-serif; font-weight: 400; }
    img { width: 100%; height: auto; object-fit: cover; }
    .main { max-width: 600px; margin: 0 auto; background: url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/bg.png); background-repeat: no-repeat; background-position: center; padding: 40px 40px 60px; }
    .hide { display: none; }
    .show { display: block; }
    .scratch-img-wrap { background: transparent; border: 0; outline: none; cursor: pointer; }
    @media screen and (max-width: 600px) { .main { padding: 20px; }
    .heading { font-size: 30px; line-height: 40px; }
    .coupon { font-size: 24px; line-height: 32px; }
    .scratch-img-wrap { width: 100%; height: auto; }
    .scratch-code { padding: 15px 10px; } }
    .promo { margin: 0 auto; position: relative; transform-style: preserve-3d; border-radius: 8px; border: 2px solid #d1d1d1; overflow: hidden; height: 120px; width: 450px; background-color: transparent; }
    .promo .scratch { position: absolute; top: 0; right: 0; bottom: 0; left: 0; display: flex; flex-wrap: wrap; overflow: hidden; cursor: pointer }
    .promo .scratch u { display: block; width: 10%; height: 10%; background: rgb(2, 0, 36); background: #e3e3e3; /* Golden color */ transform: rotate(0) translateY(0) scale(1.7); transition: transform 0s; transition-delay: 9999s; opacity: .99; }
    .promo.auto .scratch u:nth-of-type(1n) { transition-delay: 2.25s }
    .promo.auto .scratch u:nth-of-type(10n-11) { transition-delay: 0s }
    .promo.auto .scratch u:nth-of-type(10n-8) { transition-delay: .25s }
    .promo.auto .scratch u:nth-of-type(10n-10) { transition-delay: .5s }
    .promo.auto .scratch u:nth-of-type(12n-9) { transition-delay: .75s }
    .promo.auto .scratch u:nth-of-type(12n-12) { transition-delay: 1s }
    .promo.auto .scratch u:nth-of-type(12n-7) { transition-delay: 1.25s }
    .promo.auto .scratch u:nth-of-type(13n-13) { transition-delay: 1.5s }
    .promo.auto .scratch u:nth-of-type(13n-6) { transition-delay: 1.75s }
    .promo.auto .scratch u:nth-of-type(13n-14) { transition-delay: 2s }
    .promo .scratch u:hover, .promo.auto .scratch u { transform: scale(0); transition-delay: 0s }
    .offer { justify-content: center; text-align: center; margin-top: 25px; /* Center aligns the content */ color: white; /* Sets text color to white */ font-weight: bold; /* Makes "You Won!" text bold */ font-size: 20px; /* Adjust size if necessary */ }
    .coupon-code { margin-top: 10px; /* Adds some space above the coupon code */ font-size: 24px; /* Adjust coupon code font size */ font-weight: bold; /* Makes the coupon code bold */ color: white; /* White text for the coupon code */ background-color: rgba(0, 0, 0, 0.7); /* Optional: add a semi-transparent background */ padding: 5px 10px; /* Add padding for better visibility */ border-radius: 4px; /* Rounded corners for the coupon box */ display: inline-block; /* Ensures proper alignment and box behavior */ }
    .black-but { margin-top: 20px; padding: 10px; }
    /* Additional Media Queries for smaller screens */ @media screen and (max-width: 600px) { .main { padding: 20px; }
    .heading { font-size: 30px; line-height: 40px; }
    .coupon { font-size: 24px; line-height: 32px; }
    .scratch-img-wrap { width: 100%; height: auto; }
    .scratch-code { padding: 15px 10px; } }
    /* More media queries for smaller screens */ @media screen and (max-width: 400px) { .main { padding: 15px; }
    .heading { font-size: 28px; line-height: 35px; }
    .coupon { font-size: 22px; line-height: 30px; }
    .scratch-img-wrap { width: 100%; height: auto; }
    .coupon-code { font-size: 20px; padding: 4px 8px; }
    .offer { font-size: 18px; }
    .promo { width: 100%; height: auto; } }
    /* Media queries for very small screens */ @media screen and (max-width: 300px) { .promo { width: 100%; height: auto; }
    .offer { font-size: 16px; }
    .coupon-code { font-size: 18px; padding: 3px 6px; } } 
    </style>
    </head>
    <body>
    <table border="0" cellpadding="0" cellspacing="0" class="main" role="presentation" width="100%">
    <!-- header start--> 
    <tbody>
    <tr>
    <td style="text-align: center; vertical-align: middle; margin-bottom: 40px;">
    <!-- Logo Image--> 
    <div class="logo" style="background: url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/logobg.png);background-repeat: no-repeat; background-position: center;">
    <amp-img layout="fixed" alt="Logo" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" width="127" height="60" />
    </div>
    <!-- Logo Image--> 
    </td>
    </tr>
    <tr>
    <td style="text-align: center;">
    <h2 class="heading" style="color:#ffffff; font-family: 'Poppins', Arial, sans-serif; font-size: 45px; font-weight: 700; line-height: 68px; margin-top: 20px;"> Mid-Season Sale</h2>
    </td>
    </tr>
    <tr>
    <!-- Banner Image --> 
    <td>
    <amp-img layout="responsive" alt="banner image" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Scratch%20Card/offer.png" width="407" height="462" />
    </td>
    <!-- Banner Image --> 
    </tr>
    <tr>
    <td style="text-align: center;">
    <p class="coupon" style="color:#ffffff; font-family: 'Poppins', Arial, sans-serif; font-size: 34px; font-weight: 600; margin-bottom: 20px;"> SCRATCH TO SEE CODE</p>
    </td>
    </tr>
    <!-- Footer Section --> 
    <tr>
    <td style="text-align: center;">
    <div class="container" id="&#x201D;scratch-card-widget&#x201D;">
    <div class="promo" [class]="auto == true ? 'promo auto' : 'promo'">
    <div class="scratch"> <u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u><u></u> </div>
    <div class="offer">
    You Won! 🎉 
    <div class="coupon-code">CODE1234</div>
    </div>
    </div>
    <p><button class="black-but" type="button" on="tap:AMP.setState({auto: true})">Scratch at once</button> </p>
    </div>
    </td>
    </tr>
    <!-- Footer Section --> 
    </tbody>
    </table>
    </body>
    </html>
  ```
</Accordion>

## Spin and Win Template

This AMP template adds a fun, gamified interaction to your email by letting users spin a virtual wheel to unlock a discount, reward, or surprise offer, directly within the email. This interactive format helps boost engagement and click-through rates while creating a sense of excitement and urgency.

<Image align="center" alt="Sample Spin and Win Template" border={true} caption="Sample Spin and Win Template" src="https://files.readme.io/594d05fecaa9eed2dbcebb6afc6d2a4ccf4afc92200373f4a5f94e9c72c40e42-Spin_and_Win_AMP.png" width="35% " />

<Accordion title="My Accordion Title" icon="fa-info-circle">
  ### Use Case Examples

  * Drive conversions during sales events or festivals with spin-to-win deals.
  * Run promotional campaigns that reward users with random offers.
  * Re-engage dormant users with a playful incentive.
  * Launch loyalty or referral-based programs with interactive rewards.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Replace Background](doc:ootb-email-templates#replace-background)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!DOCTYPE html>
<html ⚡4email data-css-strict>

<head>
<meta charset="utf-8" />
<script async src="https://cdn.ampproject.org/v0.js"></script>
<script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
<style amp4email-boilerplate>
body {
visibility: hidden;
}
</style>
<style amp-custom>
* {
margin: 0;
padding: 0;
}

body {
font-family: arial, sans-serif;
font-weight: 400;
margin: 0;
padding: 0;
background: #939393;
}

img {
width: 100%;
height: 100%;
object-fit: cover;
}

.main {
font-family: Arial, sans-serif;
max-width: 600px;
margin: 0 auto;
background: #fe592c;
}

@media only screen and (max-width: 400px) {
.main {
max-width: 95%;
}
}

.header-container {
background: transparent url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/header-design.png);
background-size: contain;
background-repeat: repeat-x;
background-position: bottom;
padding-bottom: 18px;
}

.logo-wrap {
background-color: #ffffff;
padding: 20px 0;
}

.logo-wrap .img-wrap {
width: 100%;
max-width: 145px;
max-height: 74px;
margin: 0 auto;
}

.container,
.wrapper {
position: relative;
}

.main-content {
position: relative;
}

.common-wrap .orange-triangle {
width: 100%;
height: 360px;
background: #f34626;
position: absolute;
bottom: 0;
left: 0;
transform: rotate(180deg);
}

.common-wrap .content-wrap {
max-width: 85%;
margin: 90px auto 0;
padding-bottom: 120px;
}

.top-content .title {
font-family: Arial, sans-serif;
font-size: 42px;
font-weight: 500;
color: #ffffff;
line-height: 46px;
text-align: center;
text-transform: none;
margin-bottom: 22px;
}

.top-content .sub-title {
font-family: Arial, sans-serif;
font-size: 16px;
font-weight: 500;
line-height: 22px;
text-align: center;
color: #ffffff;
text-transform: none;
margin-bottom: 11px;
}

.top-content .desc {
font-family: Arial, sans-serif;
font-size: 12px;
font-weight: 400;
line-height: 18px;
text-align: center;
text-transform: none;
color: #ffffff;
max-width: 70%;
margin: 0 auto 55px;
}

.wheel-spin-gif-box,
.wheel-spin-box {
max-width: 450px;
max-height: 450px;
position: relative;
overflow: hidden;
margin: 0 auto;
}

.ticker {
position: absolute;
top: 50%;
transform: translateY(-50%);
right: 0;
z-index: 2;
}

.btn-wrap {
text-align: center;
position: relative;
}

.spin-btn {
margin-top: -80px;
background: #ffffff;
box-shadow: 0px 3.29px 3.29px 0px #00000040;
width: 100%;
max-width: 242px;
height: auto;
max-height: 52px;
display: inline-block;
border-radius: 50px;
padding: 18px 20px;
font-size: 18px;
font-weight: 400;
line-height: 20px;
text-align: center;
text-decoration: none;
text-transform: none;
color: #ffae97;
border: 0;
outline: none;
cursor: pointer;
position: absolute;
top: -25px;
left: 50%;
transform: translateX(-50%);
}

@media (max-width: 768px) {
.spin-btn {
max-width: 200px;

font-size: 16px;

padding: 16px 18px;

}
}

@media (max-width: 480px) {
.spin-btn {
max-width: 150px;

font-size: 14px;

padding: 12px 15px;

margin-top: -40px;

}
}

@media (max-width: 320px) {
.spin-btn {

max-width: 120px;

font-size: 12px;

padding: 10px 12px;

}
}


.spin-btn.typ-2 {
color: #FE592C;
}

.img-wrap {
width: 73px;
height: 93px;
}

.hidden {
display: none;
}

.yellow-wrap {
max-width: 401px;
min-height: 300px;
margin: 0 auto 14px;
}

.result-content {
font-size: 28px;
font-weight: 400;
line-height: 38px;
text-align: center;
color: #ffffff;
text-transform: none;
position: relative;
z-index: 1;
}

.cm-bold {
font-weight: 700;
display: block;
}

.footer {
border-top: 0.5px solid #ffff;
background: #ffff;
}

.media-logo-list {
display: flex;
justify-content: center;
align-items: center;
list-style: none;
gap: 23px;
margin: 65px 0 17px;
}

.media-logo-list .logo-item {
width: 20px;
height: 20px;
}

.media-logo-list .logo-item .logo-link {
width: 100%;
height: 100%;
display: inline-block;
}

.f-desc {
font-size: 14px;
font-weight: 400;
line-height: 24px;
color: #939393;
text-align: center;
max-width: 80%;
margin: 0 auto;
padding-bottom: 27px;
text-transform: none;
}

.f-nav-list {
padding: 27px 0;
display: flex;
justify-content: center;
align-items: center;
list-style: none;
border-top: 0.5px solid #979797;
}

.f-nav-list .f-nav-item {
margin: 0 5px;
}

.f-nav-list .f-nav-item .f-nav-link {
font-size: 14px;
font-weight: 400;
line-height: 24px;
text-align: center;
color: #939393;
text-decoration: none;
}

@media only screen and (max-width: 480px) {
.logo-wrap {
padding: 25px 0;
}

.spin-btn {
max-width: 200px;
font-size: 14px;
line-height: 18px;
}

.top-content .desc {
margin: 0 auto 40px;
max-width: 80%;
}

.header-container {
background-size: auto;
}

.common-wrap .content-wrap {
max-width: 90%;
margin: 60px auto 0;
padding-bottom: 80px;
}

.top-content .title {
font-size: 30px;
line-height: 40px;
margin-bottom: 10px;
}

.f-desc {
line-height: 20px;
}

.logo-wrap .img-wrap {
width: 100%;
max-width: 130px;
max-height: 60px;
margin: 0 auto;
}
}
</style>
</head>

<body>
<amp-state id="step">
<script type="application/json">
{
"step": 1
}
</script>
</amp-state>
<div class="main">
<!-- header section -->
<header>
<div class="header-container">
<div class="logo-wrap">
<div class="img-wrap">
<amp-img layout="responsive"
src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo"
width="159" height="73" />
</div>
</div>
</div>
</header>
<!-- header section -->
<!-- main content section -->
<div class="main-content">
<div class="common-wrap">
<div class="orange-triangle"></div>
<div class="content-wrap">
<div class="top-content">
<h1 class="title">SPIN AND WIN</h1>
<h2 class="sub-title">Try your luck and grab an exclusive reward!</h2>
<p class="desc">
We’ve loaded up the wheel with rewards you’ll love — all you have to do is spin.
</p>
</div>
<div class="bottom-content">
<div class="wrapper">
<!--<div class="ticker">
<amp-img
layout="fixed"
src="./images/icon-arrow.png"
alt="ticker"
class="ticker-icon"
width="80"
height="50">
</amp-img>
</div> -->
<div class="step-1" [hidden]="step != 1">
<div class="wheel-spin-box">
<amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/wheel-start.png"
layout="responsive" width="450" height="450" role="button" tabindex="0" layout="responsive">
</amp-img>
</div>
</div>
<div class="step-2" hidden [hidden]="step != 2">
<div class="wheel-spin-gif-box">
<amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/spin-wheel.gif"
layout="responsive" width="450" height="450" role="button" tabindex="0" layout="responsive">
</amp-img>
</div>
</div>
<div class="step-3" hidden [hidden]="step != 3">
<div class="wheel-spin-box">
<amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/wheel-win.png"
layout="responsive" width="450" height="450" role="button" tabindex="0" layout="responsive">
</amp-img>
</div>
</div>
</div>

<!-- Result Section -->
<div class="result-wrapper step-4" hidden [hidden]="step != 4">
<div class="yellow-wrap">
<amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/result-tshirt.png"
width="490" height="350" layout="responsive" alt="result image">
</amp-img>
</div>
<h2 class="result-content">
Congratulations, you win
<span class="cm-bold">A Half white T-Shirt!</span>
</h2>
</div>
</div>
</div>
</div>
<div class="btn-wrap">
<button class="spin-btn typ-2" [hidden]="step != 1" on="tap:AMP.setState({ step: 2 })"> Spin the Wheel </button>
<button class="spin-btn typ-2" hidden [hidden]="step != 2" on="tap:AMP.setState({ step: 3 })">Stop the
Wheel</button>
<button class="spin-btn typ-2" hidden [hidden]="step != 3" on="tap:AMP.setState({ step: 4 })">Get now</button>
<a href="https://www.google.com" class="spin-btn typ-2" hidden [hidden]="step != 4"
on="tap:AMP.setState({ step: 4 })">Shop now</a>
</div>
</div>
<!-- main content section -->
<!-- footer start -->
<footer class="footer">
<ul class="media-logo-list">
<li class="logo-item">
<a href="https://www.google.co.in/" class="logo-link">
<amp-img layout="fixed" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/5c06fdefb77c4f6c94c17f953b0e98e4.png"
alt="instagram" class="media-logo" width="20" height="20"></amp-img>
</a>
</li>
<li class="logo-item">
<a href="https://www.google.co.in/" class="logo-link">
<amp-img layout="fixed"
src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/afb3cd0c5d954fca8702c0401e1bf97b.png" alt="facebook"
class="media-logo" width="20" height="20"></amp-img>
</a>
</li>
<li class="logo-item">
<a href="https://www.google.co.in/" class="logo-link">
<amp-img layout="fixed" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/8b474f3170b346318eade16ae1fc3f63.png"
alt="x" class="media-logo" width="20" height="20"></amp-img>
</a>
</li>
</ul>
<p class="f-desc">
For assistance, connect with us on social media or reach out to our support team at 
<a href="https://google.com" style="color: #939393">support@example.com</a>
</p>
<p class="f-desc">
To opt out of promotional emails like this, <a href="https://google.com"
style="color:#fe592c;font-weight:bold;text-decoration:none;">unsubscribe here</a>
</p>
</footer>
<!-- footer end -->
</div>
</body>
    </html>
  ```
</Accordion>

## Quick Survey Form Template

This AMP template collects valuable user information and preferences for a more personalized shopping experience. This template helps brands understand their audience better.

<Image align="center" alt="Sample Customer Survey Form Template" border={true} caption="Sample Customer Survey Form Template" src="https://files.readme.io/73047359b602a87553b6b35c1c1a3431b7c98adfdd1a49a304c04ae15ec570d8-Customer_Survey_-1_AMP.png" width="25% " />

<Accordion title="My Accordion Title" icon="fa-info-circle">
  ### Use Case Examples

  * Gather customer preferences (for example, gender, favorite clothing items) to drive personalized product recommendations.
  * Use this form post-sale or post-subscription to understand satisfaction and expectations.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Replace Background](doc:ootb-email-templates#replace-background)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html Quick Customer Survey - Variant 1
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script><script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script><script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>body {visibility: hidden;}</style>
  <style amp-custom>* {margin: 0;padding: 0;}
  body {font-family: "Helvetica", Arial, sans-serif;font-weight: 400;}
  img {width: 100%;height: 100%;object-fit: cover;}
  /* Change Theme */.main {width: 100%;max-width: 600px;overflow: hidden;margin: 0 auto;background: #cecece;position: relative;}/* Change Theme */
  @media only screen and (max-width: 400px) {body .main {max-width: 95%;}}
  .logo-wrap {padding: 16px 0;background-color: #ffffff;}
  .logo-wrap .img-wrap {max-width: 146px;max-height: 75px;margin: 0 auto;}
  .footer {border-top: 0.5px solid #ffff;background: #ffff;}
  .media-logo-list {display: flex;justify-content: center;align-items: center;list-style: none;gap: 16px;margin: 39px 0 14px;}
  .media-logo-list .logo-item {width: 28px;height: 28px;}
  .media-logo-list .logo-item .logo-link {width: 100%;height: 100%;display: inline-block;}
  .f-desc {font-size: 14px;font-weight: 400;line-height: 24px;color: #939393;text-align: center;max-width: 65%;margin: 0 auto 27px;padding-bottom: 47px;}
  .f-nav-list {padding: 27px 0;display: flex;justify-content: center;align-items: center;list-style: none;border-top: 0.5px solid #979797;}
  .f-nav-list .f-nav-item {margin: 0 5px;}
  .f-nav-list .f-nav-item .f-nav-link {font-size: 14px;font-weight: 400;line-height: 24px;text-align: center;color: #939393;text-decoration: none;}
  .banner .img-wrap {max-height: 361px;width: 100%;}
  .success-container {text-align: center;background-color: rgba(206, 206, 206, 0.5);position: absolute;top: 0;left: 0;width: 100%;height: 100%;z-index: 10;}
  .success-container .success-wrap {max-width: 312px;width: 100%;position: relative;top: 20%;left: 50%;transform: translateX(-50%);background: #ffffff;padding: 60px 40px;}
  .success-wrap h4 {font-size: 16px;font-weight: 400;line-height: 27px;text-align: center;text-transform: uppercase;margin-bottom: 10px;}
  .success-wrap p {font-size: 12px;font-weight: 400;line-height: 20px;text-align: center;color: #909090;text-transform: none;}
  .container {max-width: 555px;margin: -30px auto 42px;position: relative;z-index: 2;}
  .form-container {padding: 33px 22px 26px 23px;background-color: #ffffff;box-shadow: 0px 8.26px 3.3px 0px #00000040;}
  .form-container h2 {font-size: 16px;font-weight: 400;line-height: 22px;color: #000000;margin-bottom: 8px;}
  .form-container p {font-size: 12px;font-weight: 400;line-height: 16px;color: #909090;margin-bottom: 20px;text-transform: none;}
  .form-container .form-field-wrap {display: flex;gap: 14px;flex-wrap: wrap;}
  .form-field-wrap .form-group {display: flex;flex-direction: column;max-width: 248px;width: 100%;}
  .form-group label {
  font-size: 12px;font-weight: 400;line-height: 16.52px;text-align: left;color: #000000;text-transform: none;margin-bottom: 5px;}
  .form-group input {padding: 5px 0 5px 8px;max-width: 248.65px;height: 27.26px;margin-bottom: 2px;font-size: 12px;font-weight: 400;line-height: 16.52px;text-align: left;color: #000000;text-transform: none;border: 0.83px solid #adadad;}
  .form-group input[type="date"] {text-transform: uppercase;}
  .form-group .label-wrap {display: flex;justify-content: space-between;}
  .form-group .label-wrap .remove .remove-logo {width: 16px;height: 16px;}
  .form-group.gender,.form-group.favorite,.form-group.purchase {margin-top: 16px;max-width: 100%;}
  .form-group select {flex-grow: 1;padding: 8px;border: 1px solid #ccc;border-radius: 4px;}
  .form-container .gender-options {display: flex;justify-content: space-between;margin-bottom: 16px;max-width: 130px;}
  .form-container .gender-options label {display: flex;align-items: center;max-width: 100px;width: 100%;margin: 0;font-size: 14px;font-weight: 400;line-height: 19.83px;text-align: center;}
  .gender-options input {margin-right: 6px;}
  .form-group.favorite {display: flex;flex-direction: column;margin-bottom: 5px;}
  .favorite select {font-size: 10px;font-weight: 400;line-height: 15px;text-align: left;background: #ffffff;color: #000000;border: 0.83px solid #ADADAD;border-radius: 0;}
  .favorite select option {width: 50px;font-size: 12px;}
  .form-container .checkbox {display: flex;flex-direction: column;margin-top: 5px;}
  .purchase .checkbox label {display: flex;align-items: center;max-width: 100px;width: 100%;
  font-size: 14px;font-weight: 400;line-height: 16.83px;text-align: center;margin-bottom: 11px;}
  .purchase .checkbox label input {margin-right: 6px;width: 14px;height: 14px;padding: 0;}
  .form-container .submit {padding: 7px 45px;background-color: #000000;color: #ffffff;border: none;cursor: pointer;text-transform: uppercase;font-size: 16px;font-weight: 400;line-height: 16.52px;text-align: left;position: relative;left: 50%;transform: translateX(-50%);margin-top: 10px;}
  .remove {background: transparent;border: none;outline: 0;}
  .hidden {display: none;}
  .show {display: block;}
  @media only screen and (max-width: 400px) {.f-desc {max-width: 80%;}}
  @media only screen and (max-width: 375px) {
  .form-field-wrap .form-group,.form-group input,.form-group input[type="date"],input#birth-date {max-width: 100%;width: 100%;}
  .favorite select {height: 27.26px;}
  input[type="radio"] {width: auto;}}
  </style>
  </head>
  <body>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <!-- Change Logo Image src as per your requirements -->
  <amp-img layout="responsive"src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo"width="146" height="75"></amp-img>
  <!-- Change Logo Image src as per your requirements -->
  </div>
  </div>
  </header>
  <div class="banner">
  <div class="img-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/banner.png"alt="Banner" width="600" height="361"></amp-img>
  </div>
  </div>
  <!-- Success Container - Initially Hidden -->
  <div class="success-container hidden"[class]="!successVisible ? 'success-container hidden' : 'success-container show'">
  <div class="success-wrap">
  <h4 class="title">Information saved</h4>
  <p class="para">Help us recommend products you'll love and create a personalized shopping experience just for you.</p>
  </div>
  </div>
  <div class="container">
  <div class="form-container">
  <h2>Tell us about you!</h2>
  <p>Help us recommend products you'll love and create a personalized shopping experience just for you.</p>
  <form method="post" class="form" action-xhr="https://google.com"on="submit-success:AMP.setState({successVisible: false})">
  <div class="form-field-wrap">
  <!-- First Name -->
  <div class="form-group">
  <div class="label-wrap"><label for="first-name">First Name</label></div>
  <input type="text" id="first-name" name="firstName" placeholder="Enter first name" [value]="firstName"on="input-debounced:AMP.setState({firstName: event.target.value}), change:AMP.setState({firstName: event.value})" />
  </div>
  <!-- Last Name -->
  <div class="form-group">
  <div class="label-wrap"><label for="last-name">Last Name</label></div>
  <input type="text" id="last-name" name="lastName" placeholder="Enter last name" [value]="lastName"on="input-debounced:AMP.setState({lastName: event.target.value}), change:AMP.setState({lastName: event.value})" />
  </div>
  <!-- Phone Number -->
  <div class="form-group">
  <div class="label-wrap"><label for="phone-number">Phone Number</label></div>
  <input type="tel" id="phone-number" name="phoneNumber" placeholder="Enter phone number" [value]="phoneNumber"on="input-debounced:AMP.setState({phoneNumber: event.target.value}), change:AMP.setState({phoneNumber: event.value})" />
  </div>
  <!-- Birth Date -->
  <div class="form-group">
  <div class="label-wrap"><label for="birth-date">Date of Birth</label></div>
  <input type="date" id="birth-date" name="birthDate" placeholder="Enter date" [value]="birthDate"on="input-debounced:AMP.setState({birthDate: event.target.value}), change:AMP.setState({birthDate: event.value})" />
  </div>
  <!-- Gender -->
  <div class="form-group gender">
  <div class="label-wrap"><label>Gender</label></div>
  <div class="gender-options"><label><input type="radio" name="gender" value="Male" checked /> Male</label><label><input type="radio" name="gender" value="Female" /> Female</label></div>
  </div>
  <!-- Favorite Clothing -->
  <div class="form-group favorite">
  <div class="label-wrap"><label for="clothing">Favorite clothing item</label></div>
  <select id="clothing" name="clothing" on="change:AMP.setState({clothing: event.value})">
  <option disabled selected>Select</option>
  <option value="Casual">Casual</option>
  <option value="Formal">Formal</option>
  <option value="Sportswear">Sportswear</option>
  </select>
  </div>
  <!-- Purchased Before -->
  <div class="form-group purchase">
  <div class="label-wrap"><label>Have you shopped with us before?</label></div>
  <div class="checkbox">
  <label>
  <input type="radio" name="purchasedBefore" value="Yes"
  on="change:AMP.setState({purchasedBefore: event.target.checked ? 'Yes' : ''})" /> Yes
  </label>
  <label>
  <input type="radio" name="purchasedBefore" value="No"
  on="change:AMP.setState({purchasedBefore: event.target.checked ? 'No' : ''})" /> No
  </label>
  </div>
  </div>
  <div class="btn-wrap" style="width:100%">
  <!-- Change CTA --><button type="submit" class="submit" on="tap:AMP.setState({successVisible: true})">Submit</button><!-- Change CTA -->
  </div>
  </div>
  </form>
  </div>
  </div>
  <!-- Footer Section -->
  <footer class="footer">
  <ul class="media-logo-list">
  <!-- Social Links -->
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4246683f26846a6a5966a72e37034d4.png" alt="instagram"class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/677a3f1dbf554cdc858f91cfd9c8c05d.png" alt="facebook"class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/dd65dffd70e34ccab634a38185229fd0.png" alt="x"class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <!-- Social Links -->
  </ul>
  <p class="f-desc">For assistance, connect with us on social media or reach out to our support team at support@example.com </p>
  <p class="f-desc">To opt out of promotional emails like this, <a href="https://google.com"style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
  </footer>
  <!-- Footer Section -->
  </div>
  </body>
  </html>
  ```
  ```html Quick Customer Survey - Variant 2
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  }
  img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }
  /* Change Theme */
  .main {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: 0 auto;
  background: #cecece;
  position: relative;
  }
  /* Change Theme */
  @media only screen and (max-width: 400px) {
  body .main {
  max-width: 95%;
  }
  }
  .logo-wrap {
  padding: 16px 0;
  background-color: #ffffff;
  }
  .logo-wrap .img-wrap {
  max-width: 146px;
  max-height: 75px;
  margin: 0 auto;
  }
  .footer {
  border-top: 0.5px solid #ffff;
  background: #ffff;
  }
  .media-logo-list {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  gap: 16px;
  margin: 39px 0 14px;
  }
  .media-logo-list .logo-item {
  width: 28px;
  height: 28px;
  }
  .media-logo-list .logo-item .logo-link {
  width: 100%;
  height: 100%;
  display: inline-block;
  }
  .f-desc {
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  color: #939393;
  text-align: center;
  max-width: 65%;
  margin: 0 auto 27px;
  padding-bottom: 47px;
  }
  .f-nav-list {
  padding: 27px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  border-top: 0.5px solid #979797;
  }
  .f-nav-list .f-nav-item {
  margin: 0 5px;
  }
  .f-nav-list .f-nav-item .f-nav-link {
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  text-align: center;
  color: #939393;
  text-decoration: none;
  }
  .banner .img-wrap {
  max-height: 361px;
  width: 100%;
  }
  .success-container {
  text-align: center;
  background-color: rgba(206, 206, 206, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 10;
  }
  .success-container .success-wrap {
  max-width: 312px;
  width: 100%;
  position: relative;
  top: 20%;
  left: 50%;
  transform: translateX(-50%);
  background: #ffffff;
  padding: 60px 40px;
  }
  .success-wrap h4 {
  font-size: 16px;
  font-weight: 400;
  line-height: 27px;
  text-align: center;
  text-transform: uppercase;
  margin-bottom: 10px;
  }
  .success-wrap p {
  font-size: 12px;
  font-weight: 400;
  line-height: 20px;
  text-align: center;
  color: #909090;
  text-transform: none;
  }
  .container {
  max-width: 555px;
  margin: -30px auto 42px;
  position: relative;
  z-index: 2;
  }
  .form-container {
  padding: 33px 22px 26px 23px;
  background-color: #ffffff;
  box-shadow: 0px 8.26px 3.3px 0px #00000040;
  }
  .form-container h2 {
  font-size: 16px;
  font-weight: 400;
  line-height: 22px;
  color: #000000;
  margin-bottom: 8px;
  }
  .form-container p {
  font-size: 12px;
  font-weight: 400;
  line-height: 16px;
  color: #909090;
  margin-bottom: 20px;
  text-transform: none;
  }
  .form-container .form-field-wrap {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  }
  .form-field-wrap .form-group {
  display: flex;
  flex-direction: column;
  width: 48%;
  }
  .form-group label {
  font-size: 12px;
  font-weight: 400;
  line-height: 16.52px;
  text-align: left;
  color: #000000;
  text-transform: none;
  margin-bottom: 8px;
  }
  .form-group input[type="text"],
  .form-group input[type="date"],
  .form-group input[type="tel"],
  .form-group input[type="number"] {
  padding: 5px 10px;
  width: 91%;
  height: 27.26px;
  margin-bottom: 2px;
  font-size: 12px;
  font-weight: 400;
  line-height: 16.52px;
  text-align: left;
  color: #000000;
  text-transform: none;
  border: 0.83px solid #adadad;
  }
  .form-group input[type="date"] {
  text-transform: uppercase;
  }
  .form-group .label-wrap {
  display: flex;
  justify-content: space-between;
  }
  .form-group .label-wrap .remove .remove-logo {
  width: 16px;
  height: 16px;
  }
  .form-group.full-width {
  margin-bottom: 15px;
  }
  .form-group.full-width input[type="text"] {
  width: 96%;
  }
  .form-group.feedback,
  .form-group.gender,
  .form-group.favorite,
  .form-group.purchase {
  margin-top: 16px;
  width: 100%;
  }
  .form-group select {
  flex-grow: 1;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
  }
  .form-container .gender-options {
  display: flex;
  justify-content: space-between;
  margin-bottom: 16px;
  max-width: 130px;
  }
  .form-container .gender-options label {
  display: flex;
  align-items: center;
  max-width: 100px;
  width: 100%;
  margin: 0;
  font-size: 14px;
  font-weight: 400;
  line-height: 19.83px;
  text-align: center;
  }
  .gender-options input[type="radio"] {
  margin-right: 6px;
  }
  .form-group.favorite {
  display: flex;
  flex-direction: column;
  margin-bottom: 5px;
  }
  .favorite select {
  font-size: 10px;
  font-weight: 400;
  line-height: 15px;
  text-align: left;
  background: #ffffff;
  color: #000000;
  border: 0.83px solid #ADADAD;
  border-radius: 0;
  }
  .favorite select option {
  width: 50px;
  font-size: 12px;
  }
  .form-container .checkbox {
  display: flex;
  flex-direction: column;
  margin-top: 5px;
  }
  .purchase .checkbox label {
  display: flex;
  align-items: center;
  max-width: 100px;
  width: 100%;
  font-size: 14px;
  font-weight: 400;
  line-height: 16.83px;
  text-align: center;
  margin-bottom: 11px;
  }
  .purchase .checkbox label input {
  margin-right: 6px;
  width: 14px;
  height: 14px;
  padding: 0;
  }
  .form-container .submit {
  padding: 7px 45px;
  background-color: #000000;
  color: #ffffff;
  border: none;
  cursor: pointer;
  text-transform: uppercase;
  font-size: 16px;
  font-weight: 400;
  line-height: 16.52px;
  position: relative;
  }
  .remove {
  background: transparent;
  border: none;
  outline: 0;
  }
  .hidden {
  display: none;
  }
  .show {
  display: block;
  }
  @media only screen and (max-width: 400px) {
  .f-desc {
  max-width: 80%;
  }
  }
  .btn-wrap {
  width: 100%;
  margin-top: 35px;
  display: flex;
  justify-content: center;
  align-items: center;
  }
  .nav-cta {
  font-size: 16px;
  font-weight: 400;
  line-height: 19.76px;
  text-align: center;
  color: #000000;
  text-transform: uppercase;
  background: transparent;
  border: 0;
  display: flex;
  align-items: center;
  }
  .nav-cta {
  margin: 0 2px;
  }
  .feedback-options {
  display: flex;
  flex-direction: column;
  }
  .form-group .feedback-label {
  margin-bottom: 13px;
  display: flex;
  align-items: center;
  font-size: 14px;
  font-weight: 400;
  line-height: 19.83px;
  }
  .feedback-label input {
  margin-right: 10px;
  }
  .feedback-input input[type="text"] {
  margin-bottom: 20px;
  }
  .feedback-bad-group,
  .feedback-good-group {
  margin-left: 20px;
  }
  @media only screen and (max-width: 375px) {
  .form-field-wrap .form-group,
  .form-group input,
  .form-group input[type="date"],
  input#birth-date {
  max-width: 100%;
  width: 100%;
  }
  .favorite select {
  height: 27.26px;
  }
  input[type="radio"] {
  width: auto;
  }
  }
  </style>
  </head>
  <body>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <!-- Change Logo Image src as per your requirements -->
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo" width="146" height="75" />
  <!-- Change Logo Image src as per your requirements -->
  </div>
  </div>
  </header>
  <div class="banner">
  <div class="img-wrap">
  <!-- Change Banner Image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/banner.png" alt="Banner" width="600" height="361"></amp-img>
  <!-- Change Banner Image src as per your requirements -->
  </div>
  </div>
  <!-- Success Container - Initially Hidden -->
  <div class="success-container" hidden [hidden]="!showSuccess">
  <div class="success-wrap">
  <h4 class="title">Information saved</h4>
  <p class="para">
  Help us recommend products you'll love and create a personalized shopping experience just for you.
  </p>
  </div>
  </div>
  <div class="container">
  <div class="form-container">
  <h2>Tell us about you!</h2>
  <p>
  Help us recommend products you'll love and create a personalized shopping experience just for you.
  </p>
  <form method="post" class="form" action-xhr="https://example.com/submit" on="submit-success:AMP.setState({showSuccess: false, feedbackType: '', selectedGoodQuestion: '', selectedBadQuestion: ''})">
  <div class="form-field-wrap">
  <!-- First Name -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="first-name">First Name</label>
  </div>
  <input type="text" id="first-name" name="firstName" placeholder="Enter First name" required on="input-debounced:AMP.setState({firstName: event.target.value}), change:AMP.setState({firstName: event.value})" />
  </div>
  <!-- Last Name -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="last-name">Last Name</label>
  </div>
  <input type="text" id="last-name" name="lastName" placeholder="Enter Last name" required on="input-debounced:AMP.setState({lastName: event.target.value}), change:AMP.setState({lastName: event.value})" />
  </div>
  <!-- Phone Number -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="phone-number">Phone Number</label>
  </div>
  <input type="tel" id="phone-number" name="phoneNumber" placeholder="Enter Phone number" required on="input-debounced:AMP.setState({phoneNumber: event.target.value}), change:AMP.setState({phoneNumber: event.value})" />
  </div>
  <!-- Birth Date -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="birth-date">Date of Birth</label>
  </div>
  <input type="date" id="birth-date" name="birthDate" placeholder="Enter date" required on="change:AMP.setState({birthDate: event.value})" />
  </div>
  <!-- Gender -->
  <div class="form-group gender">
  <div class="label-wrap">
  <label>Gender</label>
  </div>
  <div class="gender-options">
  <label>
  <input type="radio" name="gender" value="Male" required checked /> Male
  </label>
  <label>
  <input type="radio" name="gender" value="Female" /> Female
  </label>
  </div>
  </div>
  <!-- Favorite Clothing -->
  <div class="form-group favorite">
  <div class="label-wrap">
  <label for="clothing">Favorite clothing item</label>
  </div>
  <select id="clothing" name="clothing" required on="change:AMP.setState({clothing: event.value})">
  <option value="">Select</option>
  <option value="Casual">Casual</option>
  <option value="Formal">Formal</option>
  <option value="Sportswear">Sportswear</option>
  </select>
  </div>
  <!-- Purchased Before -->
  <div class="form-group purchase">
  <div class="label-wrap"><label>Have you shopped with us before?</label></div>
  <div class="checkbox">
  <label>
  <input type="radio" name="purchasedBefore" value="Yes"
  on="change:AMP.setState({purchasedBefore: event.target.checked ? 'Yes' : ''})" /> Yes
  </label>
  <label>
  <input type="radio" name="purchasedBefore" value="No"
  on="change:AMP.setState({purchasedBefore: event.target.checked ? 'No' : ''})" /> No
  </label>
  </div>
  </div>
  <!-- Please give feedback on our brand. -->
  <div class="form-group feedback">
  <div class="label-wrap">
  <label>Would you recommend our brand to your friends and family?</label>
  </div>
  <div class="feedback-options">
  <!-- Good Feedback Option -->
  <label class="feedback-label">
  <input type="radio" name="feedback" value="Good" on="change:AMP.setState({feedbackType: 'Good', selectedGoodQuestion: ''})" required /> Yes
  </label>
  <div class="feedback-good-group" hidden [hidden]="feedbackType != 'Good'">
  <label class="feedback-label">
  <input type="radio" name="goodFeedback" value="Question 1" on="change:AMP.setState({selectedGoodQuestion: 'Question1'})" required /> Question 1
  </label>
  <div class="feedback-input" hidden [hidden]="selectedGoodQuestion != 'Question1'">
  <input type="text" id="goodFeedback1" name="goodFeedback1" placeholder="Answer Here" required />
  </div>
  <label class="feedback-label">
  <input type="radio" name="goodFeedback" value="Question 2" on="change:AMP.setState({selectedGoodQuestion: 'Question2'})" required /> Question 2
  </label>
  <div class="feedback-input" hidden [hidden]="selectedGoodQuestion != 'Question2'">
  <input type="text" id="goodFeedback2" name="goodFeedback2" placeholder="Answer Here" required />
  </div>
  </div>
  <!-- Bad Feedback Option -->
  <label class="feedback-label">
  <input type="radio" name="feedback" value="Bad" on="change:AMP.setState({feedbackType: 'Bad', selectedBadQuestion: ''})" /> No
  </label>
  <div class="feedback-bad-group" hidden [hidden]="feedbackType != 'Bad'">
  <label class="feedback-label">
  <input type="radio" name="badFeedback" value="Question 1" on="change:AMP.setState({selectedBadQuestion: 'Question1'})" required /> Question 1
  </label>
  <div class="feedback-input" hidden [hidden]="selectedBadQuestion != 'Question1'">
  <input type="text" id="badFeedback1" name="badFeedback1" placeholder="Answer Here" required />
  </div>
  <label class="feedback-label">
  <input type="radio" name="badFeedback" value="Question 2" on="change:AMP.setState({selectedBadQuestion: 'Question2'})" required /> Question 2
  </label>
  <div class="feedback-input" hidden [hidden]="selectedBadQuestion != 'Question2'">
  <input type="text" id="badFeedback2" name="badFeedback2" placeholder="Answer Here" required />
  </div>
  </div>
  </div>
  </div>
  <div class="btn-wrap">
  <!-- Submit Button -->
  <button type="submit" class="submit" on="tap:AMP.setState({showSuccess: true})">Submit</button>
  </div>
  </div>
  </form>
  </div>
  </div>
  <!-- <script type="application/json" id="amp-state">
  {
  "showSuccess": false,
  "feedbackType": ""
  }
  </script> -->
  <footer class="footer">
  <ul class="media-logo-list">
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4246683f26846a6a5966a72e37034d4.png" alt="instagram" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/677a3f1dbf554cdc858f91cfd9c8c05d.png" alt="facebook" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/dd65dffd70e34ccab634a38185229fd0.png" alt="x" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  </ul>
  <p class="f-desc">
  For assistance, connect with us on social media or reach out to our support team at support@example.com 
  </p>
  <p class="f-desc">
  To opt out of promotional emails like this, <a href="https://google.com" style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
  </p>
  </footer>
  </div>
  </body>
  </html>
  ```
  ```html Extended Customer Survey
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  }
  img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }
  /* Change Theme */
  .main {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: 0 auto;
  background: #cecece;
  position: relative;
  }
  /* Change Theme */
  @media only screen and (max-width: 400px) {
  body .main {
  max-width: 95%;
  }
  }
  .logo-wrap {
  padding: 16px 0;
  background-color: #ffffff;
  }
  .logo-wrap .img-wrap {
  max-width: 146px;
  max-height: 75px;
  margin: 0 auto;
  }
  .footer {
  border-top: 0.5px solid #ffff;
  background: #ffff;
  }
  .media-logo-list {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  gap: 16px;
  margin: 39px 0 14px;
  }
  .media-logo-list .logo-item {
  width: 28px;
  height: 28px;
  }
  .media-logo-list .logo-item .logo-link {
  width: 100%;
  height: 100%;
  display: inline-block;
  }
  .f-desc {
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  color: #939393;
  text-align: center;
  max-width: 65%;
  margin: 0 auto 27px;
  padding-bottom: 47px;
  }
  .f-nav-list {
  padding: 27px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  border-top: 0.5px solid #979797;
  }
  .f-nav-list .f-nav-item {
  margin: 0 5px;
  }
  .f-nav-list .f-nav-item .f-nav-link {
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  text-align: center;
  color: #939393;
  text-decoration: none;
  }
  .banner .img-wrap {
  max-height: 361px;
  width: 100%;
  }
  .success-container {
  text-align: center;
  background-color: rgba(206, 206, 206, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 10;
  }
  .success-container .success-wrap {
  max-width: 312px;
  width: 100%;
  position: relative;
  top: 20%;
  left: 50%;
  transform: translateX(-50%);
  background: #ffffff;
  padding: 60px 40px;
  }
  .success-wrap h4 {
  font-size: 16px;
  font-weight: 400;
  line-height: 27px;
  text-align: center;
  text-transform: uppercase;
  margin-bottom: 10px;
  }
  .success-wrap p {
  font-size: 12px;
  font-weight: 400;
  line-height: 20px;
  text-align: center;
  color: #909090;
  text-transform: none;
  }
  .container {
  max-width: 555px;
  margin: -30px auto 42px;
  position: relative;
  z-index: 2;
  }
  .form-container {
  padding: 33px 22px 26px 23px;
  background-color: #ffffff;
  box-shadow: 0px 8.26px 3.3px 0px #00000040;
  }
  .form-container h2 {
  font-size: 16px;
  font-weight: 400;
  line-height: 22px;
  color: #000000;
  margin-bottom: 8px;
  }
  .form-container p {
  font-size: 12px;
  font-weight: 400;
  line-height: 16px;
  color: #909090;
  margin-bottom: 20px;
  text-transform: none;
  }
  .form-container .form-field-wrap {
  display: flex;
  gap: 14px;
  flex-wrap: wrap;
  }
  .form-field-wrap .form-group {
  display: flex;
  flex-direction: column;
  width: 48%;
  }
  .form-group label {
  font-size: 12px;
  font-weight: 400;
  line-height: 16.52px;
  text-align: left;
  color: #000000;
  text-transform: none;
  margin-bottom: 8px;
  }
  .form-group input[type="text"],
  .form-group input[type="date"],
  .form-group input[type="tel"],
  .form-group input[type="number"] {
  padding: 5px 10px;
  width: 91%;
  height: 27.26px;
  margin-bottom: 2px;
  font-size: 12px;
  font-weight: 400;
  line-height: 16.52px;
  text-align: left;
  color: #000000;
  text-transform: none;
  border: 0.83px solid #adadad;
  }
  .form-group input[type="date"] {
  text-transform: uppercase;
  }
  .form-group .label-wrap {
  display: flex;
  justify-content: space-between;
  }
  .form-group .label-wrap .remove .remove-logo {
  width: 16px;
  height: 16px;
  }
  .form-group.full-width {
  margin-bottom: 15px;
  }
  .form-group.full-width input[type="text"] {
  width: 96%;
  }
  .form-group.feedback,
  .form-group.gender,
  .form-group.favorite,
  .form-group.purchase {
  margin-top: 16px;
  width: 100%;
  }
  .form-group select {
  flex-grow: 1;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
  }
  .form-container .gender-options {
  display: flex;
  justify-content: space-between;
  margin-bottom: 16px;
  max-width: 130px;
  }
  .form-container .gender-options label {
  display: flex;
  align-items: center;
  max-width: 100px;
  width: 100%;
  margin: 0;
  font-size: 14px;
  font-weight: 400;
  line-height: 19.83px;
  text-align: center;
  }
  .gender-options input[type="radio"] {
  margin-right: 6px;
  }
  .form-group.favorite {
  display: flex;
  flex-direction: column;
  margin-bottom: 5px;
  }
  .favorite select {
  font-size: 10px;
  font-weight: 400;
  line-height: 15px;
  text-align: left;
  background: #ffffff;
  color: #000000;
  border: 0.83px solid #ADADAD;
  border-radius: 0;
  }
  .favorite select option {
  width: 50px;
  font-size: 12px;
  }
  .form-container .checkbox {
  display: flex;
  flex-direction: column;
  margin-top: 5px;
  }
  .purchase .checkbox label {
  display: flex;
  align-items: center;
  max-width: 100px;
  width: 100%;
  font-size: 14px;
  font-weight: 400;
  line-height: 16.83px;
  text-align: center;
  margin-bottom: 11px;
  }
  .purchase .checkbox label input {
  margin-right: 6px;
  width: 14px;
  height: 14px;
  padding: 0;
  }
  .form-container .submit {
  padding: 7px 45px;
  background-color: #000000;
  color: #ffffff;
  border: none;
  cursor: pointer;
  text-transform: uppercase;
  font-size: 16px;
  font-weight: 400;
  line-height: 16.52px;
  position: relative;
  }
  .remove {
  background: transparent;
  border: none;
  outline: 0;
  }
  .hidden {
  display: none;
  }
  .show {
  display: block;
  }
  @media only screen and (max-width: 400px) {
  .f-desc {
  max-width: 80%;
  }
  }
  .btn-wrap {
  width: 100%;
  margin-top: 35px;
  display: flex;
  justify-content: center;
  align-items: center;
  }
  .nav-cta {
  font-size: 16px;
  font-weight: 400;
  line-height: 19.76px;
  text-align: center;
  color: #000000;
  text-transform: uppercase;
  background: transparent;
  border: 0;
  display: flex;
  align-items: center;
  }
  .nav-cta {
  margin: 0 2px;
  }
  .feedback-options {
  display: flex;
  flex-direction: column;
  }
  .form-group .feedback-label {
  margin-bottom: 13px;
  display: flex;
  align-items: center;
  font-size: 14px;
  font-weight: 400;
  line-height: 19.83px;
  }
  .feedback-label input {
  margin-right: 10px;
  }
  .feedback-input input[type="text"] {
  margin-bottom: 20px;
  }
  .feedback-bad-group,
  .feedback-good-group {
  margin-left: 20px;
  }
  @media only screen and (max-width: 375px) {
  .form-field-wrap .form-group,
  .form-group input,
  .form-group input[type="date"],
  input#birth-date {
  max-width: 100%;
  width: 100%;
  }
  .favorite select {
  height: 27.26px;
  }
  input[type="radio"] {
  width: auto;
  }
  }
  </style>
  </head>
  <body>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <!-- Change Logo Image src as per your requirements -->
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo" width="146" height="75" />
  <!-- Change Logo Image src as per your requirements -->
  </div>
  </div>
  </header>
  <div class="banner">
  <div class="img-wrap">
  <!-- Change Banner Image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/AMP-FORM/banner.png" alt="Banner" width="600" height="361"></amp-img>
  <!-- Change Banner Image src as per your requirements -->
  </div>
  </div>
  <!-- Success Container - Initially Hidden -->
  <div class="success-container" hidden [hidden]="!showSuccess">
  <div class="success-wrap">
  <h4 class="title">Information saved</h4>
  <p class="para">
  Help us recommend products you'll love and create a personalized shopping experience just for you.
  </p>
  </div>
  </div>
  <div class="container">
  <div class="form-container">
  <h2>Tell us about you!</h2>
  <p>
  Help us recommend products you'll love and create a personalized shopping experience just for you.
  </p>
  <form method="post" class="form" action-xhr="https://example.com/submit" on="submit-success:AMP.setState({showSuccess: false, feedbackType: '', selectedGoodQuestion: '', selectedBadQuestion: ''})">
  <div class="form-field-wrap">
  <!-- First Name -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="first-name">First Name</label>
  </div>
  <input type="text" id="first-name" name="firstName" placeholder="Enter First name" required on="input-debounced:AMP.setState({firstName: event.target.value}), change:AMP.setState({firstName: event.value})" />
  </div>
  <!-- Last Name -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="last-name">Last Name</label>
  </div>
  <input type="text" id="last-name" name="lastName" placeholder="Enter Last name" required on="input-debounced:AMP.setState({lastName: event.target.value}), change:AMP.setState({lastName: event.value})" />
  </div>
  <!-- Phone Number -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="phone-number">Phone Number</label>
  </div>
  <input type="tel" id="phone-number" name="phoneNumber" placeholder="Enter Phone number" required on="input-debounced:AMP.setState({phoneNumber: event.target.value}), change:AMP.setState({phoneNumber: event.value})" />
  </div>
  <!-- Birth Date -->
  <div class="form-group">
  <div class="label-wrap">
  <label for="birth-date">Date of Birth</label>
  </div>
  <input type="date" id="birth-date" name="birthDate" placeholder="Enter date" required on="change:AMP.setState({birthDate: event.value})" />
  </div>
  <!-- Gender -->
  <div class="form-group gender">
  <div class="label-wrap">
  <label>Gender</label>
  </div>
  <div class="gender-options">
  <label>
  <input type="radio" name="gender" value="Male" required checked /> Male
  </label>
  <label>
  <input type="radio" name="gender" value="Female" /> Female
  </label>
  </div>
  </div>
  <!-- Favorite Clothing -->
  <div class="form-group favorite">
  <div class="label-wrap">
  <label for="clothing">Favorite clothing item</label>
  </div>
  <select id="clothing" name="clothing" required on="change:AMP.setState({clothing: event.value})">
  <option value="">Select</option>
  <option value="Casual">Casual</option>
  <option value="Formal">Formal</option>
  <option value="Sportswear">Sportswear</option>
  </select>
  </div>
  <!-- Purchased Before -->
  <div class="form-group purchase">
  <div class="label-wrap"><label>Have you shopped with us before?</label></div>
  <div class="checkbox">
  <label>
  <input type="radio" name="purchasedBefore" value="Yes"
  on="change:AMP.setState({purchasedBefore: event.target.checked ? 'Yes' : ''})" /> Yes
  </label>
  <label>
  <input type="radio" name="purchasedBefore" value="No"
  on="change:AMP.setState({purchasedBefore: event.target.checked ? 'No' : ''})" /> No
  </label>
  </div>
  </div>
  <!-- Please give feedback on our brand. -->
  <div class="form-group feedback">
  <div class="label-wrap">
  <label>Would you recommend our brand to your friends and family?</label>
  </div>
  <div class="feedback-options">
  <!-- Good Feedback Option -->
  <label class="feedback-label">
  <input type="radio" name="feedback" value="Good" on="change:AMP.setState({feedbackType: 'Good', selectedGoodQuestion: ''})" required /> Yes
  </label>
  <div class="feedback-good-group" hidden [hidden]="feedbackType != 'Good'">
  <label class="feedback-label">
  <input type="radio" name="goodFeedback" value="Question 1" on="change:AMP.setState({selectedGoodQuestion: 'Question1'})" required /> Question 1
  </label>
  <div class="feedback-input" hidden [hidden]="selectedGoodQuestion != 'Question1'">
  <input type="text" id="goodFeedback1" name="goodFeedback1" placeholder="Answer Here" required />
  </div>
  <label class="feedback-label">
  <input type="radio" name="goodFeedback" value="Question 2" on="change:AMP.setState({selectedGoodQuestion: 'Question2'})" required /> Question 2
  </label>
  <div class="feedback-input" hidden [hidden]="selectedGoodQuestion != 'Question2'">
  <input type="text" id="goodFeedback2" name="goodFeedback2" placeholder="Answer Here" required />
  </div>
  </div>
  <!-- Bad Feedback Option -->
  <label class="feedback-label">
  <input type="radio" name="feedback" value="Bad" on="change:AMP.setState({feedbackType: 'Bad', selectedBadQuestion: ''})" /> No
  </label>
  <div class="feedback-bad-group" hidden [hidden]="feedbackType != 'Bad'">
  <label class="feedback-label">
  <input type="radio" name="badFeedback" value="Question 1" on="change:AMP.setState({selectedBadQuestion: 'Question1'})" required /> Question 1
  </label>
  <div class="feedback-input" hidden [hidden]="selectedBadQuestion != 'Question1'">
  <input type="text" id="badFeedback1" name="badFeedback1" placeholder="Answer Here" required />
  </div>
  <label class="feedback-label">
  <input type="radio" name="badFeedback" value="Question 2" on="change:AMP.setState({selectedBadQuestion: 'Question2'})" required /> Question 2
  </label>
  <div class="feedback-input" hidden [hidden]="selectedBadQuestion != 'Question2'">
  <input type="text" id="badFeedback2" name="badFeedback2" placeholder="Answer Here" required />
  </div>
  </div>
  </div>
  </div>
  <div class="btn-wrap">
  <!-- Submit Button -->
  <button type="submit" class="submit" on="tap:AMP.setState({showSuccess: true})">Submit</button>
  </div>
  </div>
  </form>
  </div>
  </div>
  <!-- <script type="application/json" id="amp-state">
  {
  "showSuccess": false,
  "feedbackType": ""
  }
  </script> -->
  <footer class="footer">
  <ul class="media-logo-list">
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4246683f26846a6a5966a72e37034d4.png" alt="instagram" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/677a3f1dbf554cdc858f91cfd9c8c05d.png" alt="facebook" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/dd65dffd70e34ccab634a38185229fd0.png" alt="x" class="media-logo" width="34" height="34"></amp-img>
  </a>
  </li>
  </ul>
  <p class="f-desc">
  For assistance, connect with us on social media or reach out to our support team at support@example.com 
  </p>
  <p class="f-desc">
  To opt out of promotional emails like this, <a href="https://google.com" style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a>
  </p>
  </footer>
  </div>
  </body>
  </html>
  ```
</Accordion>

## Feedback Form Template

This AMP template enables you to collect user input directly within the email, allowing for quick interactions such as survey responses, feedback, or sign-ups. With AMP’s real-time interactivity, the form can be submitted without users needing to open a separate browser window, making the experience fast, seamless, and conversion-friendly.

<Image align="center" alt="Sample Feedback Form Template" border={true} caption="Sample Feedback Form Template" src="https://files.readme.io/6e23a38d585989d9dc98e056b2f634c33c347857892ef9e1ea7b3f35f934308e-Feedback_Form_AMP.png" width="25% " />

<details>
  <summary><b>Expand to know more about the template.</b></summary>

  ### Use Case Examples

  * Gather user feedback post-purchase or post-interaction.
  * Collect survey responses (for example, NPS survey, product ratings, and so on).
  * Enable newsletter or webinar sign-ups within the email.
  * Registration for events, contests, or loyalty programs.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  background-color: #f5f5f5;
  }
  img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }
  .table-container{
  max-width: 90%;
  background: #FFFFFF; margin-top: -60px;
  }
  .container{
  max-width: 85%; margin: 0 auto;
  }
  @media screen and (max-width: 480px) {
  .container {
  max-width: 90%;
  } 
  .table-container{
  max-width: 95%;
  } 
  .logo{
  width: 150px; height: 60px;
  } 
  } 
  .form-container{
  padding: 34px 20px;
  position: relative;
  }
  .field-wrap{
  padding: 40px 0;
  border-bottom: 1px solid #ADADAD;
  }
  .field-wrap.typ-last{
  border-bottom: none;
  }
  .field-wrap .field-label{
  font-size: 16px;
  font-weight: 400;
  line-height: 20px;
  color: #000000; 
  text-transform: none;
  margin-bottom: 25px; 
  display: flex;
  align-items: center; 
  }
  .field-wrap .marker{
  width: 20px;
  height: 20px;
  background: #5A3D2B;
  margin-right: 15px;
  display: inline-block;
  }
  .field-wrap .input-list{
  margin-left: 30px;
  list-style: none;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-wrap: wrap;
  }
  .radio-input{
  display:none;
  visibility:hidden;
  appearance: none;
  }
  .radio-field {
  cursor: pointer;
  }
  .field-wrap .input-list .input-item{
  margin-right: 25px;
  }
  .field-wrap .input-list .input-item.full-width{
  width: 100%;
  }
  .field-wrap .radio-field.thumb{
  display: flex;
  align-items: center;
  }
  .field-wrap .radio-field.thumb .radio-img{
  width: 34px;
  height: 34px;
  display: inline-block;
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-thumbsUp.png');
  background-position: 0 0;
  background-repeat: no-repeat;
  background-size: contain;
  }
  .field-wrap .radio-field.thumb input[type=radio]:checked + .radio-img{
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-thumbsUp.png');
  background-size: contain;
  }
  .field-wrap .radio-field.thumb.thumb-down .radio-img{
  transform: rotate(180deg);
  }
  .field-wrap .radio-field.thumb .text{
  font-size: 16px;
  font-weight: 400;
  line-height: 20px;
  color: #595959;
  margin-left: 10px;
  }
  /* styling for rating */
  .field-wrap .radio-field.star .radio-img{
  width: 28px;
  height: 28px;
  display: inline-block;
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-star.png');
  background-position: 0 0;
  background-repeat: no-repeat;
  background-size: contain;
  }
  .field-wrap .radio-field.star input[type=radio]:checked + .radio-img{
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-star.png');
  background-size: contain;
  }
  /* styling for smiley */
  .field-wrap .radio-field.smiley .radio-img{
  width: 38px;
  height: 38px;
  display: inline-block;
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-smile3.png');
  background-position: 0 0;
  background-repeat: no-repeat;
  background-size: contain;
  }
  .field-wrap .radio-field.smiley input[type=radio]:checked + .radio-img{
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-smile3.png');
  background-size: contain;
  }
  .field-wrap .radio-field.smiley.smiley-normal .radio-img{
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-smile2.png');
  background-size: contain;
  }
  .field-wrap .radio-field.smiley.smiley-normal input[type=radio]:checked + .radio-img{
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-smile2.png');
  background-size: contain;
  }
  .field-wrap .radio-field.smiley.smiley-sad .radio-img{
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-smile1.png');
  background-size: contain;
  }
  .field-wrap .radio-field.smiley.smiley-sad input[type=radio]:checked + .radio-img{
  background: transparent url('https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-fill-smile1.png');
  background-size: contain;
  }
  .field-wrap .input{
  width: 100%;
  height: 81px;
  border: 1px solid #A9A9A9;
  border-radius: 5px;
  resize: none;
  padding: 10px;
  font-size: 14px;
  font-weight: 400;
  line-height: 20.56px;
  color: #A2A2A2;;
  }
  .field-wrap .field-head{
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  }
  .field-wrap .field-head .remove{
  border: none;
  background: transparent;
  }
  .field-wrap .field-head .remove .remove-logo {
  width: 22px;
  height: 22px;
  }
  .submit-cta{
  display:inline-block; 
  background-color: #5A3D2B; 
  font-size: 20px; 
  font-weight: 400;
  line-height: 22px;
  text-align: center; 
  color: #FFFFFF; 
  text-transform: uppercase; 
  border-radius: 5px; 
  text-decoration: none; 
  padding: 14px 10px; 
  width: 100%;
  border: 0;
  outline: 0;
  }
  .submit-cta.disable{
  background: #D1D1D1;
  }
  .success-container{
  border: 1px solid #5A3D2B;
  text-align: center;
  padding: 10px 30px;
  box-shadow: 2px 4px 4px 0px #00000040;
  z-index: 2;
  position: absolute;
  left: 50%;
  bottom: -72px;
  width: 80%;
  transform: translateX(-50%);
  background: #FFFFFF;
  }
  .success-container .title{
  font-size: 20px;
  font-weight: 400;
  line-height: 28px;
  color: #000000;
  text-transform: none;
  margin-bottom: 5px;
  }
  .success-container .para{
  font-size: 10px;
  font-weight: 400;
  line-height: 15px;
  color: #7D7D7D;
  text-transform: none;
  }
  .hidden {
  display: none;
  }
  .show{
  display: block;
  }
  .main-title{
  margin: 0 0 8px; font-family: 'Helvetica', Arial, sans-serif; font-size: 32px; font-weight: 400; color: #FFFFFF; line-height: 32px; text-align: center; text-transform: uppercase;
  }
  .main-desc{
  margin: 0; text-transform: none; font-family: 'Helvetica', Arial, sans-serif; font-size: 12px; font-weight: 400; line-height: 20px; text-align: center; color: #FFFFFF;
  }
  .form-title{
  text-transform: none; font-size: 32px; font-weight: 400; line-height: 46px; text-align: center; color: #000000; margin-bottom: 9px;
  }
  @media screen and (max-width: 480px) {
  .main-title,
  .form-title{
  font-size: 28px;
  line-height: 38px;
  }
  .field-wrap {
  padding: 20px 0;
  }
  .field-wrap .marker {
  width: 10px;
  height: 10px;
  }
  .field-wrap .field-label {
  font-size: 14px;
  line-height: 18px;
  margin-bottom: 20px;
  }
  .field-wrap .input-list .input-item{
  margin-right: 15px;
  }
  .field-wrap .radio-field.thumb .radio-img,
  .field-wrap .radio-field.star .radio-img,
  .field-wrap .radio-field.smiley .radio-img {
  width: 25px;
  height: 25px;
  }
  .submit-cta{
  font-size: 16px;
  line-height: 18px; 
  padding: 10px;
  }
  }
  </style>
  </head>
  <body style="font-family: 'Helvetica', Arial, sans-serif; font-weight: 400; margin: 0; padding: 0;">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; border-spacing: 0;">
  <!-- header start-->
  <tr>
  <td align="center" style="display: block; padding: 20px 0; max-width: 90%; margin: 0 auto;" class="container">
  <div class="logo-wrap">
  <!-- Change image src as per your requirements -->
  <amp-img src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" width="159" height="73" layout="fixed" class="logo" alt="Logo"></amp-img>
  </div>
  </td>
  </tr>
  <!-- header end-->
  <tr>
  <td style="background: #5A3D2B;">
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/banner.jpg" alt="Banner" width="600" height="360" />
  </td>
  </tr>
  <tr>
  <td align="center" style="padding: 28px 0 96px; background: #5A3D2B;">
  <div class="container">
  <h2 class="main-title" style="margin: 0 0 8px; font-family: 'Helvetica', Arial, sans-serif; font-size: 32px; font-weight: 400; color: #FFFFFF; line-height: 32px; text-align: center; text-transform: uppercase;">WE VALUE YOUR FEEDBACK</h2>
  <p class="main-desc">Your feedback will help us improve the app experience for you and other customers.</p>
  </div>
  </td>
  </tr>
  <tr>
  <td align="center" style="background: gray; padding-bottom: 30px;">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center" width="100%" class="table-container">
  <tr>
  <td>
  <div class="form-container">
  <h2 class="form-title">Survey</h2>
  <form method="post" action-xhr="https://google.com" id="feedbackForm" enctype="multipart/form-data" on="submit-success:AMP.setState({successVisible: false})">
  <!-- Question 1 -->
  <div class="field-wrap">
  <h3 class="field-label"><span class="marker"></span>Are you satisfied with the comfort of our shoes?</h3>
  <ul class="input-list">
  <li class="input-item">
  <label class="radio-field thumb thumb-up" for="thumbUp">
  <input type="radio" name="satisfied" value="thumb-up" class="radio-input" id="thumbUp">
  <span class="radio-img"></span>
  <span class="text">Yes</span>
  </label>
  </li>
  <li class="input-item">
  <label class="radio-field thumb thumb-down" for="thumbDown">
  <input type="radio" name="satisfied" value="thumb-down" class="radio-input" id="thumbDown">
  <span class="radio-img"></span>
  <span class="text">No</span>
  </label>
  </li>
  </ul>
  </div>
  <!-- Question 2 -->
  <div class="field-wrap">
  <h3 class="field-label"><span class="marker"></span>How would you rate the quality of our shoes?</h3>
  <ul class="input-list">
  <li class="input-item">
  <label class="radio-field star" for="star1">
  <input type="radio" name="rate" value="star1" class="radio-input" id="star1">
  <span class="radio-img"></span>
  </label>
  </li>
  <li class="input-item">
  <label class="radio-field star" for="star2">
  <input type="radio" name="rate" value="star2" class="radio-input" id="star2">
  <span class="radio-img"></span>
  </label>
  </li>
  <li class="input-item">
  <label class="radio-field star" for="star3">
  <input type="radio" name="rate" value="star3" class="radio-input" id="star3">
  <span class="radio-img"></span>
  </label>
  </li>
  <li class="input-item">
  <label class="radio-field star" for="star4">
  <input type="radio" name="rate" value="star4" class="radio-input" id="star4">
  <span class="radio-img"></span>
  </label>
  </li>
  <li class="input-item">
  <label class="radio-field star" for="star5">
  <input type="radio" name="rate" value="star5" class="radio-input" id="star5">
  <span class="radio-img"></span>
  </label>
  </li>
  </ul>
  </div>
  <!-- Question 3 -->
  <div class="field-wrap">
  <h3 class="field-label"><span class="marker"></span>How do you feel about the design of our shoes?</h3>
  <ul class="input-list">
  <li class="input-item">
  <label class="radio-field smiley smiley-happy" for="happy">
  <input type="radio" name="feel" value="happy" class="radio-input" id="happy">
  <span class="radio-img"></span>
  </label>
  </li>
  <li class="input-item">
  <label class="radio-field smiley smiley-normal " for="normal">
  <input type="radio" name="feel" value="thumb-down" class="radio-input" id="normal">
  <span class="radio-img"></span>
  </label>
  </li>
  <li class="input-item">
  <label class="radio-field smiley smiley-sad" for="sad">
  <input type="radio" name="feel" value="smiley-sad" class="radio-input" id="sad">
  <span class="radio-img"></span>
  </label>
  </li>
  </ul>
  </div>
  <!-- Question 4 -->
  <div class="field-wrap typ-last">
  <div class="field-head">
  <h3 class="field-label"><span class="marker"></span>Share any additional thoughts about our products.</h3>
  <button class="remove" on="tap:AMP.setState({feedbackInput: ''})">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/feedback-html/icon-trash.png" alt="remove" class="remove-logo" width="20" height="20"></amp-img>
  </button>
  </div>
  <ul class="input-list">
  <li class="input-item full-width">
  <textarea class="input" id="feedback-input" name="feedbackInput" placeholder="Please explain here" on="input-debounced:AMP.setState({feedbackInput: event.target.value})"> </textarea>
  </li>
  </ul>
  </div>
  <div class="btn-wrap">
  <!-- Submit Button -->
  <button type="submit" class="submit-cta" [class]="!successVisible ? 'submit-cta' : 'submit-cta disable'" on="tap:AMP.setState({successVisible: true})">Submit</button>
  </div>
  </form>
  <!-- Success Container - Initially Hidden -->
  <div class="success-container hidden" [class]="!successVisible ? 'success-container hidden' : 'success-container show'">
  <h4 class="title">Thank you</h4>
  <p class="para">
  is simply dummy text of the printing and typesetting is simply dummy text of the printing and typesetting industry.g industry. is simply dummy text of the printing and typesetting is simply dummy.
  </p>
  </div>
  </div>
  </td>
  </tr>
  <!-- footer start-->
  <tr>
  <td align="center">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center" style="padding: 50px 0; border-top: 1px solid #ADADAD">
  <tr>
  <td style="padding: 0 0 18px;">
  <table align="center" cellpadding="0" cellspacing="0" width="100%" style="text-align: center;">
  <tr>
  <td style="padding: 0 15px; display: inline-block;">
  <a href="https://www.google.co.in/" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;">
  <!-- Change image src as per your requirements -->
  <amp-img src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d84491d2c49a419695672cacb928bde3.png" alt="instagram" width="34" height="34">
  </a>
  </td>
  <td style="padding: 0 15px; display: inline-block;">
  <a href="https://www.google.co.in/" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;">
  <!-- Change image src as per your requirements -->
  <amp-img src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9d7b2e5525c24688ab9bc1257b76394c.png" alt="facebook" width="34" height="34">
  </a>
  </td>
  <td style="padding: 0 15px; display: inline-block;">
  <a href="https://www.google.co.in/" style="vertical-align: middle;display: inline-block; width: 34px; height: 34px;">
  <!-- Change image src as per your requirements -->
  <amp-img src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/a2e1ff645faa427f997b50f6277f98fb.png" alt="x" width="34" height="34">
  </a>
  </td>
  </tr>
  </table>
  </td>
  </tr>
  <tr>
  <td>
  <p style="color: #939393; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin: 0 auto; max-width: 80%;">
  For assistance, connect with us on social media or reach out to our support team at support@example.com 
  </p>
  </td>
  </tr>
  <tr>
  <td>
  <p style="color: #939393; font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; margin: 0 auto; max-width: 80%;">To opt out of sharing feedback in the future, <a href="https://google.com" style="color:#5A3D2B;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
  </td>
  </tr>
  </table>
  </td>
  </tr>
  <!-- footer end-->
  </table>
  </td>
  </tr>
  </table>
  </body>
  </html>
  ```
</details>

## EMI Calculator Template

This AMP template offers users an embedded calculator directly within the email, allowing them to input loan details and instantly view their EMI (Equated Monthly Installment) amount, without needing to leave the inbox. This interactive feature enhances the user journey by making decision-making quicker, simpler, and more engaging.

<Image align="center" alt="Sample EMI Calculator Template" border={true} caption="Sample EMI Calculator Template" src="https://files.readme.io/cdd5657aa21e673ad2539a78a33f8ee5641de418777efcfd80323826bbeab7e8-EMI_Calculator_AMP.png" width="35% " />

<details>
  <summary><b>Expand to know more about the template.</b></summary>

  ### Use Case Examples

  * Promote new loan or credit products with an embedded EMI estimator.
  * Assist users in planning repayments based on tenure and interest rate.
  * Offer personalized finance tools in engagement campaigns.
  * Support comparison scenarios between multiple loan products.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>

  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }

  body {
  font-family: arial, sans-serif;
  font-weight: 400;
  background-color: #f5f5f5;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  }

  img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }

  /* Change Theme */

  .main {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: 0 auto;
  background: #f5f5f5;
  flex: 1;
  }

  /* Change Theme */

  @media only screen and (max-width: 400px) {
  .main {
  max-width: 100%;
  }
  }

  .logo-wrap {
  padding: 12px 24px;
  background-color: #F5F5F5;
  border-radius: 0 0 41px 41px;
  text-align: center;
  z-index: 2;
  position: relative;
  }

  .logo-wrap .img-wrap {
  max-width: 145.78px;
  max-height: 74.89px;
  }

  .footer {
  width: 90%;
  margin: 45px auto 0;
  background: #ffffff;
  border-radius: 24px 24px 0 0;
  background-color: #ffffff;
  padding: 1px 0 33px;
  }

  .media-logo-list {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  gap: 16px;
  margin: 32px 0 17px;
  }

  .media-logo-list .logo-item {
  width: 20px;
  height: 20px;
  }

  .media-logo-list .logo-item .logo-link {
  width: 100%;
  height: 100%;
  display: inline-block;
  }

  .f-desc {
  font-size: 12px;
  font-weight: 400;
  line-height: 20px;
  color: #6f6f6f;
  text-align: center;
  max-width: 95%;
  margin: 0 auto;
  text-transform: none;
  }

  .banner {
  margin: -35px;
  }

  .banner .img-wrap {
  max-height: 381px;
  width: 100%;
  }

  .calculator-wrap {
  width: 90%;
  position: relative;
  border-radius: 24px;
  background-color: #ffffff;
  margin: -62px auto 0;
  }

  .calculator-wrap .form-wrap {
  padding: 24px 26px 40px;
  }

  .form-wrap .text {
  font-size: 20px;
  line-height: 28px;
  font-weight: 400;
  color: #3D3D3D;
  align-items: center;
  }

  .form-wrap .calculator-title {
  padding: 8px 0 32px;
  font-size: 32px;
  font-weight: 400;
  line-height: 38px;
  }

  .form-wrap .calculator-title span {
  color: #4140FF;
  }

  .form-wrap label,
  .question h2 {
  display: block;
  padding-bottom: 13px;
  font-size: 16px;
  font-weight: 400;
  line-height: 20px;
  }

  .field-wrap .answer {
  margin-bottom: 32px;
  }

  .field-wrap .input-wrap {
  border-radius: 79px;
  border: 0.82px solid #5a5959;
  padding: 15px;
  }

  .form-wrap input,
  .input-style {
  width: 95%;
  text-indent: 5px;
  color: #000000;
  font-size: 16px;
  line-height: 23px;
  border: 0;
  outline: 0;
  }

  .form-wrap button,
  .button {
  width: 100%;
  border-radius: 50px;
  padding: 13px;
  background: #3e3cf9;
  color: #ffffff;
  font-weight: 400;
  font-size: 16px;
  line-height: 23px;
  border: 0.82px solid #5a5959;
  text-decoration: none;
  text-align: center;
  display: block;
  text-transform: none;
  }

  .form-wrap button:disabled,
  .disabled {
  background: #D8D8FE;
  }

  .calculator-wrap .result-wrap {
  padding: 64px 0 0;
  }

  .result-wrap .result-title {
  padding: 0 0 12px;
  font-size: 32px;
  font-weight: 400;
  line-height: 38px;
  }

  .result-wrap .result-output {
  display: flex;
  justify-content: space-between;
  max-width: 464px;
  height: 76px;
  align-items: center;
  border-radius: 0 0 41px 41px;
  border-bottom: 0.82px solid #5a5959;
  margin-bottom: 29px;
  padding: 0 22px;
  }

  .result-output .total-text {
  font-size: 16px;
  font-weight: 400;
  line-height: 19.36px;
  text-align: center;
  }

  .result-output .total-value {
  font-size: 24px;
  font-weight: 400;
  line-height: 29.05px;
  text-align: center;
  }

  .result-wrap button {
  width: 100%;
  border-radius: 79.98px;
  padding: 13px;
  background: #3e3cf9;
  color: #ffffff;
  font-weight: 400;
  font-size: 16px;
  line-height: 23px;
  border: 0.82px solid #5a5959;
  margin-bottom: 11px;
  cursor: pointer;
  }

  .result-wrap button.disabled,
  .result-wrap button:disabled,
  .result-wrap .button.disabled,
  .result-wrap .button:disabled {
  opacity: 0.5;
  }

  @media only screen and (max-width: 480px) {
  .logo-wrap .img-wrap {
  max-width: 130px;
  max-height: 60px;
  }

  .form-wrap input,
  .input-style {
  width: 90%;
  }

  .calculator-wrap .form-wrap {
  padding: 20px 20px 40px;
  }

  .calculator-wrap .result-wrap {
  padding: 40px 0 0;
  }

  .result-wrap .result-title {
  font-size: 25px;
  line-height: 30px;
  }

  .form-wrap .calculator-title {
  padding: 8px 0 25px;
  font-size: 25px;
  line-height: 30px;
  }

  .field-wrap .input-wrap {
  padding: 10px;
  }

  .form-wrap .text {
  font-size: 15px;
  line-height: 20px;
  }

  .result-output .total-value {
  font-size: 20px;
  line-height: 24px;
  }

  .result-wrap .result-output {
  padding: 20px 15px;
  height: auto;
  }

  .form-wrap .question {
  padding-bottom: 8px;
  }
  }

  @media only screen and (max-width: 300px) {
  .product-wrap {
  padding: 40px 5px 20px;
  }
  }
  </style>
  </head>

  <body>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <!-- Change Logo Image src as per your requirements -->
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo"
  width="159" height="73" />
  <!-- Change Logo Image src as per your requirements -->
  </div>
  </div>
  </header>
  <div class="banner">
  <div class="img-wrap">
  <!-- Change Banner Image src as per your requirements -->
  <amp-img layout="responsive"
  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/stacks-coins-arranged-bar-graph%201.png"
  alt="Banner" width="600" height="381"></amp-img>
  <!-- Change Banner Image src as per your requirements -->
  </div>
  </div>
  <div class="calculator-wrap">
  <div on="tap:AMP.setState({
  formxo5j8158: {
  fuuid: formxo5j8158.fuuid || floor(random() * 100000),
  responses: {
  stepra77z1:{
  elementzzr6o10:elementzzr6o10Formula(formxo5j8158.responses.stepv119k145.element232766,formxo5j8158.responses.stepv119k145.elementaa3vl4,formxo5j8158.responses.stepv119k145.elementst0oh2)
  }
  }
  }
  })" role="tab" tabindex="1" class="form-wrap amp-form-block amp-html-block formxo5j8158-wrapper"
  style="margin:auto;text-align:left">
  <div class="data"><amp-state id="formxo5j8158">
  <script type="application/json">{"currentStep":"stepv119k145","responses":{},"formHistory":[]}</script>
  </amp-state></div>
  <p class="text">Instantly</p>
  <h2 class="calculator-title">
  Calculate Your <span> EMI </span>
  </h2>
  <form id="formWidgetFallbackAnchorLinkformxo5j8158" class="formxo5j8158"
  style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit" on="submit:AMP.setState({formxo5j8158:{formHistory: formxo5j8158.formHistory.splice(formxo5j8158.formHistory.length,0,formxo5j8158.currentStep) 
  , currentStep: 'stepra77z1'}})" action-xhr="https://google.com">
  <div class="overall screen current_screen" style="box-sizing:border-box">
  <div class="element-wrapper field-wrap">
  <div class="question">
  <h2>Principal Amount</h2>
  </div>
  <div class="answer">
  <div class="input-outer input-wrap" style="display:flex;flex-direction:row; align-items: center;">
  <span class="prefix">$ </span>
  <input class="input-style" required type="number" name="PrincipalAmount" id="elementst0oh2"
  placeholder="Enter Loan Amount" style="box-sizing:border-box"
  [value]="formxo5j8158.responses.stepv119k145.elementst0oh2 || ''"
  pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({formxo5j8158:{
  responses: {stepv119k145:{elementst0oh2: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
  validation-for="elementst0oh2">This field is required</div>
  <div visible-when-invalid="patternMismatch" validation-for="elementst0oh2"
  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
  <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
  validation-for="elementst0oh2">Invalid input, number expected</div>
  </div>
  </div>
  <div class="element-wrapper field-wrap">
  <div class="question">
  <h2>Interest Rate</p>
  </div>
  <div class="answer">
  <div class="input-outer input-wrap" style="display:flex;flex-direction:column">
  <input class="input-style" required type="number" name="InterestRate" id="elementaa3vl4"
  placeholder="Enter rate in %" style="box-sizing:border-box"
  [value]="formxo5j8158.responses.stepv119k145.elementaa3vl4 || ''"
  pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({formxo5j8158:{
  responses: {stepv119k145:{elementaa3vl4: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
  validation-for="elementaa3vl4">This field is required</div>
  <div visible-when-invalid="patternMismatch" validation-for="elementaa3vl4"
  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
  <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
  validation-for="elementaa3vl4">Invalid input, number expected</div>
  </div>
  </div>
  <div class="element-wrapper field-wrap">
  <div class="question">
  <h2>Tenure in Years</h2>
  </div>
  <div class="answer">
  <div class="input-outer input-wrap" style="display:flex;flex-direction:column">
  <input class="input-style" required type="number" name="LoanTenure" id="element232766"
  placeholder="Enter no. of years" style="box-sizing:border-box"
  [value]="formxo5j8158.responses.stepv119k145.element232766 || ''"
  pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({formxo5j8158:{
  responses: {stepv119k145:{element232766: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
  validation-for="element232766">This field is required</div>
  <div visible-when-invalid="patternMismatch" validation-for="element232766"
  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
  <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
  validation-for="element232766">Invalid input, number expected</div>
  </div>
  </div>
  <input hidden id="fuuid" name="fuuid" [value]="formxo5j8158.fuuid"> <input hidden id="next-step-id"
  name="next-step-id" [value]="'stepra77z1'"> <input hidden id="total-steps" name="total-steps"
  value="3">
  <div class="navigation-button-wrapper">
  <!-- Change CTA-->
  <button class="button" type="submit">
  <p>Calculate</p>
  </button>
  <!-- Change CTA-->
  </div>
  </div>
  </form>
  <form id="formWidgetFallbackAnchorLinkformxo5j8158" class="formxo5j8158 result-wrap"
  style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit"
  on="submit-success:AMP.setState({formxo5j8158:{currentStep: 'success'}})"
  action-xhr="https://google.com">
  <div class="overall screen current_screen" style="box-sizing:border-box" hidden
  [hidden]="formxo5j8158.currentStep != 'stepra77z1'">
  <div class="element-wrapper field-wrap">
  <div class="question"></div>
  <div class="answer">
  <amp-bind-macro id="elementzzr6o10Formula" arguments="element232766,elementaa3vl4,elementst0oh2"
  expression="((((+elementst0oh2 * (+elementaa3vl4 / 1200)) * pow((1 + (+elementaa3vl4 / 1200)), (+element232766 * 12))) / (pow((1 + (+elementaa3vl4 / 1200)), (+element232766 * 12)) - 1)) || 0).toFixed(2)"></amp-bind-macro>
  <h2 class="result-title">Result</h2>
  <div class="result-output">
  <h3 class="total-text">EMI Per Month</h3>
  <input hidden id="elementzzr6o10" name="elementzzr6o10"
  [value]="elementzzr6o10Formula(formxo5j8158.responses.stepv119k145.element232766,formxo5j8158.responses.stepv119k145.elementaa3vl4,formxo5j8158.responses.stepv119k145.elementst0oh2)">
  <span class="formula-result total-value"
  [text]="elementzzr6o10Formula(formxo5j8158.responses.stepv119k145.element232766,formxo5j8158.responses.stepv119k145.elementaa3vl4,formxo5j8158.responses.stepv119k145.elementst0oh2)">0</span>
  </div>
  </div>
  </div>
  <input hidden id="fuuid" name="fuuid" [value]="formxo5j8158.fuuid"> <input hidden id="next-step-id"
  name="next-step-id" [value]="'success'"> <input hidden id="total-steps" name="total-steps"
  value="3">
  <div class="navigation-button-wrapper">
  <button class="button" type="submit">
  Go to website
  </button>
  <button class="button" type="button" on="tap:AMP.setState({
  formxo5j8158: {
  responses: {
  stepv119k145: {
  elementst0oh2: '',
  elementaa3vl4: '',
  element232766: ''
  }
  },
  currentStep: 'stepv119k145'
  }
  })">
  Calculate AGAIN
  </button>

  </div>
  </div>
  </form>
  </div>
  </div>
  <!-- Footer Section -->
  <footer class="footer">
  <ul class="media-logo-list">
  <!-- Footer Link -->
  <!-- Social Links -->
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/bd1ea3eef7974e80b8ab9306bce4fd7f.png" alt="instagram"
  class="media-logo" width="20" height="20"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fbfd5b911f9442a48e555b2c4bb75fab.png" alt="facebook"
  class="media-logo" width="20" height="20"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/908da4928efe4beba4828e7497a2a93f.png" alt="x"
  class="media-logo" width="20" height="20"></amp-img>
  </a>
  </li>
  <!-- Social Links -->
  <!-- Footer Link -->
  </ul>
  <p class="f-desc">
  For assistance, connect with us on social media or reach out to our support team at support@example.com </p>
  <p class="f-desc" style="margin-top: 50px;">To opt out of promotional emails like this, <a href="https://google.com"
  style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
  </footer>
  </div>
  </body>

  </html>
  ```
</details>

## SIP Calculator Template

This AMP template allows users to calculate the potential returns of their Systematic Investment Plan (SIP) right within the email. By entering basic investment details such as monthly contribution, duration, and expected return rate, users get instant projections, creating a smooth, informative experience that supports smarter financial decisions.

<Image align="center" alt="Sample SIP Calculator Template" border={true} caption="Sample SIP Calculator Template" src="https://files.readme.io/0bfead2af5fe6db82b947443e276b647d357044f2beda009bb8660e29536044c-SIP_Calculator_AMP.png" width="35% " />

<details>
  <summary><b>Expand to know more about the template.</b></summary>

  ### Use Case Examples

  * Educate users about SIP benefits while promoting mutual fund products.
  * Encourage investment planning by allowing quick in-email projections.
  * Enable financial goal-based marketing through interactive calculators.
  * Re-engage users by helping them visualize long-term returns.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>

  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }

  body {
  font-family: arial, sans-serif;
  font-weight: 400;
  background-color: #f5f5f5;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  }

  img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }

  /* Change Theme */
  .main {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: 0 auto;
  background: #f5f5f5;
  flex: 1;
  }

  /* Change Theme */
  @media only screen and (max-width: 400px) {
  .main {
  max-width: 100%;
  }
  }

  .logo-wrap {
  padding: 12px 24px;
  background-color: #F5F5F5;
  border-radius: 0 0 41px 41px;
  text-align: center;
  z-index: 2;
  position: relative;
  }

  .logo-wrap .img-wrap {
  max-width: 145.78px;
  max-height: 74.89px;
  }

  .footer {
  width: 90%;
  margin: 45px auto 0;
  background: #ffffff;
  border-radius: 24px 24px 0 0;
  background-color: #ffffff;
  padding: 1px 0 33px;
  }

  .media-logo-list {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  gap: 16px;
  margin: 32px 0 17px;
  }

  .media-logo-list .logo-item {
  width: 20px;
  height: 20px;
  }

  .media-logo-list .logo-item .logo-link {
  width: 100%;
  height: 100%;
  display: inline-block;
  }

  .f-desc {
  font-size: 12px;
  font-weight: 400;
  line-height: 20px;
  color: #6f6f6f;
  text-align: center;
  max-width: 95%;
  margin: 0 auto;
  text-transform: none;
  }

  .banner {
  margin: -35px;
  }

  .banner .img-wrap {
  max-height: 381px;
  width: 100%;
  }

  .calculator-wrap {
  width: 90%;
  position: relative;
  border-radius: 24px;
  background-color: #ffffff;
  margin: -62px auto 0;
  }

  .calculator-wrap .form-wrap {
  padding: 24px 26px 40px;
  }

  .form-wrap .text {
  font-size: 20px;
  line-height: 28px;
  font-weight: 400;
  color: #3D3D3D;
  align-items: center;
  }

  .form-wrap .calculator-title {
  padding: 8px 0 32px;
  font-size: 32px;
  font-weight: 400;
  line-height: 38px;
  }

  .form-wrap .calculator-title span {
  color: #4140FF;
  }

  .form-wrap label,
  .question h2 {
  display: block;
  padding-bottom: 13px;
  font-size: 16px;
  font-weight: 400;
  line-height: 20px;
  }

  .field-wrap .answer {
  margin-bottom: 32px;
  }

  .field-wrap .input-wrap {
  border-radius: 79px;
  border: 0.82px solid #5a5959;
  padding: 15px;
  }

  .form-wrap input,
  .input-style {
  width: 95%;
  text-indent: 5px;
  color: #000000;
  font-size: 16px;
  line-height: 23px;
  border: 0;
  outline: 0;
  }

  .form-wrap button,
  .button {
  width: 100%;
  border-radius: 50px;
  padding: 13px;
  background: #3e3cf9;
  color: #ffffff;
  font-weight: 400;
  font-size: 16px;
  line-height: 23px;
  border: 0.82px solid #5a5959;
  text-decoration: none;
  text-align: center;
  display: block;
  text-transform: none;
  }

  .form-wrap button:disabled,
  .disabled {
  background: #D8D8FE;
  }

  .calculator-wrap .result-wrap {
  padding: 64px 0 0;
  }

  .result-wrap .result-title {
  padding: 0 0 12px;
  font-size: 32px;
  font-weight: 400;
  line-height: 38px;
  }

  .result-wrap .result-output {
  display: flex;
  justify-content: space-between;
  max-width: 464px;
  height: 76px;
  align-items: center;
  border-radius: 0 0 41px 41px;
  border-bottom: 0.82px solid #5a5959;
  margin-bottom: 29px;
  padding: 0 22px;
  }

  .result-output .total-text {
  font-size: 16px;
  font-weight: 400;
  line-height: 19.36px;
  text-align: center;
  }

  .result-output .total-value {
  font-size: 24px;
  font-weight: 400;
  line-height: 29.05px;
  text-align: center;
  }

  .result-wrap button {
  width: 100%;
  border-radius: 79.98px;
  padding: 13px;
  background: #3e3cf9;
  color: #ffffff;
  font-weight: 400;
  font-size: 16px;
  line-height: 23px;
  border: 0.82px solid #5a5959;
  margin-bottom: 11px;
  cursor: pointer;
  }

  .result-wrap button.disabled,
  .result-wrap button:disabled,
  .result-wrap .button.disabled,
  .result-wrap .button:disabled {
  opacity: 0.5;
  }

  @media only screen and (max-width: 480px) {
  .logo-wrap .img-wrap {
  max-width: 130px;
  max-height: 60px;
  }

  .form-wrap input,
  .input-style {
  width: 90%;
  }

  .calculator-wrap .form-wrap {
  padding: 20px 20px 40px;
  }

  .calculator-wrap .result-wrap {
  padding: 40px 0 0;
  }

  .result-wrap .result-title {
  font-size: 25px;
  line-height: 30px;
  }

  .form-wrap .calculator-title {
  padding: 8px 0 25px;
  font-size: 25px;
  line-height: 30px;
  }

  .field-wrap .input-wrap {
  padding: 10px;
  }

  .form-wrap .text {
  font-size: 15px;
  line-height: 20px;
  }

  .result-output .total-value {
  font-size: 20px;
  line-height: 24px;
  }

  .result-wrap .result-output {
  padding: 20px 15px;
  height: auto;
  }

  .form-wrap .question {
  padding-bottom: 8px;
  }
  }

  @media only screen and (max-width: 300px) {
  .product-wrap {
  padding: 40px 5px 20px;
  }
  }
  </style>
  </head>

  <body>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <!-- Change Logo -->
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo"
  width="159" height="73"></amp-img>
  <!-- Change Logo -->
  </div>
  </div>
  </header>
  <div class="banner">
  <div class="img-wrap">
  <!-- Change Banner -->
  <amp-img layout="responsive"
  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/stacks-coins-arranged-bar-graph%201.png"
  alt="Banner" width="600" height="381"></amp-img>
  <!-- Change Banner -->
  </div>
  </div>
  <div class="calculator-wrap">
  <div on="tap:AMP.setState({
  form6850m49: {
  fuuid: form6850m49.fuuid || floor(random() * 100000),
  responses: {
  stepag3y745:{
  elementvw5q7629:elementvw5q7629Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628),elementa1mgz630:elementa1mgz630Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628,form6850m49.responses.steprj7lv44.elementwikv1627),element4q9av631:element4q9av631Formula(form6850m49.responses.stepag3y745.elementa1mgz630,form6850m49.responses.stepag3y745.elementvw5q7629)
  }
  }
  }
  })" role="tab" tabindex="1" class="form-wrap amp-form-block amp-html-block form6850m49-wrapper"
  style="margin:auto;text-align:left">
  <div class="data">
  <amp-state id="form6850m49">
  <script type="application/json">{"currentStep":"steprj7lv44","responses":{},"formHistory":[]}</script>
  </amp-state>
  </div>
  <p class="text">Instantly</p>
  <h2 class="calculator-title">Calculate Your <span> SIP Investment </span></h2>
  <form action-xhr="https://google.com" id="formWidgetFallbackAnchorLinkform6850m49" class="form6850m49"
  style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit" on="submit:AMP.setState({form6850m49:{formHistory: form6850m49.formHistory.splice(form6850m49.formHistory.length,0,form6850m49.currentStep) 
  , currentStep: 'stepag3y745'}})">
  <div class="overall screen current_screen" style="box-sizing:border-box">
  <div class="field-wrap">
  <div class="question">
  <h2>Monthly SIP Investment</h2>
  </div>
  <div class="answer">
  <div class="input-outer input-wrap" style="display:flex;flex-direction:row">
  <span class="prefix">$ </span>
  <input class="input-style" required type="number" name="element4b6vf626" id="element4b6vf626"
  placeholder="Enter SIP amount" style="box-sizing:border-box"
  [value]="form6850m49.responses.steprj7lv44.element4b6vf626 || ''"
  pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({form6850m49:{
  responses: {steprj7lv44:{element4b6vf626: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
  validation-for="element4b6vf626">This field is required</div>
  <div visible-when-invalid="patternMismatch" validation-for="element4b6vf626"
  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
  <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
  validation-for="element4b6vf626">Invalid input, number expected</div>
  </div>
  </div>
  <div class="field-wrap">
  <div class="question">
  <h2>Rate of Return ( in % )</h2>
  </div>
  <div class="answer">
  <div class="input-outer input-wrap" style="display:flex;flex-direction:column">
  <input class="input-style" required type="number" name="elementwikv1627" id="elementwikv1627"
  placeholder="Enter rate in %" style="box-sizing:border-box"
  [value]="form6850m49.responses.steprj7lv44.elementwikv1627 || ''"
  pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({form6850m49:{
  responses: {steprj7lv44:{elementwikv1627: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
  validation-for="elementwikv1627">This field is required</div>
  <div visible-when-invalid="patternMismatch" validation-for="elementwikv1627"
  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
  <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
  validation-for="elementwikv1627">Invalid input, number expected</div>
  </div>
  </div>
  <div class="field-wrap">
  <div class="question">
  <h2>Tenure in Years</h2>
  </div>
  <div class="answer">
  <div class="input-outer input-wrap" style="display:flex;flex-direction:column"><input
  class="input-style" required type="number" name="elementhwgbp628" id="elementhwgbp628"
  placeholder="Enter no. of years" style="box-sizing:border-box"
  [value]="form6850m49.responses.steprj7lv44.elementhwgbp628 || ''"
  pattern="[-]?[\d\.]{0,200}" on="input-throttled:AMP.setState({form6850m49:{
  responses: {steprj7lv44:{elementhwgbp628: event.value}}}})"></div>
  <div visible-when-invalid="valueMissing" style="font-size:13px;padding-top:4px"
  validation-for="elementhwgbp628">This field is required</div>
  <div visible-when-invalid="patternMismatch" validation-for="elementhwgbp628"
  style="font-size:13px;margin-top:4px">Please enter a number of length 0 - 200 digits</div>
  <div visible-when-invalid="badInput" style="font-size:13px;margin-top:4px"
  validation-for="elementhwgbp628">Invalid input, number expected</div>
  </div>
  </div>
  <input hidden id="fuuid" name="fuuid" [value]="form6850m49.fuuid"> <input hidden id="next-step-id"
  name="next-step-id" [value]="'stepag3y745'"> <input hidden id="total-steps" name="total-steps"
  value="3">
  <div class="navigation-button-wrapper">
  <!-- Change CTA -->
  <button class="button" type="submit">
  <p>Calculate</p>
  </button>
  <!-- Change CTA -->
  </div>
  </div>
  </form>
  <form action-xhr="https://google.com" id="formWidgetFallbackAnchorLinkform6850m49" class="form6850m49"
  style="display:flex;flex-direction:column" method="post" custom-validation-reporting="show-all-on-submit"
  on="submit-success:AMP.setState({form6850m49:{currentStep: 'success'}})">
  <div class="result-wrap" style="box-sizing:border-box" hidden
  [hidden]="form6850m49.currentStep != 'stepag3y745'">
  <h2 class="result-title">Result</h2>
  <div class="element-wrapper">
  <div class="answer"><amp-bind-macro id="elementvw5q7629Formula"
  arguments="element4b6vf626,elementhwgbp628"
  expression="(((+element4b6vf626 * +elementhwgbp628) * 12) || 0).toFixed(2)"></amp-bind-macro>
  <div class="result-output"><span class="formula-sub-heading">
  <p>Total Investment</p>
  </span><input hidden id="elementvw5q7629" name="elementvw5q7629"
  [value]="elementvw5q7629Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628)">
  <span class="formula-result total-value" style="font-family:Arial, sans-serif"
  [text]="elementvw5q7629Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628)">0</span>
  </div>
  </div>
  </div>
  <div class="element-wrapper">
  <div class="answer"><amp-bind-macro id="elementa1mgz630Formula"
  arguments="element4b6vf626,elementhwgbp628,elementwikv1627"
  expression="(((+element4b6vf626 * ((pow((1 + (+elementwikv1627 / 1200)), ((12 * +elementhwgbp628) + 1)) - 1) / (+elementwikv1627 / 1200))) - +element4b6vf626) || 0).toFixed(2)"></amp-bind-macro>
  <div class="result-output"><span class="formula-sub-heading">
  <p>Total Maturity Amount</p>
  </span><input hidden id="elementa1mgz630" name="elementa1mgz630"
  [value]="elementa1mgz630Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628,form6850m49.responses.steprj7lv44.elementwikv1627)">
  <span class="formula-result total-value" style="font-family:Arial, sans-serif"
  [text]="elementa1mgz630Formula(form6850m49.responses.steprj7lv44.element4b6vf626,form6850m49.responses.steprj7lv44.elementhwgbp628,form6850m49.responses.steprj7lv44.elementwikv1627)">0</span>
  </div>
  </div>
  </div>
  <div class="element-wrapper">
  <div class="answer"><amp-bind-macro id="element4q9av631Formula"
  arguments="elementa1mgz630,elementvw5q7629"
  expression="((+elementa1mgz630 - +elementvw5q7629) || 0).toFixed(2)"></amp-bind-macro>
  <div class="result-output"><span class="formula-sub-heading">
  <p>Interest Earned</p>
  </span><input hidden id="element4q9av631" name="element4q9av631"
  [value]="element4q9av631Formula(form6850m49.responses.stepag3y745.elementa1mgz630,form6850m49.responses.stepag3y745.elementvw5q7629)">
  <span class="formula-result total-value" style="font-family:Arial, sans-serif"
  [text]="element4q9av631Formula(form6850m49.responses.stepag3y745.elementa1mgz630,form6850m49.responses.stepag3y745.elementvw5q7629)">0</span>
  </div>
  </div>
  </div><input hidden id="fuuid" name="fuuid" [value]="form6850m49.fuuid"> <input hidden id="next-step-id"
  name="next-step-id" [value]="'success'"> <input hidden id="total-steps" name="total-steps"
  value="3">
  <div class="navigation-button-wrapper">
  <button class="button" type="submit">
  Go to website
  </button>
  <button class="button" type="button" on="tap:AMP.setState({
  form6850m49: {
  responses: {
  steprj7lv44: {
  element4b6vf626: '',
  elementwikv1627: '',
  elementhwgbp628: ''
  }
  },
  currentStep: 'steprj7lv44'
  }
  })">
  Calculate AGAIN
  </button>
  </div>
  </div>
  </form>
  </div>
  </div>
  <!-- Footer Section -->
  <footer class="footer">
  <ul class="media-logo-list">


  <!-- Footer Link -->
  <!-- Social Links -->
  <li class="logo-item"><a href="https://www.google.co.in/" class="logo-link"><amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/bd1ea3eef7974e80b8ab9306bce4fd7f.png" alt="instagram"
  class="media-logo" width="20" height="20"></amp-img></a></li>
  <li class="logo-item"><a href="https://www.google.co.in/" class="logo-link"><amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fbfd5b911f9442a48e555b2c4bb75fab.png" alt="facebook"
  class="media-logo" width="20" height="20"></amp-img></a></li>
  <li class="logo-item"><a href="https://www.google.co.in/" class="logo-link"><amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/908da4928efe4beba4828e7497a2a93f.png" alt="x"
  class="media-logo" width="20" height="20"></amp-img></a></li>
  <!-- Footer Link -->
  <!-- Social Links -->

  </ul>
  <p class="f-desc">For assistance, connect with us on social media or reach out to our support team at support@example.com</p>
  <p class="f-desc" style="margin-top: 50px;">To opt out of promotional emails like this, <a href="https://google.com"
  style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
  </footer>
  <!-- Footer Section -->
  </div>
  </body>

  </html>
  ```
</details>

## Insurance Premium Calculator Template

This AMP template empowers users to estimate insurance premiums based on parameters such as coverage amount, age, and policy term right within their inbox. It also enables users to explore coverage options and assess affordability instantly, making the research and decision-making process much more convenient and personalized.

<Image align="center" alt="Sample Premium Calculator Template" border={true} caption="Sample Premium Calculator Template" src="https://files.readme.io/f95f0f21079c99d5fcff4395c0b5322e87a7bef9e74c8c4c6e0f127cc0381fe8-Insurance_Premium_Calculator.png" width="35% " />

<details>
  <summary>Expand to know more about the template.</summary>

  ### Use Case Examples

  * Promote insurance plans with embedded quote estimators.
  * Help users calculate premiums before applying for a policy.
  * Improve lead conversion by reducing drop-offs during research.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <script async custom-element="amp-selector" src="https://cdn.ampproject.org/v0/amp-selector-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  background-color: #f5f5f5;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  }
  img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }
  /* Change Theme */
  .main {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: 0 auto;
  background: #f5f5f5;
  flex: 1;
  }
  /* Change Theme */
  @media only screen and (max-width: 400px) {
  .main {
  max-width: 100%;
  }
  }
  .logo-wrap {
  padding: 12px 24px;
  background-color: #F5F5F5;
  border-radius: 0 0 41px 41px;
  text-align: center;
  z-index: 2;
  position: relative;
  }
  .logo-wrap .img-wrap {
  max-width: 145.78px;
  max-height: 74.89px;
  }
  .footer {
  width: 90%;
  margin: 45px auto 0;
  background: #ffffff;
  border-radius: 24px 24px 0 0;
  background-color: #ffffff;
  padding: 1px 0 33px;
  }
  .media-logo-list {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  gap: 16px;
  margin: 32px 0 17px;
  }
  .media-logo-list .logo-item {
  width: 20px;
  height: 20px;
  }
  .media-logo-list .logo-item .logo-link {
  width: 100%;
  height: 100%;
  display: inline-block;
  }
  .f-desc {
  font-size: 12px;
  font-weight: 400;
  line-height: 20px;
  color: #6f6f6f;
  text-align: center;
  max-width: 95%;
  margin: 0 auto;
  text-transform: none;
  }
  .banner {
  margin: -35px;
  }
  .banner .img-wrap {
  max-height: 381px;
  width: 100%;
  }
  .calculator-wrap {
  width: 90%;
  position: relative;
  border-radius: 24px;
  background-color: #ffffff;
  margin: -62px auto 0;
  }
  .calculator-wrap .form-wrap {
  padding: 24px 26px 40px;
  }
  .form-wrap .text {
  font-size: 20px;
  line-height: 28px;
  font-weight: 400;
  color: #3D3D3D;
  align-items: center;
  }
  .form-wrap .calculator-title {
  padding: 8px 0 32px;
  font-size: 32px;
  font-weight: 400;
  line-height: 38px;
  }
  .form-wrap .calculator-title span {
  color: #4140FF;
  }
  .form-wrap label {
  display: block;
  padding-bottom: 13px;
  font-size: 16px;
  font-weight: 400;
  line-height: 20px;
  }
  .field-wrap {
  margin-bottom: 32px;
  }
  .field-wrap .input-wrap {
  border-radius: 79px;
  border: 0.82px solid #5a5959;
  padding: 15px;
  }
  .form-wrap input,
  .form-wrap select {
  width: 95%;
  text-indent: 5px;
  color: #000000;
  background: #ffffff;
  font-size: 16px;
  line-height: 23px;
  border: 0;
  outline: 0;
  }
  .form-wrap select option {
  margin-top: 10px;
  padding: 15px 5px;
  font-size: 16px;
  line-height: 23px;
  }
  .form-wrap button,
  .button {
  width: 100%;
  border-radius: 50px;
  padding: 13px;
  background: #3e3cf9;
  color: #ffffff;
  font-weight: 400;
  font-size: 16px;
  line-height: 23px;
  border: 0.82px solid #5a5959;
  text-decoration: none;
  text-align: center;
  display: block;
  text-transform: none;
  }
  .form-wrap button:disabled,
  .disabled {
  background: #D8D8FE;
  }
  .calculator-wrap .result-wrap {
  padding: 64px 0 0;
  }
  .result-wrap .result-title {
  padding: 0 0 12px;
  font-size: 32px;
  font-weight: 400;
  line-height: 38px;
  }
  .result-wrap .result-output {
  display: flex;
  justify-content: space-between;
  max-width: 464px;
  height: 76px;
  align-items: center;
  border-radius: 0 0 41px 41px;
  border-bottom: 0.82px solid #5a5959;
  margin-bottom: 29px;
  padding: 0 22px;
  }
  .result-output .total-text {
  font-size: 16px;
  font-weight: 400;
  line-height: 19.36px;
  text-align: center;
  }
  .result-output .total-value {
  font-size: 24px;
  font-weight: 400;
  line-height: 29.05px;
  text-align: center;
  }
  .result-wrap button {
  width: 100%;
  border-radius: 79.98px;
  padding: 13px;
  background: #3e3cf9;
  color: #ffffff;
  font-weight: 400;
  font-size: 16px;
  line-height: 23px;
  border: 0.82px solid #5a5959;
  margin-bottom: 11px;
  cursor: pointer;
  }
  .result-wrap button.disabled,
  .result-wrap button:disabled {
  opacity: 0.5;
  }
  @media only screen and (max-width: 480px) {
  .result-output .total-text {
  margin-bottom: 10px;
  }
  .logo-wrap .img-wrap {
  max-width: 130px;
  max-height: 60px;
  }
  .form-wrap input {
  width: 90%;
  }
  .calculator-wrap .form-wrap {
  padding: 20px 20px 40px;
  }
  .calculator-wrap .result-wrap {
  padding: 40px 0 0;
  }
  .result-wrap .result-title {
  font-size: 25px;
  line-height: 30px;
  }
  .form-wrap .calculator-title {
  padding: 8px 0 25px;
  font-size: 25px;
  line-height: 30px;
  }
  .field-wrap .input-wrap {
  padding: 10px;
  }
  .form-wrap .text {
  font-size: 15px;
  line-height: 20px;
  }
  .result-output .total-value {
  font-size: 20px;
  line-height: 24px;
  }
  .result-wrap .result-output {
  padding: 20px 15px;
  height: auto;
  flex-wrap: wrap;
  }
  .form-wrap label {
  padding-bottom: 8px;
  }
  }
  @media only screen and (max-width: 300px) {
  .product-wrap {
  padding: 40px 5px 20px;
  }
  }
  </style>
  </head>
  <body>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <!-- Change Logo image src as per your requirements -->
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo"
  width="159" height="73" />
  <!-- Change Logo image src as per your requirements -->
  </div>
  </div>
  </header>
  <div class="banner">
  <div class="img-wrap">
  <!-- Change Banner image src as per your requirements -->
  <amp-img layout="responsive"
  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/SIP-Calculator/stacks-coins-arranged-bar-graph%201.png"
  alt="Banner" width="600" height="381"></amp-img>
  <!-- Change Banner image src as per your requirements -->
  </div>
  </div>
  <div class="calculator-wrap">
  <div on="tap:AMP.setState({
  formInsuranceCalc: {
  fuuid: formInsuranceCalc.fuuid || floor(random() * 100000),
  responses: {
  stepInsuranceResult: {
  insuranceResult: insuranceFormula(
  formInsuranceCalc.responses.stepInsuranceInput.sumInsured,
  formInsuranceCalc.responses.stepInsuranceInput.premium,
  formInsuranceCalc.responses.stepInsuranceInput.policyTenure,
  formInsuranceCalc.responses.stepInsuranceInput.age,
  formInsuranceCalc.responses.stepInsuranceInput.coverageType
  )
  }
  }
  }
  })" class="form-wrap amp-form-block amp-html-block formInsuranceCalc-wrapper" style="margin:auto;text-align:left">
  <!-- Initial form state -->
  <amp-state id="formInsuranceCalc">
  <script type="application/json">{"currentStep":"stepInsuranceInput","responses":{},"formHistory":[]}</script>
  </amp-state>
  <h2 class="calculator-title">Calculate Your Premium</h2>
  <form id="formWidgetInsuranceCalc" method="post" custom-validation-reporting="show-all-on-submit"
  on="submit:AMP.setState({formInsuranceCalc:{formHistory: formInsuranceCalc.formHistory.splice(formInsuranceCalc.formHistory.length,0,formInsuranceCalc.currentStep) , currentStep: 'stepInsuranceResult'}})"
  action-xhr="https://google.com">
  <!-- Sum Insured -->
  <div class="field-wrap">
  <label>Sum Insured</label>
  <div class="input-wrap">
  <span class="prefix">$ </span>
  <input type="number" class="input-style" name="sumInsured" id="sumInsured"
  placeholder="Enter sum insured" required
  [value]="formInsuranceCalc.responses.stepInsuranceInput.sumInsured || ''"
  on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{sumInsured: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" validation-for="sumInsured" style="font-size:13px;padding-top:4px">
  This field is required
  </div>
  </div>
  <!-- Premium -->
  <!-- <div class="field-wrap">
  <label>Premium Amount ($)</label>
  <div class="input-wrap">
  <span class="prefix">$ </span>
  <input type="number" class="input-style" name="premium" id="premium" placeholder="Enter premium amount"
  required pattern="[-]?[\d\.]{0,200}"
  [value]="formInsuranceCalc.responses.stepInsuranceInput.premium || ''"
  on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{premium: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" validation-for="premium" style="font-size:13px;padding-top:4px">
  This field is required
  </div>
  </div> -->
  <!-- Policy Tenure -->
  <div class="field-wrap">
  <label>Policy Tenure in Years</label>
  <div class="input-wrap">
  <input type="number" class="input-style" name="policyTenure" id="policyTenure"
  placeholder="Enter no. of years" required pattern="[-]?[\d\.]{0,200}"
  [value]="formInsuranceCalc.responses.stepInsuranceInput.policyTenure || ''"
  on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{policyTenure: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" validation-for="policyTenure"
  style="font-size:13px;padding-top:4px">
  This field is required
  </div>
  </div>
  <!-- Age -->
  <div class="field-wrap">
  <label>Age</label>
  <div class="input-wrap">
  <input type="number" class="input-style" name="age" id="age" placeholder="Enter age" required
  pattern="[-]?[\d\.]{0,200}" [value]="formInsuranceCalc.responses.stepInsuranceInput.age || ''"
  on="input-throttled:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{age: event.value}}}})">
  </div>
  <div visible-when-invalid="valueMissing" validation-for="age" style="font-size:13px;padding-top:4px">
  This field is required
  </div>
  </div>
  <!-- Coverage Type -->
  <div class="field-wrap">
  <label>Insurance Type</label>
  <div class="input-wrap">
  <select id="coverageType" name="coverageType"
  on="change:AMP.setState({formInsuranceCalc:{responses:{stepInsuranceInput:{coverageType: event.value}}}})">
  <option value="Health insurance">Health insurance</option>
  <option value="Life insurance">Life insurance</option>
  </select>
  </div>
  </div>
  <input hidden id="fuuid" name="fuuid" [value]="formInsuranceCalc.fuuid">
  <input hidden id="next-step-id" name="next-step-id" value="stepInsuranceResult">
  <div class="navigation-button-wrapper">
  <!-- Change CTA -->
  <button class="button" type="submit">Calculate</button>
  <!-- Change CTA -->
  </div>
  </form>
  <!-- Result screen -->
  <form class="result-wrap" method="post" hidden action-xhr="https://google.com"
  [hidden]="formInsuranceCalc.currentStep != 'stepInsuranceResult'">
  <div class="field-wrap">
  <amp-bind-macro id="insuranceFormula" arguments="sumInsured,premium,policyTenure,age, coverageType"
  expression="(((((+sumInsured * +premium) / (+policyTenure + +age)) * (coverageType == 'Life insurance' ? 1.1 : 1)) || 0).toFixed(2))"></amp-bind-macro>
  <h2 class="result-title">Insurance Premium Result</h2>
  <div class="result-output">
  <h3 class="total-text">Total Premium:</h3>
  <span class="formula-result total-value"
  [text]="insuranceFormula(formInsuranceCalc.responses.stepInsuranceInput.sumInsured,formInsuranceCalc.responses.stepInsuranceInput.premium,formInsuranceCalc.responses.stepInsuranceInput.policyTenure,formInsuranceCalc.responses.stepInsuranceInput.age,formInsuranceCalc.responses.stepInsuranceInput.coverageType)">
  0
  </span>
  </div>
  </div>
  <input hidden id="fuuid" name="fuuid" [value]="formInsuranceCalc.fuuid">
  <div class="navigation-button-wrapper">
  <button class="button" type="submit">
  Visit website
  </button>
  <button class="button" type="button" on="tap:AMP.setState({
  formInsuranceCalc: {
  responses: {
  stepInsuranceInput: {
  sumInsured: '', premium: '', policyTenure: '', age: '', coverageType: 'Health insurance'
  }
  },
  currentStep: 'stepInsuranceInput'
  }
  })">
  Calculate Again
  </button>
  </div>
  </form>
  </div>
  </div>
  <!-- Footer Section -->
  <footer class="footer">
  <ul class="media-logo-list">
  <!-- Footer Links -->
  <!-- Social Links -->
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/bd1ea3eef7974e80b8ab9306bce4fd7f.png" alt="instagram"
  class="media-logo" width="20" height="20"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/fbfd5b911f9442a48e555b2c4bb75fab.png" alt="facebook"
  class="media-logo" width="20" height="20"></amp-img>
  </a>
  </li>
  <li class="logo-item">
  <a href="https://www.google.co.in/" class="logo-link">
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/908da4928efe4beba4828e7497a2a93f.png" alt="x"
  class="media-logo" width="20" height="20"></amp-img>
  </a>
  </li>
  <!-- Footer Links -->
  <!-- Social Links -->
  </ul>
  <p class="f-desc">
  For assistance, connect with us on social media or reach out to our support team at support@example.com 
  </p>
  <p class="f-desc" style="margin-top: 50px;">To opt out of promotional emails like this, <a href="https://google.com"
  style="color:#1E1E1E;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
  </footer>
  <!-- Footer Section -->
  </div>
  </body>
  </html>
  ```
</details>

## Product Recommendations Template

This AMP template dynamically showcases relevant products based on a user’s past browsing or purchase behavior. It displays collections or personalized categories and allows users to apply filters and explore product grids without leaving the email. With built-in interactivity and clear CTAs such as Shop Now and See More, this template is designed to drive high engagement and product discovery.

<Image align="center" alt="Sample Product Recommendations Template" border={true} caption="Sample Product Recommendations Template" src="https://files.readme.io/40e6d2bbef79979989ac846fb018ed1588439e65f7071c1781fc61d7001ebdb1-Product_Recommendations_AMP.png" width="25% " />

<details>
  <summary>Expand to know more about the template.</summary>

  ### Use Case Examples

  * Recommend products personalized to users’ past interactions or preferences.
  * Launch seasonal or trending collections in an interactive format.
  * Encourage repeat purchases with dynamic product carousels and filters.
  * Promote gender- or category-specific catalogs (for example, Men/Women collections).

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer]()
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)
  * [Add or Modify Filters](doc:ootb-email-templates#add-or-modify-filters)

  ### Template Code

  ```html
  <!doctype html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.1.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-selector" src="https://cdn.ampproject.org/v0/amp-selector-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  background: #F5F5F5;
  }
  img{
  width: 100%;
  height: 100%;
  object-fit: cover;
  }
  @media only screen and (max-width: 400px) {
  .main {
  max-width: 95%;
  }
  }
  .logo-wrap {
  padding: 17px 0;
  }
  .title {
  margin: 31px 0 10px;
  font-size: 30px;
  font-weight: 400;
  line-height: 43.35px;
  text-align: center;
  color: #000000;
  text-transform: To opt out of promotional emails like this,;
  }
  .para {
  margin: 0 auto;
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  text-align: center;
  color: #6F6F6F;
  text-transform: To opt out of promotional emails like this,;
  max-width: 70%;
  }
  .category-btn-wrap {
  margin: 30px 0 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  }
  .wrapper {
  padding: 0 25px;
  }
  .btn {
  border: 1px solid #1DBF73;
  background: #1DBF73;
  color: #FFFFFF;
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-transform: To opt out of promotional emails like this,;
  text-align: center;
  padding: 6px;
  margin: 0 5px;
  max-width: 95px;
  width: 100%;
  display: inline-block;
  text-decoration: none;
  }
  .btn.typ-secondary {
  color: #1DBF73;
  background: #FFFFFF;
  }
  .sec-title {
  margin: 0 0 15px;
  font-size: 22px;
  font-weight: 400;
  line-height: 25px;
  text-transform: To opt out of promotional emails like this,;
  color: #1E1E1E;
  }
  .product-list {
  padding: 0;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 15px;
  flex-wrap: wrap;
  list-style: none;
  }
  .product-list .product-item {
  width: 48%;
  }
  .product-card {
  padding: 5px;
  background: #EFEFEF;
  }
  .product-card .img-wrap {
  max-width: 258px;
  max-height: 174px;
  margin-bottom: 5px;
  width: 100%;
  height: 100%;
  }
  .product-card .content-wrap {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  }
  .product-card .content-wrap .lhs {
  width: 80%;
  }
  .product-card .content-wrap .rhs {
  width: 20%;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  }
  .p-title {
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  color: #1E1E1E;
  text-transform: To opt out of promotional emails like this,;
  }
  .p-desc {
  color: #909090;
  font-size: 8px;
  font-weight: 400;
  line-height: 13px;
  text-transform: none;
  }
  .p-amt {
  font-size: 12px;
  font-style: italic;
  font-weight: 400;
  line-height: 25px;
  text-align: right;
  color: #252525;
  }
  .rupee {
  font-size: 10px;
  }
  .p-link {
  max-width: 92%;
  margin: 5px 0 0;
  border: 1px solid #1DBF73;
  background: #1DBF73;
  color: #1E1E1E;
  font-size: 10px;
  font-weight: 400;
  line-height: 13px;
  text-transform: To opt out of promotional emails like this,;
  text-align: center;
  padding: 6px 10px;
  display: block;
  text-decoration: none;
  }
  .btn-wrap {
  text-align: center;
  margin: 28px 0 50px;
  }
  .media-logo {
  width: 20px;
  height: 20px;
  }
  .color-list{
  display: flex;
  justify-items: flex-end;
  align-items: center;
  list-style: none;
  gap: 5px;
  }
  amp-selector [option]{
  outline: 1px solid #00000033;
  }
  amp-selector [option][selected]{
  outline: 1px solid #1DBF73;
  }
  @media screen and (max-width: 480px) {
  .wrapper {
  padding: 0 10px;
  }
  .product-list {
  gap: 10px;
  }
  .product-card .content-wrap .lhs {
  width: 70%;
  }
  .product-card .content-wrap .rhs {
  width: 30%;
  }
  .p-title {
  line-height: 18px;
  }
  }
  @media screen and (max-width: 300px) {
  .product-list .product-item {
  width: 100%;
  }
  }
  </style>
  </head>
  <body>
  <!-- AMP state for handling category selection -->
  <amp-state id="selectedCategory">
  <script type="application/json">
  { "value": "men" }
  </script>
  </amp-state>
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; position: relative;" class="main">
  <tbody><!-- header start-->
  <tr>
  <td style="text-align: center; vertical-align: middle; padding: 20px">
  <amp-img width="159" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" class="logo" alt="Logo" style="display: inline-block; object-fit: cover;"/>
  </td>
  </tr>
  <!-- header end-->
  <!-- Banner slider start-->
  <tr>
  <td align="center">
  <div class="banner">
  <amp-carousel width="600" height="400" layout="responsive" type="slides" autoplay loop delay="10000" role="region" aria-label="banner carousel with autoplay">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/banner-1.png" width="600" height="400" layout="responsive" alt="a sample image"></amp-img>
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/banner-2.png" width="600" height="400" layout="responsive" alt="another sample image"></amp-img>
  </amp-carousel>
  </div>
  </td>
  </tr>
  <!-- Banner slider end-->
  <!-- Change CTA -->
  <tr>
  <td align="center">
  <h1 class="title">PICKS FOR YOU</h1>
  <p class="para">We’ve handpicked products we think you’ll love! Browse through some of our most recent additions.</p>
  <div class="category-btn-wrap">
  <button class="btn" [class]="'btn ' + (selectedCategory.value == 'men' ? '' : 'typ-secondary')" value="men" on="tap:AMP.setState({selectedCategory: {value: 'men'}})">
  Men
  </button>
  <button class="btn typ-secondary" [class]="'btn ' + (selectedCategory.value == 'women' ? '' : 'typ-secondary')" value="women" on="tap:AMP.setState({selectedCategory: {value: 'women'}})">
  Women
  </button>
  </div>
  </td>
  </tr>
  <!-- Change CTA -->
  <tr>
  <td class="wrapper">
  <!-- Title changes dynamically based on selected category -->
  <form id="order" method="POST" action-xhr="https://google.com">
  <h2 class="sec-title" [text]="selectedCategory.value">Men</h2>
  <!-- Men category product list -->
  <div class="category category-men" [hidden]="selectedCategory.value != 'men'">
  <ul class="product-list">
  <li class="product-item">
  <amp-state id="selectedMenProduct1">
  <script type="application/json">
  { "value": "option1" }
  </script>
  </amp-state>
  <!-- Men Product 1 Option 1 -->
  <div class="product-card" [hidden]="selectedMenProduct1.value != 'option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">BOLD RED HOODIE</h3>
  <p class="p-desc">Cozy, vibrant, and perfect for casual everyday wear.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="men-product-1" on="select:AMP.setState({selectedMenProduct1: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #1DBF73" option="option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Men Product 1 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedMenProduct1.value != 'option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">BOLD RED HOODIE 2</h3>
  <p class="p-desc">Cozy, vibrant, and perfect for casual everyday wear.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="men-product-1" on="select:AMP.setState({selectedMenProduct1: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #1DBF73" option="option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  <li class="product-item">
  <amp-state id="selectedMenProduct2">
  <script type="application/json">
  { "value": "men2option1" }
  </script>
  </amp-state>
  <!-- Men Product 2 Option 1 -->
  <div class="product-card" [hidden]="selectedMenProduct2.value != 'men2option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">EVERYDAY WHITE HOODIE</h3>
  <p class="p-desc">Clean, comfortable, and effortlessly versatile for layering or lounging.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="men-product-2" on="select:AMP.setState({selectedMenProduct2: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="men2option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="men2option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Men Product 2 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedMenProduct2.value != 'men2option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">EVERYDAY WHITE HOODIE 2</h3>
  <p class="p-desc">Clean, comfortable, and effortlessly versatile for layering or lounging.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="men-product-2" on="select:AMP.setState({selectedMenProduct2: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="men2option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="men2option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  <li class="product-item">
  <amp-state id="selectedMenProduct3">
  <script type="application/json">
  { "value": "men3option1" }
  </script>
  </amp-state>
  <!-- Men Product 3 Option 1 -->
  <div class="product-card" [hidden]="selectedMenProduct3.value != 'men3option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">ESSENTIAL WHITE SHIRT</h3>
  <p class="p-desc">Crisp and classic — perfect for both work and weekend looks.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="men-product-3" on="select:AMP.setState({selectedMenProduct3: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #8C1F34;" option="men3option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #EBEBEB" option="men3option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Men Product 3 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedMenProduct3.value != 'men3option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">ESSENTIAL WHITE SHIRT 2</h3>
  <p class="p-desc">Crisp and classic — perfect for both work and weekend looks.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="men-product-3" on="select:AMP.setState({selectedMenProduct3: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #8C1F34;" option="men3option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #EBEBEB" option="men3option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  <li class="product-item">
  <amp-state id="selectedMenProduct4">
  <script type="application/json">
  { "value": "men4option1" }
  </script>
  </amp-state>
  <!-- Men Product 4 Option 1 -->
  <div class="product-card" [hidden]="selectedMenProduct4.value != 'men4option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">MIDNIGHT BLACK SHIRT</h3>
  <p class="p-desc">Sharp, sleek, and tailored for elevated everyday dressing.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="men-product-4" on="select:AMP.setState({selectedMenProduct4: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #D4D9DD;" option="men4option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #0A0B0D" option="men4option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Men Product 4 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedMenProduct4.value != 'men4option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/men-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">MIDNIGHT BLACK SHIRT 2</h3>
  <p class="p-desc">Sharp, sleek, and tailored for elevated everyday dressing.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="men-product-4" on="select:AMP.setState({selectedMenProduct4: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #D4D9DD;" option="men4option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #0A0B0D" option="men4option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  </ul>
  </div>
  <!-- Women category product list -->
  <div class="category category-women" hidden [hidden]="selectedCategory.value != 'women'">
  <ul class="product-list">
  <li class="product-item">
  <amp-state id="selectedWomenProduct1">
  <script type="application/json">
  { "value": "women1option1" }
  </script>
  </amp-state>
  <!-- Women Product 1 Option 1 -->
  <div class="product-card" [hidden]="selectedWomenProduct1.value != 'women1option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">COCOA BROWN TEE</h3>
  <p class="p-desc">Soft, earthy, and effortlessly stylish for everyday wear.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="women-product-1" on="select:AMP.setState({selectedWomenProduct1: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women1option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women1option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Women Product 1 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedWomenProduct1.value != 'women1option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">COCOA BROWN TEE 2</h3>
  <p class="p-desc">Soft, earthy, and effortlessly stylish for everyday wear.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="women-product-1" on="select:AMP.setState({selectedWomenProduct1: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women1option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women1option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  <li class="product-item">
  <amp-state id="selectedWomenProduct2">
  <script type="application/json">
  { "value": "women2option1" }
  </script>
  </amp-state>
  <!-- Women Product 2 Option 1 -->
  <div class="product-card" [hidden]="selectedWomenProduct2.value != 'women2option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-2.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">CLASSIC WHITE TEE</h3>
  <p class="p-desc">A wardrobe essential that pairs with just about anything.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="women-product-2" on="select:AMP.setState({selectedWomenProduct2: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women2option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women2option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Women Product 2 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedWomenProduct2.value != 'women2option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">CLASSIC WHITE TEE 2</h3>
  <p class="p-desc">A wardrobe essential that pairs with just about anything.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="women-product-2" on="select:AMP.setState({selectedWomenProduct2: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women2option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women2option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  <li class="product-item">
  <amp-state id="selectedWomenProduct3">
  <script type="application/json">
  { "value": "women3option1" }
  </script>
  </amp-state>
  <!-- Women Product 3 Option 1 -->
  <div class="product-card" [hidden]="selectedWomenProduct3.value != 'women3option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-3.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">SLATE GREY LONG SLEEVE</h3>
  <p class="p-desc">Lightweight layering made easy with this timeless piece.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="women-product-3" on="select:AMP.setState({selectedWomenProduct3: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women3option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women3option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Women Product 3 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedWomenProduct3.value != 'women3option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">SLATE GREY LONG SLEEVE 2</h3>
  <p class="p-desc">Lightweight layering made easy with this timeless piece.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="women-product-3" on="select:AMP.setState({selectedWomenProduct3: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women3option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women3option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  <li class="product-item">
  <amp-state id="selectedWomenProduct4">
  <script type="application/json">
  { "value": "women4option1" }
  </script>
  </amp-state>
  <!-- Women Product 4 Option 1 -->
  <div class="product-card" [hidden]="selectedWomenProduct4.value != 'women4option1'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-4.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">SUNBURST YELLOW LONG SLEEVE</h3>
  <p class="p-desc">Bright, breathable, and perfect for cooler days.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>1500</p>
  <amp-selector layout="container" name="women-product-4" on="select:AMP.setState({selectedWomenProduct4: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women4option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women4option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  <!-- Women Product 4 Option 2 -->
  <div class="product-card" hidden [hidden]="selectedWomenProduct4.value != 'women4option2'">
  <div class="img-wrap">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-1.png" alt="Product Image" width="258" height="174"></amp-img>
  </div>
  <div class="content-wrap">
  <div class="lhs">
  <h3 class="p-title">SUNBURST YELLOW LONG SLEEVE 2</h3>
  <p class="p-desc">Bright, breathable, and perfect for cooler days.</p>
  </div>
  <div class="rhs">
  <p class="p-amt"><span class="rupee">$</span>2500</p>
  <amp-selector layout="container" name="women-product-4" on="select:AMP.setState({selectedWomenProduct4: { value: event.targetOption }})">
  <ul class="color-list">
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #000000;" option="women4option1"></div>
  </li>
  <li class="color-item">
  <div class="color" style="width: 15px; height: 14px; background: #DFDAD4" option="women4option2"></div>
  </li>
  </ul>
  </amp-selector>
  </div>
  </div>
  <a href="https://www.google.co.in/" class="p-link">Shop now</a>
  </div>
  </li>
  </ul>
  </div>
  <div class="btn-wrap">
  <button class="btn ">View All</button>
  </div>
  </form>
  </td>
  </tr>
  <!-- product section end-->
  <!-- footer start-->
  <tr>
  <td style="text-align: center;">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" class="container" style="background: #EFEFEF; padding: 40px 0;">
  <tr>
  <td>
  <table align="center" cellpadding="0" cellspacing="0" width="100%" style="text-align: center; margin-bottom: 30px;">
  <!-- Footer Link-->
  <!-- Social Links -->
  <tr>
  <td style="padding: 7px 39px; border: 1px solid #1DBF73; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/7c0f383a34174b419048c105abef1c6d.png" alt="Social Icon" class="media-logo" width="20" height="20">
  </amp-img>
  </a>
  </td>
  <td style="padding: 7px 39px; border: 1px solid #1DBF73; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9e433bfc71464f51ac6bf991cc15c61e.png" alt="Social Icon" class="media-logo" width="20" height="20"></amp-img>
  </a>
  </td>
  <td style="padding: 7px 39px; border: 1px solid #1DBF73; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/84960566b3bd48c49d86b17263d4cee8.png" alt="Social Icon" class="media-logo" width="20" height="20">
  </amp-img>
  </a>
  </td>
  </tr>
  <!-- Social Links -->
  <!-- Footer Link-->
  </table>
  </td>
  </tr>
  <tr>
  <td>
  <p style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #4F4F4F; text-align: center; max-width: 90%; margin: 0 auto; text-transform: To opt out of promotional emails like this,;">
  For assistance, connect with us on social media or reach out to our support team at support@example.com 
  </p>
  </td>
  </tr>
  </table>
  </td>
  </tr>
  <tr>
  <td>
  <p style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: none; margin: 15px 0; ">
  To opt out of promotional emails like this, <a href="https://www.google.co.in/" style="color: #1DBF73 ; font-weight: 700; text-transform: none; text-decoration: none;">unsubscribe
  here</a>
  </p>
  </td>
  </tr>
  <!-- footer end-->
  </table>
  </body>
  </html>
  ```
</details>

## Show Recommendations

This AMP template introduces users to personalized product suggestions using interactive email content. It can be used for onboarding new subscribers or re-engaging recent visitors by showcasing curated products tailored to their interests. This template typically includes featured products, category filters, and direct Shop Now CTAs, all rendered dynamically within the inbox.

<Image align="center" alt="Sample Show Recommendations With and Without Notify Me CTA Templates" border={true} caption="Sample Show Recommendations With and Without Notify Me CTA Templates" src="https://files.readme.io/a301d644acdc9ddb7700612e3a2276f9401438bec493ecc47c758a47889d5c4a-Show_Recommendations_1__2_AMP.png" width="65% " />

<details>
  <summary><b>Expand to know more about the template.</b></summary>

  ### Use Case Examples

  * Introduce new users to relevant collections based on browsing behavior.
  * Highlight bestsellers or staff picks to increase discovery.
  * Re-engage dormant users with personalized product nudges.
  * Encourage first purchases through category filters and CTAs.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)
  * [Add or Modify Filters](doc:ootb-email-templates#add-or-modify-filters)

  ### Template Code

  ```html Recommendations
  <!doctype html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.1.js"></script>
  <style amp4email-boilerplate>
  body{visibility:hidden}
  </style>
  <style amp-custom>
  *{
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  background: #F5F5F5;
  }
  img{
  object-fit: cover;
  }
  @media only screen and (max-width: 400px) {
  .main {
  max-width: 95% ;
  }
  }
  .logo-wrap{
  padding: 15px 0;
  position: relative;
  }
  .line{
  position: absolute;
  width: 100%; height: 1px;
  background: #F04444;
  top: 50%;
  left: 0;
  transform: translateY(-50%);
  }
  .logo-wrap .logo{
  max-width: 157px;
  max-height: 81px;
  margin: 0 auto;
  background: #FFFFFF;
  z-index: 1;
  padding: 0 30px;
  }
  .logo-wrap img{
  object-fit: contain;
  }
  .play-btn{
  border: 1px solid #F04444;
  background: #F04444;
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-transform: none;
  text-align: center;
  padding: 6px 15px 6px 6px; 
  display: inline-block;
  text-decoration: none;
  border-radius: 50px;
  color: #FFFFFF;
  display: flex;
  align-items: center;
  }
  .play-btn .play-icon{
  width: 31px;
  height: 31px;
  margin-right: 10px;
  }
  .banner{
  margin-bottom: 25px;
  }
  .media-logo{
  width: 25px;
  height: 25px;
  } 
  .section{
  padding-bottom: 60px;
  }
  .sec-title{ position: relative; margin-bottom: 12px; }
  .sec-title .text{
  background: #FFFFFF;
  padding: 0 25px;
  font-size: 24px;
  font-weight: 400;
  line-height: 39px;
  text-align: center;
  color: #000000;
  text-transform: uppercase;
  z-index: 1;
  display: inline-block;
  position: relative;
  }
  .sec-desc{
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  color: #6F6F6F;
  text-align: center; 
  text-transform: none;
  max-width: 85%;
  margin: 0 auto 25px;
  }
  .btn{
  border: 1px solid #F04444;
  background: #FFFFFF;
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-transform: none;
  text-align: center;
  padding: 6px; 
  display: inline-block;
  text-align: center;
  text-decoration: none;
  border-radius: 50px;
  color: #F04444;
  max-width: 113px;
  width: 100%;
  margin: 5px;
  }
  .btn.typ-active{
  background: #F04444;
  color: #FFFFFF;
  }
  .category-btn-wrap{
  margin: 0 0 38px;
  }
  .img-wrap,
  .card{
  position: relative;
  }
  .btn-play{
  position: absolute;
  width: 74px; height: 74px;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  }
  .card .card-body{
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  background: #00000080;
  padding: 18px 0
  }
  .card .card-title{ 
  font-size: 20px;
  font-weight: 400;
  line-height: 25px;
  text-align: left;
  color: #FFFFFF;
  margin: 0 18px 5px;
  text-transform: uppercase;
  }
  .card .card-desc{
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-align: left;
  color: #FFFFFF;
  margin: 0 18px;
  text-transform: none;
  }
  .movie-list{
  list-style: none;
  display: flex;
  justify-content: space-between;
  gap: 20px;
  max-width: 88%;
  margin: 0 auto;
  }
  .movie-list .movie-item{
  width: 48%;
  }
  .weekly-card .weekly-body{
  padding: 7px 0;
  }
  .weekly-card .weekly-title{
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  color: #000000;
  text-align: left;
  text-transform: uppercase;
  }
  .weekly-card .weekly-desc{
  font-size: 10px;
  font-weight: 400;
  line-height: 15px;
  color: #6F6F6F;
  text-align: left;
  text-transform: none;
  }
  .btn-wrap{
  margin-top: 30px;
  }
  @media only screen and (max-width: 400px) {
  .logo-wrap .logo {
  max-width: 130px;
  max-height: 70px;
  }
  .sec-title .text {
  font-size: 20px;
  font-weight: 400;
  padding: 0 10px;
  }
  .sec-desc{
  line-height: 20px;
  }
  .card .card-title {
  font-size: 18px;
  line-height: 20px;
  margin: 0 10px 5px;
  }
  .card .card-desc {
  font-size: 12px;
  line-height: 18px;
  margin: 0 10px;
  }
  }
  </style>
  </head>
  <body>
  <!-- AMP state for handling category selection -->
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" class="main">
  <!-- header start-->
  <tr>
  <td align="center" style="padding: 5px 0;">
  <div class="logo-wrap">
  <div class="line"></div>
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo" width="157" height="81" class="logo" />
  </div>
  </td>
  </tr>
  <!-- header end-->
  <!-- banner start-->
  <tr>
  <td align="center">
  <div class="banner">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/banner.png" width="600" height="280" layout="responsive" alt="a sample image"></amp-img>
  </div>
  </td>
  </tr>
  <!-- banner end-->
  <!-- new episodes start-->
  <tr>
  <td align="center">
  <div class="section">
  <div class="sec-head">
  <div class="sec-title">
  <h2 class="text">CATCH UP WITH YOUR FAVORITES</h2>
  <div class="line"></div>
  </div>
  <p class="sec-desc">The wait is over! New episodes of <i>Black Mirror, Suits, Stranger Things</i>, and more are now streaming.</p>
  <button class="play-btn">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="31" height="31"></amp-img>
  View All
  </button>
  </div>
  </div>
  </td>
  </tr>
  <!-- new episodes end-->
  <!-- product section start-->
  <amp-state id="selectedCategory">
  <script type="application/json">
  { "value": "action" }
  </script>
  </amp-state>
  <tr>
  <td align="center">
  <div class="section">
  <div class="sec-head">
  <div class="sec-title">
  <h2 class="text">NEW EPISODES OUT!</h2>
  <div class="line"></div>
  </div>
  <p class="sec-desc">Catch up on the latest seasons of your favorite shows.</p>
  <div class="category-btn-wrap">
  <button class="btn typ-active" [class]="'btn ' + (selectedCategory.value == 'action' ? 'typ-active' : '')" value="action" on="tap:AMP.setState({selectedCategory: {value: 'action'}})">
  Action
  </button>
  <button class="btn" [class]="'btn ' + (selectedCategory.value == 'horror' ? 'typ-active' : '')" value="horror" on="tap:AMP.setState({selectedCategory: {value: 'horror'}})">
  Horror
  </button>
  <button class="btn" [class]="'btn ' + (selectedCategory.value == 'drama' ? 'typ-active' : '')" value="drama" on="tap:AMP.setState({selectedCategory: {value: 'drama'}})">
  Drama
  </button>
  </div>
  </div>
  <!-- action cards start-->
  <div class="sec-content" [hidden]="selectedCategory.value != 'action'">
  <amp-carousel loop width="600" height="375" layout="responsive" type="slides" role="region" aria-label="action carousel">
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-1.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">THE WITCHER - SEASON 3</h3>
  <p class="card-desc">Geralt’s epic journey continues with battles, betrayals, and dark forces looming.</p>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-2.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">STRANGER THINGS - SEASON 4</h3>
  <p class="card-desc">The gang faces terrifying new threats from the Upside Down.</p>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-3.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">THE CROWN - SEASON 6</h3>
  <p class="card-desc">The royal family’s trials and triumphs unfold in this gripping final chapter.</p>
  </div>
  </div>
  </amp-carousel>
  </div>
  <!-- action cards end-->
  <!-- horror cards start-->
  <div class="sec-content" hidden [hidden]="selectedCategory.value != 'horror'">
  <amp-carousel width="600" loop height="375" layout="responsive" type="slides" role="region" aria-label="horror carousel">
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-1.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">STRANGER THINGS - SEASON 4</h3>
  <p class="card-desc">The gang faces terrifying new threats from the Upside Down.</p>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-2.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">THE WITCHER - SEASON 3</h3>
  <p class="card-desc">Geralt’s epic journey continues with battles, betrayals, and dark forces looming.</p>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-3.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">THE CROWN - SEASON 6</h3>
  <p class="card-desc">The royal family’s trials and triumphs unfold in this gripping final chapter.</p>
  </div>
  </div>
  </amp-carousel>
  </div>
  <!-- horror cards end-->
  <!-- drama cards start-->
  <div class="sec-content" hidden [hidden]="selectedCategory.value != 'drama'">
  <amp-carousel width="600" loop height="375" layout="responsive" type="slides" role="region" aria-label="drama carousel">
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-1.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">THE CROWN - SEASON 6</h3>
  <p class="card-desc">The royal family’s trials and triumphs unfold in this gripping final chapter.</p>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-2.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">STRANGER THINGS - SEASON 4</h3>
  <p class="card-desc">The gang faces terrifying new threats from the Upside Down.</p>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-3.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <h3 class="card-title">THE WITCHER - SEASON 3</h3>
  <p class="card-desc">Geralt’s epic journey continues with battles, betrayals, and dark forces looming.</p>
  </div>
  </div>
  </amp-carousel>
  </div>
  </div>
  <!-- drama cards end-->
  </td>
  </tr>
  <!-- product section end-->
  <tr>
  <td align="center">
  <div class="section">
  <div class="sec-head">
  <div class="sec-title">
  <h2 class="text">MORE SHOWS YOU’LL LIKE</h2>
  <div class="line"></div>
  </div>
  </div>
  <div class="sec-content">
  <ul class="movie-list">
  <li class="movie-item">
  <div class="weekly-card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-1.png" width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
  </div>
  <div class="weekly-body">
  <h3 class="weekly-title">Breaking Bad</h3>
  <p class="weekly-desc">A teacher turns to crime in desperate times.</p>
  </div>
  </div>
  </li>
  <li class="movie-item">
  <div class="weekly-card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-2.png" width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
  </div>
  <div class="weekly-body">
  <h3 class="weekly-title">The Crown</h3>
  <p class="weekly-desc">The life and reign of Queen Elizabeth II.</p>
  </div>
  </div>
  </li>
  </ul>
  <div class="btn-wrap">
  <button class="btn typ-active">
  View All
  </button>
  </div>
  </div>
  </div>
  </td>
  </tr>
  <!-- footer start-->
  <tr>
  <td style="text-align: center;">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" class="container" style="border-top: 2px solid #D33C3C; padding: 30px 0 40px;">
  <tr>
  <td>
  <table align="center" cellpadding="0" cellspacing="0" width="100%" style="text-align: center; margin-bottom: 30px;">
  <tr>
  <td style="padding: 0 16px; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/46e890761aa9484488a1d4b5b7e5e90a.png" alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
  </td>
  <td style="padding: 0 16px; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/1ba99ae8ff9a4646a043bc4572c74c85.png" alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
  </td>
  <td style="padding: 0 16px; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9fd609ff93f44ae98273362f7509d619.png" alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
  </td>
  </tr>
  </table>
  </td>
  </tr>
  <tr>
  <td>
  <p style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #4F4F4F; text-align: center; max-width: 80%; margin: 0 auto; text-transform: none;">For assistance, connect with us on social media or reach out to our support team at support@example.com </p>
  </td>
  </tr>
  </table>
  </td>
  </tr>
  <tr>
  <td style="border-top: 2px solid #D33C3C">
  <p style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: none; margin: 15px 0; ">To opt out of promotional emails like this, <a href="https://www.google.co.in/" style="color: #F04444 ; font-weight: 700; text-transform: none; text-decoration: none;">unsubscribe here</a></p>
  </td>
  </tr>
  <!-- footer end-->
  </table>
  </body>
  </html>
  ```
  ```html Recommendations with Notify Me
  <!doctype html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <script async custom-element="amp-carousel" src="https://cdn.ampproject.org/v0/amp-carousel-0.1.js"></script>
  <style amp4email-boilerplate>
  body{visibility:hidden}
  </style>
  <style amp-custom>
  *{
  margin: 0;
  padding: 0;
  }
  body {
  font-family: "Helvetica", arial, sans-serif;
  font-weight: 400;
  background: #F5F5F5;
  }
  img{
  object-fit: cover;
  }
  @media only screen and (max-width: 400px) {
  .main {
  max-width: 95% ;
  }
  }
  .logo-wrap{
  padding: 15px 0;
  position: relative;
  }
  .line{
  position: absolute;
  width: 100%; height: 1px;
  background: #F04444;
  top: 50%;
  left: 0;
  transform: translateY(-50%);
  }
  .logo-wrap .logo{
  max-width: 157px;
  max-height: 81px;
  margin: 0 auto;
  background: #FFFFFF;
  z-index: 1;
  padding: 0 30px;
  }
  .logo-wrap img{
  object-fit: contain;
  }
  .play-btn{
  border: 1px solid #F04444;
  background: #F04444;
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-transform: none;
  text-align: center;
  padding: 6px 15px 6px 6px; 
  display: inline-block;
  text-decoration: none;
  border-radius: 50px;
  color: #FFFFFF;
  display: flex;
  align-items: center;
  }
  .play-btn .play-icon{
  width: 31px;
  height: 31px;
  margin-right: 10px;
  }
  .banner{
  margin-bottom: 25px;
  }
  .media-logo{
  width: 25px;
  height: 25px;
  } 
  .section{
  padding-bottom: 60px;
  }
  .sec-title{ position: relative; margin-bottom: 12px; }
  .sec-title .text{
  background: #FFFFFF;
  padding: 0 25px;
  font-size: 24px;
  font-weight: 400;
  line-height: 39px;
  text-align: center;
  color: #000000;
  text-transform: uppercase;
  z-index: 1;
  display: inline-block;
  position: relative;
  }
  .sec-desc{
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  color: #6F6F6F;
  text-align: center; 
  text-transform: none;
  max-width: 85%;
  margin: 0 auto 25px;
  }
  .btn{
  border: 1px solid #F04444;
  background: #FFFFFF;
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-transform: none;
  text-align: center;
  padding: 6px; 
  display: inline-block;
  text-align: center;
  text-decoration: none;
  border-radius: 50px;
  color: #F04444;
  max-width: 113px;
  width: 100%;
  margin: 5px;
  }
  .btn.typ-active{
  background: #F04444;
  color: #FFFFFF;
  }
  .category-btn-wrap{
  margin: 0 0 38px;
  }
  .img-wrap,
  .card{
  position: relative;
  }
  .btn-play{
  position: absolute;
  width: 74px; height: 74px;
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
  }
  .btn-play img{
  object-fit: contain;
  }
  .card .card-body{
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  background: #00000080;
  padding: 18px 0;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  }
  .card .card-body .lhs{
  width: 70%;
  }
  .card .card-body .rhs{
  width: 30%;
  position: relative;
  }
  .card .card-title{ 
  font-size: 20px;
  font-weight: 400;
  line-height: 25px;
  text-align: left;
  color: #FFFFFF;
  margin: 0 18px 5px;
  text-transform: uppercase;
  }
  .card .card-desc{
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-align: left;
  color: #FFFFFF;
  margin: 0 18px;
  text-transform: none;
  }
  .movie-list{
  list-style: none;
  display: flex;
  justify-content: space-between;
  gap: 20px;
  max-width: 88%;
  margin: 0 auto;
  }
  .movie-list .movie-item{
  width: 48%;
  }
  .weekly-card .weekly-body{
  padding: 7px 0;
  }
  .weekly-card .weekly-title{
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  color: #000000;
  text-align: left;
  text-transform: uppercase;
  }
  .weekly-card .weekly-desc{
  font-size: 10px;
  font-weight: 400;
  line-height: 15px;
  color: #6F6F6F;
  text-align: left;
  text-transform: none;
  }
  .btn-wrap{
  margin-top: 30px;
  }
  .notify-btn{
  border: 1px solid #F04444;
  background: #F04444;
  font-size: 14px;
  font-weight: 400;
  line-height: 25px;
  text-transform: none;
  text-align: center;
  padding: 6px 12px; 
  text-align: center;
  border-radius: 50px;
  color: #FFFFFF;
  text-transform: uppercase;
  margin: 5px;
  display: flex;
  align-items: center;
  }
  .notify-btn .notify-icon{
  width: 19px;
  height: 21px;
  margin-left: 10px;
  }
  .notify-btn.typ-opacity{
  border: 1px solid #FFB8B8;
  background: #FFB8B8;
  }
  .notify-note{
  position: absolute;
  top: -56px;
  right: 15px;
  background: #FFFFFF;
  border-radius: 10px;
  border-bottom: 2px solid #F04444;
  padding: 5px 10px;
  }
  .notify-note .n-title{
  font-size: 14px;
  font-weight: 500;
  line-height: 29px;
  color: #000000;
  text-align: center;
  text-transform: uppercase;
  }
  .notify-note .n-desc{
  font-size: 12px;
  font-weight: 400;
  line-height: 18px;
  text-align: center;
  color: #606060;
  }
  @media only screen and (max-width: 400px) {
  .logo-wrap .logo {
  max-width: 130px;
  max-height: 70px;
  }
  .sec-title .text {
  font-size: 20px;
  font-weight: 400;
  padding: 0 10px;
  }
  .sec-desc{
  line-height: 20px;
  }
  .card .card-title {
  font-size: 18px;
  line-height: 20px;
  margin: 0 10px 5px;
  }
  .card .card-desc {
  font-size: 12px;
  line-height: 18px;
  margin: 0 10px;
  }
  }
  </style>
  </head>
  <body>
  <!-- AMP state for handling category selection -->
  <amp-state id="selectedCategory">
  <script type="application/json">
  { "value": "action" }
  </script>
  </amp-state>
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF;" class="main">
  <!-- header start-->
  <tr>
  <td align="center" style="padding: 5px 0;">
  <div class="logo-wrap">
  <div class="line"></div>
  <!-- Change image src as per your requirements -->
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo" width="157" height="81" class="logo" />
  </div>
  </td>
  </tr>
  <!-- header end-->
  <!-- banner start-->
  <tr>
  <td align="center">
  <div class="banner">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/banner.png" width="600" height="280" layout="responsive" alt="a sample image"></amp-img>
  </div>
  </td>
  </tr>
  <!-- banner end-->
  <!-- new episodes start-->
  <tr>
  <td align="center">
  <div class="section">
  <div class="sec-head">
  <div class="sec-title">
  <h2 class="text">CATCH UP WITH YOUR FAVORITES</h2>
  <div class="line"></div>
  </div>
  <p class="sec-desc">The wait is over! New episodes of <i>Black Mirror, Suits, Stranger Things</i>, and more are now streaming.</p>
  <button class="play-btn">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="31" height="31"></amp-img>
  View All
  </button>
  </div>
  </div>
  </td>
  </tr>
  <!-- new episodes end-->
  <!-- product section start-->
  <tr>
  <td align="center">
  <div class="section">
  <div class="sec-head">
  <div class="sec-title">
  <h2 class="text">NEW EPISODES OUT!</h2>
  <div class="line"></div>
  </div>
  <p class="sec-desc">Catch up on the latest seasons of your favorite shows.</p>
  <div class="category-btn-wrap">
  <button class="btn typ-active" [class]="'btn ' + (selectedCategory.value == 'action' ? 'btn typ-active' : '')" value="action" on="tap:AMP.setState({selectedCategory: {value: 'action'}})">
  Action
  </button>
  <button class="btn" [class]="'btn ' + (selectedCategory.value == 'horror' ? 'btn typ-active' : '')" value="horror" on="tap:AMP.setState({selectedCategory: {value: 'horror'}})">
  Horror
  </button>
  <button class="btn" [class]="'btn ' + (selectedCategory.value == 'drama' ? 'btn typ-active' : '')" value="drama" on="tap:AMP.setState({selectedCategory: {value: 'drama'}})">
  Drama
  </button>
  </div>
  </div>
  <!-- action cards start-->
  <div class="sec-content" [hidden]="selectedCategory.value != 'action'">
  <amp-carousel width="600" height="375" layout="responsive" type="slides" role="region" aria-label="action carousel">
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-1.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="18" height="21"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">THE WITCHER - SEASON 3</h3>
  <p class="card-desc">Geralt’s epic journey continues with battles, betrayals, and dark forces looming.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" [class]="'notify-btn ' + (showNotify ? 'typ-opacity' : '')" on="tap:AMP.setState({ showNotify: true })">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotify">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-2.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">STRANGER THINGS - SEASON 4</h3>
  <p class="card-desc">The gang faces terrifying new threats from the Upside Down.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotify1: true })" [class]="'notify-btn ' + (showNotify1 ? 'typ-opacity' : '')" on="tap:AMP.setState({ showNotify: true })">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotify1">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/action-3.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">THE CROWN - SEASON 6</h3>
  <p class="card-desc">The royal family’s trials and triumphs unfold in this gripping final chapter.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotify2: true })" [class]="'notify-btn ' + (showNotify2 ? 'typ-opacity' : '')" on="tap:AMP.setState({ showNotify: true })">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotify2">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  </amp-carousel>
  </div>
  <!-- action cards end-->
  <!-- horror cards start-->
  <div class="sec-content" hidden [hidden]="selectedCategory.value != 'horror'">
  <amp-carousel width="600" height="375" layout="responsive" type="slides" role="region" aria-label="horror carousel">
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-1.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">THE WITCHER - SEASON 3</h3>
  <p class="card-desc">Geralt’s epic journey continues with battles, betrayals, and dark forces looming.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotifyHorror1: true })" [class]="'notify-btn ' + (showNotifyHorror1 ? 'typ-opacity' : '')" on="tap:AMP.setState({ showNotifyHorror1: true })">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotifyHorror1">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-2.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">STRANGER THINGS - SEASON 4</h3>
  <p class="card-desc">The gang faces terrifying new threats from the Upside Down.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotifyHorror2: true })" [class]="'notify-btn ' + (showNotifyHorror2 ? 'typ-opacity' : '')">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotifyHorror2">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/horror-3.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">THE CROWN - SEASON 6</h3>
  <p class="card-desc">The royal family’s trials and triumphs unfold in this gripping final chapter.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotifyHorror3: true })" [class]="'notify-btn ' + (showNotifyHorror3 ? 'typ-opacity' : '')">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotifyHorror3">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  </amp-carousel>
  </div>
  <!-- horror cards end-->
  <!-- drama cards start-->
  <div class="sec-content" hidden [hidden]="selectedCategory.value != 'drama'">
  <amp-carousel width="600" height="375" layout="responsive" type="slides" role="region" aria-label="drama carousel">
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-1.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">THE WITCHER - SEASON 3</h3>
  <p class="card-desc">Geralt’s epic journey continues with battles, betrayals, and dark forces looming.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotifyDrama1: true })" [class]="'notify-btn ' + (showNotifyDrama1 ? 'typ-opacity' : '')">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotifyDrama1">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-2.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">STRANGER THINGS - SEASON 4</h3>
  <p class="card-desc">The gang faces terrifying new threats from the Upside Down.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotifyDrama2: true })" [class]="'notify-btn ' + (showNotifyDrama2 ? 'typ-opacity' : '')">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotifyDrama2">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  <div class="card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/drama-3.png" width="600" height="375" layout="responsive" alt="a sample image"></amp-img>
  <div class="btn-play">
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/play-icon.png" alt="Play Icon" class="play-icon" width="74" height="74"></amp-img>
  </div>
  </div>
  <div class="card-body">
  <div class="lhs">
  <h3 class="card-title">THE CROWN - SEASON 6</h3>
  <p class="card-desc">The royal family’s trials and triumphs unfold in this gripping final chapter.</p>
  </div>
  <div class="rhs">
  <button class="notify-btn" on="tap:AMP.setState({ showNotifyDrama3: true })" [class]="'notify-btn ' + (showNotifyDrama3 ? 'typ-opacity' : '')">
  notify me
  <amp-img layout="responsive" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/bell-icon.png" alt="Bell Icon" class="notify-icon" width="18" height="21"></amp-img>
  </button>
  <div class="notify-note" hidden [hidden]="!showNotifyDrama3">
  <h3 class="n-title">Thank you</h3>
  <p class="n-desc">You'll get all notifications</p>
  </div>
  </div>
  </div>
  </div>
  </amp-carousel>
  </div>
  </div>
  <!-- drama cards end-->
  </td>
  </tr>
  <!-- product section end-->
  <tr>
  <td align="center">
  <div class="section">
  <div class="sec-head">
  <div class="sec-title">
  <h2 class="text">MORE SHOWS YOU’LL LIKE</h2>
  <div class="line"></div>
  </div>
  </div>
  <div class="sec-content">
  <ul class="movie-list">
  <li class="movie-item">
  <div class="weekly-card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-1.png" width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
  </div>
  <div class="weekly-body">
  <h3 class="weekly-title">Breaking Bad</h3>
  <p class="weekly-desc">A teacher turns to crime in desperate times.</p>
  </div>
  </div>
  </li>
  <li class="movie-item">
  <div class="weekly-card">
  <div class="img-wrap">
  <amp-img src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/show-recommendations-amp/weekly-2.png" width="245" height="161" layout="responsive" alt="weekly image"></amp-img>
  </div>
  <div class="weekly-body">
  <h3 class="weekly-title">The Crown</h3>
  <p class="weekly-desc">The life and reign of Queen Elizabeth II.</p>
  </div>
  </div>
  </li>
  </ul>
  <div class="btn-wrap">
  <button class="btn typ-active">
  View All
  </button>
  </div>
  </div>
  </div>
  </td>
  </tr>
  <!-- footer start-->
  <tr>
  <td style="text-align: center;">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" class="container" style="border-top: 2px solid #D33C3C; padding: 30px 0 40px;">
  <tr>
  <td>
  <table align="center" cellpadding="0" cellspacing="0" width="100%" style="text-align: center; margin-bottom: 30px;">
  <tr>
  <td style="padding: 0 16px; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/46e890761aa9484488a1d4b5b7e5e90a.png" alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
  </td>
  <td style="padding: 0 16px; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/1ba99ae8ff9a4646a043bc4572c74c85.png" alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
  </td>
  <td style="padding: 0 16px; display: inline-block;">
  <a href="https://www.google.co.in/">
  <amp-img layout="responsive" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/9fd609ff93f44ae98273362f7509d619.png" alt="Social Icon" class="media-logo" width="25" height="25"></amp-img>
  </td>
  </tr>
  </table>
  </td>
  </tr>
  <tr>
  <td>
  <p style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #4F4F4F; text-align: center; max-width: 80%; margin: 0 auto; text-transform: none;">For assistance, connect with us on social media or reach out to our support team at support@example.com </p>
  </td>
  </tr>
  </table>
  </td>
  </tr>
  <tr>
  <td style="border-top: 2px solid #D33C3C">
  <p style="font-family: 'Helvetica', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 22px; text-align: center; color: #909090; text-transform: none; margin: 15px 0; ">To opt out of promotional emails like this, <a href="https://www.google.co.in/" style="color: #F04444 ; font-weight: 700; text-transform: none; text-decoration: none;">unsubscribe here</a></p>
  </td>
  </tr>
  <!-- footer end-->
  </table>
  </body>
  </html>
  ```
</details>

## Deals by Category Template

This AMP template features a clickable tile-based layout where each tile reveals a contextual popup within the email. Originally themed around zodiac signs, this template is fully customizable — tiles can represent categories like product types, service plans, travel destinations, or user personas.

When clicked, each tile displays an offer, message, or interactive form, enabling brands to deliver multiple personalized micro-experiences inside a single email.

<Image align="center" alt="Sample Deals by Category Template" border={true} caption="Sample Deals by Category Template" src="https://files.readme.io/c6b2e49e246d6a8d2fe8da10efbc2ee08a6b4f82823f4c561ab6c5aab588959c-Deals_by_Category_AMP.png" width="30% " />

<details>
  <summary><b>Expand to know more about the template.</b></summary>

  ### Use Case Examples

  * Zodiac-based Offer Engagement: Display tailored offers by the user’s zodiac sign.
  * Product Category Showcases: Let users explore offers based on product types (for example, electronics, apparel, beauty).
  * Festival/Seasonal Gifting: Show different recommendations for occasions (for example, Diwali gifts, Summer picks).
  * User Personas or Interests: Target users with content that aligns with their interests (for example, Fitness, Fashion, Tech).

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
  * [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)

  ### Template Code

  ```html
  <!doctype html>
  <html ⚡4email data-css-strict>
  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script><script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script><script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script><script async custom-element="amp-lightbox" src="https://cdn.ampproject.org/v0/amp-lightbox-0.1.js"></script>
  <style amp4email-boilerplate>body{visibility:hidden}</style>
  <style amp-custom>*{ margin: 0;padding: 0; }body {font-family: "Helvetica", arial, sans-serif;font-weight: 400; }img{width: 100%;height: 100%;object-fit: cover; }.main {width: 100%;max-width: 600px;overflow: hidden;margin: 0 auto;background: #FFFFFF; }.sec-title{font-size: 50px; font-weight: 500; line-height: 50px; text-align: center; color: #FFFFFF; text-transform: uppercase; margin-bottom: 40px;}.sec-desc{max-width: 70%; margin: 0 auto 42px; font-size: 18px; font-weight: 400; line-height: 20px; text-align: center; text-transform: none; color: #FFFFFF;}.z-list{list-style: none;display: flex;justify-content: space-between;flex-wrap: wrap;gap: 10px;margin-bottom: -100px;}.z-item{background: #FFFFFF;box-shadow: 0px 3.57px 3.57px 0px #00000040; width: 32%; }.z-card{background: #FECD2C;box-shadow: 0px 3.57px 3.57px 0px #00000040;margin: 8px;padding: 10px 8px;display: flex;justify-content: center;align-items: center;flex-direction: column;min-height: 222px; }.z-card .z-title{text-transform: none;font-weight: 600;font-size: 26px;line-height: 26px;color: #FFFFFF;margin-bottom: 5px; }.z-card .data{text-transform: none;font-weight: 400;font-size: 14px;line-height: 24px;color: #FFFFFF;text-align: center;margin-bottom: 8px; }.z-card .border{ width: 135px;height: 0.9px;background: #FFFFFF;margin: 0 auto 13px; }.z-card .img-wrap{ width: 73px;height: 73px;margin: 0 auto; }.z-card .animals{ margin-top: 5px;text-transform: none;color: #FFFFFF;font-weight: 400;font-size: 18px;line-height: 24px; }.sec-title {font-size: 35px;line-height: 40px;margin-bottom: 20px;}.sec-desc { max-width: 90%;margin: 0 auto 32px;font-size: 16px; }.container{ padding: 72px 0 40px; background-color: #FE592C; }.lightbox { background: rgba(0,0,0,0.8); width: 100%; height: 100%; position: absolute; display: flex; align-items: center; justify-content: center; }.zodiac-popup{ padding: 10px 10px 20px; max-width: 80%; background: #FFFFFF; position: relative;}.zodiac-popup .img-wrap{overflow: hidden;}.d-title{font-size: 30px;font-weight: 400;line-height: 36px;text-align: center; color: #FE592C; margin:20px 0; text-transform: uppercase;}.d-title .discount{font-size: 45px; line-height: 50px;}.cm-bold{font-weight: 400;}.wrap{position: relative;}.input-wrap{ max-width: 80%; margin: 0 auto;}.input{border: 1px dashed #FE592C; background-color: #F5F5F5; padding: 8px 20px; border-radius: 31px; font-size: 28px; font-weight: 500; line-height: 30px; text-align: left; width: 87%; margin-bottom: 28px; text-transform: uppercase;}.icon-cta{border: 0; position: absolute; background: transparent; top: 17px; right: 15px;}.redeem-cta{background: #FE592C; border: 1px solid #FE592C; font-size: 30px;font-weight: 400;line-height: 43px;text-align: center; color: #FFFFFF; vertical-align: middle; width: 100%; padding: 8px 0; border-radius: 21px; display: inline-block; text-decoration: none;}@media only screen and (max-width: 480px) {body .main {max-width: 100%;}.logo-wrap{ padding: 17px 0; }.logo-wrap .img-wrap { max-width: 130px; max-height: 60px; margin: 0 auto;}.footer{ padding-top: 100px; }.z-item{ background: #FFFFFF; box-shadow: 0px 3.57px 3.57px 0px #00000040;width: 48%; }.container{ padding: 50px 0 40px; }.z-card .z-title { font-size: 20px; line-height: 22px; }.z-card .border{ width: 94px; }.z-card .img-wrap { width: 55px; height: 56px; }.z-card .animals { font-size: 16px; line-height: 20px; }.z-card{ min-height: 180px; }.border-line{ width: 20%; }.zodiac-popup{ max-width: 80%;}.d-title {font-size: 25px;line-height: 30px;margin-bottom: 20px;margin-top: 10px;}.d-title .discount {font-size: 30px;line-height: 40px;}.input{padding: 12px; font-size: 20px; line-height: 26px; margin-bottom: 20px;}.redeem-cta{ font-size: 20px; line-height: 30px; padding: 5px; border-radius: 10px;}}</style>
  </head>
  <body>
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 0 auto; background-color: #FFFFFF; position: relative;" class="main">
  <tbody>
  <!-- header start-->
  <tr>
  <td style="text-align: center; vertical-align: middle; padding: 20px">
  <!-- Change image src as per your requirements -->
  <amp-img width="127" height="58" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" class="logo" alt="Logo" style="display: inline-block; object-fit: cover;"/>
  </td>
  </tr>
  <!-- header end-->
  <tr>
  <td class="container">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center" style=" width:95%; margin: 0 auto;">
  <tbody>
  <tr>
  <td>
  <h2 class="sec-title">UNLOCK EXCLUSIVE DISCOUNTS!</h2>
  <p class="sec-desc">Tap on your favorite category to get a special offer</p>
  </td>
  </tr>
  <tr>
  <td>
  <form id="formZodio" class="result-wrap" method="post" action-xhr="https://www.google.com/">
  <input type="hidden" name="selectedZodiac" [value]="selectedZodiac" />
  <ul class="z-list">
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Travel' }), zodiac-1.open" role="button" tabindex="0">
  <h2 class="z-title">Travel</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/c695878c6be84b1b80215a3eff3b15cb.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Beauty' }), zodiac-2.open" role="button" tabindex="0">
  <h2 class="z-title">Beauty</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/72e31d7f68df49b28a66e45f7743e37c.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Fitness' }), zodiac-3.open" role="button" tabindex="0">
  <h2 class="z-title">Fitness</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/5b2d22a2fa2045988669b46b86350b8a.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Tech' }), zodiac-4.open" role="button" tabindex="0">
  <h2 class="z-title">Tech</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/5d6ec0a9c46e4c7595476d0335cd8946.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Home' }), zodiac-5.open" role="button" tabindex="0">
  <h2 class="z-title">Home</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/c361baadbcd24333a9d383dd8d4ed7bd.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Books' }), zodiac-6.open" role="button" tabindex="0">
  <h2 class="z-title">Books</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/aa150b1c5c854ae5b87497d0f12de9e2.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Footwear' }), zodiac-7.open" role="button" tabindex="0">
  <h2 class="z-title">Footwear</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/c1fb54105f424a209db4694cbe83d73e.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Wellness' }), zodiac-8.open" role="button" tabindex="0">
  <h2 class="z-title">Wellness</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/0d35e194fbf147a488be2d4683adf4d3.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Jewellery' }), zodiac-9.open" role="button" tabindex="0">
  <h2 class="z-title">Jewellery</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/82178fa2431646ea8b3d35171d1ea306.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Fashion' }), zodiac-10.open" role="button" tabindex="0">
  <h2 class="z-title">Fashion</h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/c8f4b02e1f834d9fb938bb793b4ecdc9.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Outdoors' }), zodiac-11.open" role="button" tabindex="0">
  <h2 class="z-title">Outdoors </h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/f7f1ceb7fe1c421785196b47257560d4.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  <li class="z-item">
  <div class="z-card" on="tap:AMP.setState({ selectedZodiac: 'Work' }), zodiac-12.open" role="button" tabindex="0">
  <h2 class="z-title"> Work </h2>
  <p class="data">Save up to 80%</p>
  <div class="border"></div>
  <div class="img-wrap">
  <amp-img layout="responsive" width="73" height="73" src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/2720e979ebc54532bbfe41ef7f796110.png" alt="zodiac" class="z-img" />
  </div>
  <p class="animals">Click to get deal</p>
  </div>
  </li>
  </ul>
  </form>
  </td>
  </tr>
  </tbody>
  </table>
  </td>
  </tr>
  <amp-lightbox id="zodiac-1" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-1.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -10px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">10% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-2" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-2.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">20% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-3" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-3.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">30% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-4" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-4.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">40% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-5" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-5.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">50% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-6" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-6.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">60% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-7" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-7.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">70% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-8" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-8.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">80% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-9" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-9.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">90% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-10" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-10.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">10% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-11" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-11.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">11% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <amp-lightbox id="zodiac-12" layout="nodisplay">
  <div class="lightbox">
  <div class="zodiac-popup">
  <button on="tap:zodiac-12.close" role="button" tabindex="0" style=" width: 40px;height: 40px;outline: 0;border: 0;position: absolute;top: -20px;right: -10px; background: transparent; z-index: 2;">
  <amp-img layout="fixed" width="30" height="30" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/close-icon.png" alt="close-img" />
  </button>
  <div class="img-wrap">
  <amp-img layout="responsive" width="500" height="300" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/pop-img.png" alt="pop-img" />
  </div>
  <div class="zodiac-popup-content">
  <h4 class="d-title">get <br/><span class="discount">12% <span class="bold">Off</span></span><br/> On your purchase</h4>
  <div class="input-wrap">
  <div class="wrap">
  <input class="input" disabled value="#@556t66y6">
  <button class="icon-cta">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/copy-icon.png" alt="copy-icon" />
  </button>
  </div>
  <a href="https://google.com" class="redeem-cta" >Redeem now</a>
  </div>
  </div>
  </div>
  </div>
  </amp-lightbox>
  <!-- footer start-->
  <tr>
  <td colspan="2" align="center" class="footer" style="padding: 60px 0 10px;">
  <table role="presentation" cellspacing="0" cellpadding="0" border="0" align="center" style="width:100%;">
  <tbody>
  <tr>
  <td style="padding: 30px 0;">
  <p style="font-size: 14px; font-weight: 400; line-height: 25px; text-align: center; color: #6F6F6F; text-transform: none; max-width: 90%; margin: 0 auto;">For assistance, connect with us on social media or reach out to our support team at support@example.com </p>
  </td>
  </tr>
  <tr>
  <td style="padding-bottom: 30px 0;">
  <table align="center" cellpadding="0" cellspacing="0" width="100%" style="text-align: center;">
  <tbody>
  <tr>
  <td style="width:32%;" class="border-line">
  <div style="display: block; border:0.5px solid #FE592C;"></div>
  </td>
  <td style="padding: 10px 10px; display: inline-block;">
  <a href="https://google.com" style="vertical-align: middle;display: inline-block; width: 25px; height: 25px; ">
  <!-- Change image src as per your requirements -->
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/logo-insta.png" alt="instagram" />
  </a>
  </td>
  <td style="padding: 10px 10px; display: inline-block; ">
  <a href="https://google.com" style="vertical-align: middle;display: inline-block; width: 25px; height: 25px;">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/logo-facebook.png" alt="facebook" />
  </a>
  </td>
  <td style="padding: 10px 10px; display: inline-block;">
  <a href="https://google.com" style="vertical-align: middle;display: inline-block; width: 25px; height: 25px;">
  <amp-img layout="fixed" width="20" height="20" src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/Zodiac/logo-x.png" alt="x" />
  </a>
  </td>
  <td style="width:32%;" class="border-line">
  <div style="display: block; border:0.5px solid #FE592C;"></div>
  </td>
  </tr>
  </tbody>
  </table>
  </td>
  </tr>
  </tbody>
  </table>
  </td>
  </tr>
  <tr>
  <td style="padding: 20px 0;">
  <p style="font-size: 14px; font-weight: 400; line-height: 24px; text-align: center; color: #6F6F6F;">To opt out of promotional emails like this, <a href="https://google.com" style="color:#FE592C;font-weight:bold;text-decoration:none;">unsubscribe here</a></p>
  </td>
  </tr>
  <!-- footer end-->
  </tbody>
  </table>
  </body>
  </html>
  ```
</details>

## Click To Reveal

This AMP template allows users to engage with an email by clicking on an image to reveal a surprise offer or discount. This interactive format helps create a fun, suspense-driven experience that encourages action and drives higher conversion rates.

<Image align="center" alt="Sample Click to Reveal Template" border={true} caption="Sample Click to Reveal Template" src="https://files.readme.io/cb7e08c2ae7ea1224cf0ace234ed910ccaf65c29f80b935d20690747480e28d6-Click_to_Reveal_AMP.png" width="35% " />

<details>
  <summary><b>Expand to know more about the template.</b></summary>

  ### Use Case Examples

  * Unlock hidden discounts in flash sales or festival campaigns.
  * Gamify email experiences with “scratch-to-reveal” like formats.
  * Increase engagement during limited-time promotions.
  * Run surprise loyalty rewards or exclusive unlockable content.

  ### Template Customization Options

  * [Replace Logo](doc:ootb-email-templates#replace-logo)
  * [Replace Background](doc:ootb-email-templates#replace-background)
  * [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
  * [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
  * [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)

  ### Template Code

  ```html
  <!DOCTYPE html>
  <html ⚡4email data-css-strict>

  <head>
  <meta charset="utf-8">
  <script async src="https://cdn.ampproject.org/v0.js"></script>
  <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>
  <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>
  <style amp4email-boilerplate>
  body {
  visibility: hidden
  }
  </style>
  <style amp-custom>
  * {
  margin: 0;
  padding: 0;
  }

  body {
  font-family: arial, sans-serif;
  font-weight: 400;
  background-color: #f5f5f5;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  }

  img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }

  .main {
  width: 100%;
  max-width: 600px;
  overflow: hidden;
  margin: 0 auto;
  background: #527B66;
  border-bottom: 8px solid #FFFFFF;
  }

  @media only screen and (max-width: 400px) {
  .main {
  max-width: 100%;
  }
  }

  .logo-wrap {
  padding: 12px 24px;
  background-color: #FFFFFF;
  border-radius: 0 0 41px 41px;
  text-align: center;
  z-index: 2;
  position: relative;
  }

  .logo-wrap .img-wrap {
  max-width: 145.78px;
  max-height: 74.89px;
  margin: 0 auto;
  }

  .container {
  width: 90%;
  margin: 53px auto 18px;
  border-top: 2px solid #93784A;
  border-bottom: 2px solid #93784A;
  }

  .wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 48px 0 40px;
  }

  .title {
  font-family: arial, sans-serif;
  font-size: 32px;
  font-weight: 500;
  line-height: 52px;
  color: #FFFFFF;
  text-transform: none;
  margin-bottom: 5px;
  text-align: center;
  }

  .cm-light {
  font-weight: 300;
  }

  .desc {
  font-family: arial, sans-serif;
  font-size: 14px;
  font-weight: 400;
  line-height: 20px;
  color: #CECBD1;
  text-align: center;
  text-transform: none;
  }

  .card {
  width: 65%;
  margin: 40px auto;
  height: 381px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #FFFFFF;
  border-radius: 50%;
  padding: 0 25px;
  }

  .c-title {
  font-family: arial, sans-serif;
  font-size: 30px;
  font-weight: 400;
  line-height: 32px;
  text-align: center;
  margin-bottom: 20px;
  color: #000000;
  text-transform: none;
  }

  .c-desc {
  font-family: arial, sans-serif;
  font-size: 10px;
  font-weight: 400;
  line-height: 16px;
  text-align: center;
  text-transform: none;
  color: #525252;
  margin-bottom: 20px;
  }

  .c-cta {
  font-family: arial, sans-serif;
  font-size: 16px;
  font-weight: 500;
  line-height: 20px;
  text-align: center;
  color: #FFFFFF;
  border-radius: 100px;
  background: #527B66;
  outline: none;
  border: 0;
  padding: 11px;
  max-width: 176px;
  display: inline-block;
  width: 100%;
  text-transform: none;
  cursor: pointer;
  }

  .card-img-wrap {
  padding: 18px;
  width: 65%;
  max-height: 350px;
  background-color: #FFFFFF;
  margin: 40px auto;
  }

  .card-img-wrap .image {
  width: 100%;
  height: 100%;
  }

  .cta {
  font-family: arial, sans-serif;
  font-size: 16px;
  font-weight: 500;
  line-height: 20px;
  text-align: center;
  color: #527B66;
  border-radius: 100px;
  background: #FFFFFF;
  outline: none;
  border: 0;
  padding: 11px;
  max-width: 350px;
  display: inline-block;
  width: 100%;
  text-transform: none;
  cursor: pointer;
  }

  .wave-wrap {
  display: flex;
  align-items: center;
  margin: 40px 0;
  }

  @media only screen and (max-width: 480px) {
  .title {
  font-size: 25px;
  line-height: 35px;
  }

  .card {
  width: 75%;
  height: 300px;
  }

  .c-title {
  font-size: 20px;
  line-height: 25px;
  margin-bottom: 10px;
  }

  .c-cta {
  font-size: 14px;
  line-height: 18px;
  padding: 10px;
  max-width: 150px;
  }

  .wave-wrap {
  margin: 140px 0;
  }

  .wave-wrap .wave {
  width: 10px;
  height: 60px;
  }

  .card-img-wrap {
  padding: 10px;
  width: 85%;
  }
  }
  </style>
  </head>

  <body>
  <amp-state id="step">
  <script type="application/json">
  {
  "step": 1
  }
  </script>
  </amp-state>
  <div class="main">
  <header>
  <div class="logo-wrap">
  <div class="img-wrap">
  <amp-img layout="responsive"
  src="https://d3eqyohhnb5anr.cloudfront.net/1722578176/assets/d4a286654d114089ac42fa2fa815ac3e.png" alt="Logo"
  width="159" height="73"></amp-img>
  </div>
  </div>
  </header>
  <div class="container">
  <!-- Step 1 -->
  <form custom-validation-reporting="show-all-on-submit"
  on="submit:AMP.setState({form6850m49:{formHistory: form6850m49.formHistory.splice(form6850m49.formHistory.length,0,form6850m49.currentStep)}})"
  action-xhr="https://t.mmtrkr.com/submissions/8598e13a-92af-5ed4-a239-989e988e1a88/93a0f936-f5fd-4d94-8bf1-43d8e6571405?sender=hello@amp.mailmodo.net&formId=123"
  method="post">
  <div class="wrapper step-1" [hidden]="step != 1">
  <h2 class="title">UNLOCK AN EXCLUSIVE DISCOUNT</h2>
  <p class="desc">Tap below to reveal your surprise offer!</p>
  <div class="card">
  <h3 class="c-title">Tap to reveal discount</h3>
  <p class="c-desc">A special deal is waiting for you. Don’t miss out!</p>
  <button type="submit" class="c-cta" on="tap:AMP.setState({ step: 2 })">
  Tap here
  </button>
  </div>
  </div>
  <div [hidden]="(('success') != 'success' || (form6850m49.currentStep == 'step3' && 'success' != 'success'))">
  <div submitting>
  <!-- Add Loading Image Here -->
  <div class="wrapper step-2">
  <div class="wave-wrap">
  <amp-img width="245" height="300"
  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/image-on-click/ezgif-3-b33d1ab799.gif"
  alt="wave animation">
  </amp-img>
  </div>
  </div>
  <!-- Add Loading Image Here -->
  </div>
  <div submit-success>
  <div class="wrapper step-3">
  <h2 class="title"><span class="cm-light">Congratulations you get</span> 30% off</h2>
  <div class="card-img-wrap">
  <amp-img layout="responsive"
  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/image-on-click/pexels-karolina-grabowska-4202325%203.png"
  alt="Banner" width="320" height="320" class="image"></amp-img>
  </div>
  <button type="button" class="cta">
  Shop now
  </button>
  </div>
  </div>
  <div submit-error>
  <div class="wrapper step-3">
  <h2 class="title"><span class="cm-light">Congratulations you get</span> 30% off</h2>
  <div class="card-img-wrap">
  <amp-img layout="responsive"
  src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/image-on-click/pexels-karolina-grabowska-4202325%203.png"
  alt="Banner" width="320" height="320" class="image"></amp-img>
  </div>
  <button type="button" class="cta">
  Shop now
  </button>
  </div>
  </div>
  </div>
  </form>
  </div>
  </div>
  </body>

  </html>
  ```
</details>

# Key Template Customization Options

While the entire template is customizable, CleverTap highlights a set of key components you can easily tailor to match your brand and campaign needs. These include logos, banners, CTAs, and theme colors. This section outlines how to modify these core elements, along with reusable code snippets and step-by-step guidance to ensure consistency and ease across your email campaigns. The following are the ey key customization options:

* [Replace Logo](doc:ootb-email-templates#replace-logo)
* [Replace Background](doc:ootb-email-templates#replace-background)
* [Update Banner/Product Images](doc:ootb-email-templates#update-bannerproduct-images)
* [Update Call-To-Actions (CTAs)](doc:ootb-email-templates#update-call-to-actions-ctas)
* [Update Links in Header/Footer](doc:ootb-email-templates#update-links-in-headerfooter)
* [Change Theme or Background Color](doc:ootb-email-templates#change-theme-or-background-color)
* [Update Privacy Policy](doc:ootb-email-templates#update-privacy-policy)
* [Update Social Media and Download Links](doc:ootb-email-templates#update-social-media-links-and-download-links)
* [Countdown Timer (Flash Sale Only)](doc:ootb-email-templates#countdown-timer-flash-sale-only)
* [Add or Modify Filters](doc:ootb-email-templates#add-or-modify-filters)

## Replace Logo

Displays the brand logo at the top of the email, ensuring immediate brand recognition and consistent visual identity.

### Option 1: Using Source Mode

1. Locate the logo block in your HTML template. The following is a common example:
   ```html
   <td style="text-align: left; vertical-align: middle; padding: 20px">
     <img 
       alt="Logo"
       class="logo"
       src="https://yourdomain.com/logo.png"
       style="display: inline-block; width: 127px; height: 58px; object-fit: cover;" />
   </td>
   ```

2. Replace the `src` value with the URL of your updated brand logo as follows:
   ```html
   src="https://yourdomain.com/path-to-your-logo.png"
   ```

3. Optionally customize:
   * `alt`: Add accessible text such as `"Your Brand Logo"`
   * `width` and `height`: Adjust only if required (default is typically `127px × 58px`)

### Option 2: Using Visual Mode

1. Select the required template in the CleverTap **Email Editor** (for example, under _Create Email > Single Message_).

2. Locate and click the existing logo image in the top section of the email.

3. Choose one of the following image replacement methods:

   * **Upload** a new image file (recommended: PNG or SVG).
   * **Paste the URL where image is hosted** in the **Image URL** field (if available).

   <Image align="center" alt="Replace Logo" border={true} caption="Replace Logo" src="https://files.readme.io/ee0f3f1e5b1c453e7e6c07b3a33d9a07aa9bb10d757c40d4ffca334a0ee12c86-Replace_Logo.png" width="75% " />

4. Click Insert to add the image.

5. Adjust the image size and alignment using the **styling and formatting options**—such as margins, width, and spacing.

6. Click **Add**  and click **Done** in the top-right corner of the editor and preview the email to ensure proper rendering.

> 📘 Note
>
> Ensure to verify logo alignment, spacing, and sizing on both mobile and desktop previews after replacement.

## Replace Background

Sets or replaces the existing background with a custom image of your choice.

### Using Source Mode

1. Locate the `.header-container` property in the HTML code.
   ```css
   .header-container {
     background: transparent url(https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/spinn/header-design.png);
     background-size: contain;
     background-repeat: repeat-x;
     background-position: bottom;
     padding-bottom: 18px;
   }
   ```
2. Replace the `background` URL with the link to the new image, in this case, `header-design.png`.

## Update Banner/Product Images

Visually highlights products, offers, or campaigns at the top of the email using a full-width banner image or a product tile grid, depending on the template layout.

### Option 1: Using Source Mode

1. Locate the banner `<img>` tag in your HTML template. For example:
   ```html
   <tr>
     <td align="center">
       <img src="https://yourdomain.com/banner.jpg"
            alt="Promotional Banner"
            style="width: 100%; height: auto;" />
     </td>
   </tr>
   ```

2. Replace the `src` URL with the path to your new banner image.

3. Update the `alt` attribute to provide descriptive alternative text for accessibility and fallback scenarios.

4. Ensure the image meets the following specifications:
   * **Recommended size**: 600px (width) × 400px (height)
   * **Aspect ratio**: 3:2
   * **File formats**: `.jpg`, `.png`, `.gif`
   * **Maximum file size**: Under 1MB

### Option 2: Using Visual Mode

1. Select the required template in the CleverTap **Email Editor**.
2. Click on the existing banner image.
3. Choose one of the following image replacement methods:

   * **Upload** a new image file (recommended: PNG or SVG).
   * **Paste the URL where image is hosted** in the **Image URL** field (if available).

   <Image align="center" alt="Update Banner/Product Images.png" border={true} caption="Update Banner/Product Images.png" src="https://files.readme.io/caddfba6fc321ec0d81c6b9028c1c9ad40c7b24616e8409ac25f18b079f6c024-Update_BannerProduct_Images.png" width="75% " />
4. Click Insert to add the image.
5. Adjust the image size and alignment using the **styling and formatting options**—such as margins, width, and spacing.
6. Click **Add**  and click **Done** in the top-right corner of the editor and preview the email to ensure proper rendering.

> 📘 Note
>
> For templates using grid-based layouts or product tiles, ensure to match the original image dimensions and maintain consistent spacing to ensure the layout remains visually balanced and responsive.

## Update Call-To-Actions (CTAs)

Guides the user to take specific actions within the email, such as clicking a button to redirect the user to a web page, completing a purchase, or viewing more details. You can customize the following elements:

* **Text**: Modify the text within the anchor tag (e.g., "Discover More" → "Shop Now").
* **URL**: Update the `href` attribute with the desired link (e.g., `href="https://your-domain.com"`)
* **Styling**: Adjust the CSS properties to fit your design specifications (for example, background color, padding, text size).

### Option 1: Using Source Mode

1. Locate the CTA section in your HTML template as shown below:
   ```html
   <tr>
     <td style="text-align: center; padding: 20px;">
       <a href="https://your-link.com"
          style="background: #FF5733; padding: 10px 20px; color: #fff; text-decoration: none; font-size: 16px; border-radius: 5px;">
         Shop Now
       </a>
     </td>
   </tr>
   ```

2. Replace the `href` URL with the link where you want to direct the user:
   ```html
   href="https://yourdomain.com/your-action"
   ```

3. Optionally, modify the text of the CTA, such as changing "Shop Now" to "Get Started" or "Claim Your Offer."

4. Adjust the button styling by modifying the CSS within the `<a>` tag (for example, background color, padding, font size, etc.):
   ```html
   style="background: #FF5733; padding: 10px 20px; color: #fff; text-decoration: none; font-size: 16px; border-radius: 5px;"
   ```

### Option 2: Using Visual Mode

1. Open the template in the CleverTap **Email Editor**.
2. Click on the existing CTA button in the email layout.
3. Update the **Display Text** to match your new call to action (for example, _Learn More_, _Shop Now_, and so on).

   <Image align="center" alt="Update CTAs" border={true} caption="Update CTAs" src="https://files.readme.io/6f302e2b6f77f9058405ce8b2b1d8a08ab13bbffed52b3ce250ca2a919d9c9a9-Update_Call-to-Action.png" width="85% " />
4. Enter or update the **Link URL** to point to your desired destination.
5. Click **Add**, then click **Done** in the top-right corner.
6. Preview the email to confirm that the CTA appears and functions correctly across devices.

> 📘 Best Practices
>
> Always make sure the CTAs are clear and actionable, and consider using verbs such as "Buy," "Get Started," "Learn More," or "Shop Now."

## Update Links in Header/Footer

Updates the links in the header or footer sections of the email, such as Privacy Policy, Terms of Service, or any social media or download links, to ensure they direct to the correct URLs.

### Option 1: Using Source Mode

1. **Locate the Header/Footer Section**: Search for the relevant section in your HTML code. The following is a sample code:
   ```html
   <td class="footer" style="text-align: center; padding: 10px; font-size: 12px;">
     <a href="https://your-domain.com/privacy-policy" style="color: #939393; text-decoration: none;">Privacy Policy</a>
   </td>
   ```

2. **Update Link**: Replace the `href` URL with the new destination:
   ```html
   href="https://your-domain.com/new-link"
   ```

3. **Update the Text**: If required, update the link's visible text. For example:
   ```html
   <a href="https://your-domain.com/privacy-policy" style="color: #939393; text-decoration: none;">Terms & Conditions</a>
   ```

4. **Styling Adjustments**: You can adjust the text styles by modifying the `style` attribute (for example, font color, size, and so on).

5. **Save and Preview**: After making changes, ensure to save the file and preview the email to confirm that the links are functional and styled properly.

### Option 2: Using Visual Mode

1. Select the template from the CleverTap dashboard that fits your business requirement.
2. Click the link you want to update in the header or footer section (for example, Unsubscribe link).
3. Update the **Display Text** to reflect your desired action or label.
4. Enter or update the **Link URL** to point to the correct destination.

   <Image align="center" alt="Update Links in Header/Footer" border={true} caption="Update Links in Header/Footer" src="https://files.readme.io/61f5096178dc9c464e937ded9a7a1b9ca0f2f71a7fa2435ae263bf1510b0505b-Update_Links_in_HeaderFooter.png" width="75% " />
5. Click **Apply**, then click **Done** in the top-right corner.
6. Preview the email to confirm that the link appears and functions correctly across devices.

> 📘 Header/Footer Links
>
> * **Unsubscribe Link**: For compliance with regulations such as GDPR and CAN-SPAM, all templates that include an **Unsubscribe** link in the footer must ensure it directs to the correct unsubscribe mechanism.
> * **Social Media Links**: Ensure all social media links, like those for Facebook, Instagram, etc., are up-to-date and lead to your current active profiles.
> * **Dynamic Links**: Some templates, like **Referral** or **Cart Abandonment**, require dynamic links that change based on user activity. Make sure these URLs are generated dynamically by your platform or manually updated.
> * **Call-to-Actions (CTAs)**: Some templates, especially those with **sales**, **product promotions**, or **loyalty rewards**, might have CTAs that need to be consistently checked and updated based on current offers or time-sensitive promotions.

## Change Theme or Background Color

Modifies the background color or overall theme of the email to match your branding or campaign requirements. This ensures a consistent visual experience aligned with your marketing or seasonal themes.

### Using Source Mode

1. Locate the `<table>` tag defining the background color in your HTML code. A typical structure might look like this:
   ```html
   <table style="border-collapse: collapse; width: 100%; max-width: 600px; margin: 0 auto; background: #ffffff;" width="100%" cellspacing="0" cellpadding="0" border="0">
   ```

2. **Update the Background Color**:  
   Replace the existing `background` attribute value with your desired color. For example:
   ```html
   background: #f0f0f0;
   ```

3. **Save and Preview**: After making the changes, save the file and preview the email to ensure the new background color appears correctly across different devices.

## Update Privacy Policy

Ensures that the Privacy Policy link in the email template directs users to the most current and correct Privacy Policy page.

### Option 1: Using Source Mode

1. **Locate the Privacy Policy Link**:  
   Search for the `<a>` tag associated with the Privacy Policy in the footer or header section of your template. The following is a sample code:
   ```html
   <a href="#" class="f-nav-link" style="font-family: 'Poppins', Arial, sans-serif; font-size: 14px; font-weight: 400; line-height: 24px; color: #939393 !important; text-decoration: none;">Privacy Policy</a>
   ```

2. **Update the`href` URL**:  
   Replace the current `href="#"` with the correct URL for your Privacy Policy page. For example:
   ```html
   href="https://yourdomain.com/privacy-policy"
   ```

3. **Modify Text (Optional)**: You can optionally change the visible text of the link, such as replacing "Privacy Policy" with "Terms & Conditions" if required.

4. **Save and Preview**: After making the changes, save your template and preview it to ensure the Privacy Policy link is working correctly and properly displayed.

### Option 2: Using Visual Mode

1. Open the template in the CleverTap **Email Editor**.
2. Locate the **Privacy Policy link** in the footer (or header) section of the email.
3. Click the link to open the editing toolbar.
4. Update the **Link URL** to point to the correct Privacy Policy page.
5. Optionally, update the **Display Text** if needed (for example, change "Privacy Policy" to "Terms & Conditions").

   <Image align="center" alt="Update Privacy Policy" border={true} caption="Update Privacy Policy" src="https://files.readme.io/67f084852c6c76f39130ecea74d93a260c0b57d3d2d351614f8d5fe46352993c-Update_Privacy_Policy.png" width="75% " />
6. Click **Add**, then click **Done** in the top-right corner of the editor.
7. Preview the email to confirm the link is functional and renders correctly across devices.

## Update Social Media and Download Links

Updates and ensures all social media and download links in your email template direct users to the correct platforms, apps, or resources.

### Option 1: Using Source Mode

1. **Locate the Social Media and Download Sections**:  
   Search for sections in the HTML code related to social media platforms (such as Facebook, Twitter, Instagram, etc.) and download buttons (such as Android or Apple store download links). You may see something like:
   ```html
   <a href="https://your-facebook-link" target="_blank">
     <img src="https://path-to-facebook-icon.png" alt="Facebook" class="social-icon" />
   </a>
   ```

2. **Update the Links**:

   For social media platforms, replace the `href` with the correct URL. For example:

   ```html
   <a href="https://facebook.com/your-page" target="_blank">
     <img src="https://path-to-facebook-icon.png" alt="Facebook" class="social-icon" />
   </a>
   ```

   Similarly, for download links, locate the button or link related to the app download:

   ```html
   <a href="#" class="btn-link" style="margin: 0 10px;">
     <img src="apple-btn.png" alt="Download on Apple" class="btn-img" style="background: #F7F7F7; position: relative; z-index: 1;">
   </a>
   ```

   Update the `href` attribute with the correct download link:

   ```html
   <a href="https://www.apple.com/app-store" class="btn-link" style="margin: 0 10px;">
     <img src="apple-btn.png" alt="Download on Apple" class="btn-img" style="background: #F7F7F7; position: relative; z-index: 1;">
   </a>
   ```

3. **Save and Preview**:  
   After updating the URLs for social media and download links, save the file and preview the email to ensure all links work properly.

### Option 2: Using Visual Mode

1. Select the template from the CleverTap dashboard that fits your business requirement.
2. In the footer section, click on a social media icon (such as Facebook, Instagram, or Twitter).
3. Click the link you want to update and update the **Link URL** to point to your brand’s corresponding social media page.
4. Repeat the process for each social media icon you want to update.

   <Image align="center" alt="Update Social Media and Download Links" border={true} caption="Update Social Media and Download Links" src="https://files.readme.io/cbc9edf2828c12258b0c5a1da1ad2e0cf8ffbe4061b831de106ff9010c3d48cd-Update_Social_Media_and_Download_Links.png" width="75% " />
5. Locate and click on the download link (for example, Android or iOS button) in the footer.
6. Update the **Link URL** to the correct app store page (for example, Google Play Store or Apple App Store).
7. Click **Add** and click **Done** in the top-right corner of the dashboard.
8. **Preview the email** to ensure all links are functional and direct users to the right destinations.

## Countdown Timer (Flash Sale Only)

Adds urgency with a live or static countdown. Use a hosted GIF or PNG and replace the image attribute `src` with the required graphics.

```html
<img src="timer.gif" alt="Countdown Timer" style="width: 100%;" />
```

## Add or Modify Filters

1. Add CTA for the Filter, for example, Kids
   ```html
   <button class="btn typ-secondary"
   [class]="'btn ' + (selectedCategory.value == 'kids' ? '' :
   'typ-secondary')" value="kids"
   on="tap:AMP.setState({selectedCategory: {value: 'kids'}})">
   Kids
   </button>
   2. Add Their Products
   <div class="category category-women" hidden [hidden]="selectedCategory.value !=
   'women'">
   ```
2. Add a list of the products for Kids.

   ```html
   <div class="category category-women" hidden [hidden]="selectedCategory.value !=
   'women'">
   <ul class="product-list">
   <li class="product-item">
   <div class="product-card">
   <div class="img-wrap">
   <!-- Change image src as per your requirements -->
   <amp-img layout="responsive"
   src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-
   1.png"
   alt="Product Image" width="258"
   height="174"></amp-img>
   </div>
   <div class="content-wrap">
   <div class="lhs">
   <h3 class="p-title">Product name</h3>
   </div>
   <div class="rhs">
   <p class="p-amt"><span
   class="rupee">₹</span>1500</p>
   </div>
   </div>
   <p class="p-desc">is simply dummy text of the new age
   fashion industry.</p>
   <a href="https://www.google.co.in/" class="p-link">
   Shop now
   </a>
   </div>
   </li>
   <li class="product-item">
   <div class="product-card">
   <div class="img-wrap">
   <!-- Change image src as per your requirements -->
   <amp-img layout="responsive"
   src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-
   2.png"
   alt="Product Image" width="258"
   height="174"></amp-img>
   </div>
   <div class="content-wrap">
   <div class="lhs">
   <h3 class="p-title">Product name</h3>
   </div>
   <div class="rhs">
   <p class="p-amt"><span
   class="rupee">₹</span>1500</p>
   </div>
   </div>
   <p class="p-desc">is simply dummy text of the new age
   fashion industry.</p>
   <a href="https://www.google.co.in/" class="p-link">
   Shop now
   </a>
   </div>
   </li>
   <li class="product-item">
   <div class="product-card">
   <div class="img-wrap">
   <!-- Change image src as per your requirements -->
   <amp-img layout="responsive"
   src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-
   3.png"
   alt="Product Image" width="258"
   height="174"></amp-img>
   </div>
   <div class="content-wrap">
   <div class="lhs">
   <h3 class="p-title">Product name</h3>
   </div>
   <div class="rhs">
   <p class="p-amt"><span
   class="rupee">₹</span>1500</p>
   </div>
   </div>
   <p class="p-desc">is simply dummy text of the new age
   fashion industry.</p>
   <a href="https://www.google.co.in/" class="p-link">
   Shop now
   </a>
   </div>
   </li>
   <li class="product-item">
   <div class="product-card">
   <div class="img-wrap">
   <!-- Change image src as per your requirements -->
   <amp-img layout="responsive"
   src="https://d1qzvqecfo5h8o.cloudfront.net/images/67Z-875-RR7Z/relevant/women-product-
   4.png"
   alt="Product Image" width="258"
   height="174"></amp-img>
   </div>
   <div class="content-wrap">
   <div class="lhs">
   <h3 class="p-title">Product name</h3>
   </div>
   <div class="rhs">
   <p class="p-amt"><span
   class="rupee">₹</span>1500</p>
   </div>
   </div>
   <p class="p-desc">is simply dummy text of the new age
   fashion industry.</p>
   <a href="https://www.google.co.in/" class="p-link">
   Shop now
   </a>
   </div>
   </li>
   </ul>
   </div>

   ```

   **Output**:

   <Image align="center" alt="Output for Adding Filter" border={true} caption="Output for Adding Filter" src="https://files.readme.io/2568bab6a196e7d5593c99ef2d0a2ad9786717bea7519b0f81d93ff7b5f02e46-Output_for_Adding_New_Filter.png" width="35% " />
