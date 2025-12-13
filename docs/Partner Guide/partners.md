---
title: Technology Partners
excerpt: Learn about CleverTap's third-party integration
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Analytics

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
  <a href="https://docs.clevertap.com/docs/amplitude">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/f4f59df2070156a00d549967bcdd67c7fad4157253db4fd1d512a38738a16e98-Amplitude_idlx3byNUU_0.svg" alt="Amplitude" class="logo">
        </div>
        <div class="content">
            <div class="name">Amplitude</div>
            <div class="category">Analytics</div>
        </div>
    </div>
</a>
<a href="https://docs.clevertap.com/docs/mixpanel">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/cd97b5982cb3408405a2b6999592b7a5ed386a73b807ed53577149ba173cc245-Mixpanel_Symbol_0.svg" alt="Mixpanel" class="logo">
        </div>
        <div class="content">
            <div class="name">Mixpanel</div>
            <div class="category">Analytics</div>
        </div>
    </div>
</a> 
    </div>
</body>
</html>
`}</HTMLBlock>

# Attribution

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
  <a href="https://developer.clevertap.com/docs/adjust">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/487110869d01e0f2e506e9748d03217555ba50b6fc30f24fcd22ceeee65047a4-Adjust_idZed2gUTA_0.svg" alt="Adjust" class="logo">
        </div>
        <div class="content">
            <div class="name">Adjust</div>
            <div class="category">Attribution</div>
        </div>
    </div>
</a>

<a href="https://developer.clevertap.com/docs/airbridge">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/93bb344627f1bd8a4d187ff5ebc1da06604fb3a7805ea6fdae208089fb6c5b6b-Airbnb_Symbol_0.svg" alt="Airbridge" class="logo">
        </div>
        <div class="content">
            <div class="name">Airbridge</div>
            <div class="category">Attribution</div>
        </div>
    </div>
</a>

<a href="https://developer.clevertap.com/docs/appsflyer">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/fe763ec13f8c9d9a6a85e13a0f1ac9b8e352c8dee2887f25025a728f94204499-AppsFlyer_idZaZLy7nj_0.svg" alt="AppsFlyer" class="logo">
        </div>
        <div class="content">
            <div class="name">AppsFlyer</div>
            <div class="category">Attribution</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/apptrove">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/1d84909a84cbc1303083f451b01b6345f8329ac4a8bc8a0bf675153453cea99c-Apptrove.webp" alt="AppTrove" class="logo">
        </div>
        <div class="content">
            <div class="name">AppTrove</div>
            <div class="category">Attribution</div>
        </div>
    </div>
</a>

<a href="https://developer.clevertap.com/docs/branch">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/311972c7da6cd9956e8110911d763cb514aa30b6354505c4f6a38aea2f011ef6-Branch_idSRMs7jP1_0.svg" alt="Branch" class="logo">
        </div>
        <div class="content">
            <div class="name">Branch</div>
            <div class="category">Attribution</div>
        </div>
    </div>
</a>

<a href="https://developer.clevertap.com/docs/singular-apsalar">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/6865a95b6399b793b628eba0eec9b1a5ee851bea5b0f3eea31acf796042b599b-Singular_id1QD_LCjD_0.svg" alt="Singular" class="logo">
        </div>
        <div class="content">
            <div class="name">Singular</div>
            <div class="category">Attribution</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Contextual Location

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
  <a href="https://docs.clevertap.com/docs/open-weather">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/22be2632e5d304701ba8434cc0ad71d1baac177d941bc00b7f8c6340176124c0-OpenWeather.jpeg" alt="OpenWeather" class="logo">
        </div>
        <div class="content">
            <div class="name">OpenWeather</div>
            <div class="category">Contextual Location</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/plot-projects">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/6170d4f9636b30c0ca0cd6627a4709cca545f5f7a7deab59c2ad5e5cd35260fa-PlotProjects.webp" alt="Plot Projects" class="logo">
        </div>
        <div class="content">
            <div class="name">Plot Projects</div>
            <div class="category">Contextual Location</div>
        </div>
    </div>
</a> 
   
  </div>
</body>
</html>
`}</HTMLBlock>

# Crash Analytics

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/apteligent">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/70fbc5c82ff59badd58a4faad563c59fd734cfdfda1f55ed55f6916c474c75f8-Apteligent.jpeg" alt="Apteligent" class="logo">
        </div>
        <div class="content">
            <div class="name">Apteligent</div>
            <div class="category">Crash Analytics</div>
        </div>
    </div>
</a>
      
    </div>
</body>
</html>
`}</HTMLBlock>

# Customer Data Platform

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/census">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/716b768699d89bfcd39f879b5177c056e37cfd7b44d8c01debd34bd78d6bf736-Census.jpeg" alt="Census" class="logo">
        </div>
        <div class="content">
            <div class="name">Census</div>
            <div class="category">Customer Data Platform</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/hightouch">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/0d223308a7381e461315d3e21a6298699ad3cd135b060ae328c9593852fc1154-Hightouch.jpeg" alt="Hightouch" class="logo">
        </div>
        <div class="content">
            <div class="name">Hightouch</div>
            <div class="category">Customer Data Platform</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/mparticle-2">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/937f6e9417ec3511d650a487fbb499984e6c162c0b8e3def342dadd343e2e46d-mParticle.png" alt="mParticle" class="logo">
        </div>
        <div class="content">
            <div class="name">mParticle</div>
            <div class="category">Customer Data Platform</div>
        </div>
    </div>
</a>

<a href="https://developer.clevertap.com/docs/rudderstack">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/64575102b5ccac664d6757f23bcae33e7f1eed6d264061fdfa0bbb97528c8e84-RudderStack_Symbol_0.svg" alt="RudderStack" class="logo">
        </div>
        <div class="content">
            <div class="name">RudderStack</div>
            <div class="category">Customer Data Platform</div>
        </div>
    </div>
</a>

<a href="https://developer.clevertap.com/docs/segment">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/23acd4b1d664a001eb0d7212381744cb5a959237c6e64c9f25eb7a2c3c6497e2-Segment_Symbol_0.svg" alt="Segment" class="logo">
        </div>
        <div class="content">
            <div class="name">Segment</div>
            <div class="category">Customer Data Platform</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/treasuredata-cdp">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/ecd32ffc1a6936da60649274cf5dab0cdee6fe58ea6d33334f67e143c4a479e9-Treasure_Data_idr5-pui94_1.png" alt="Treasure Data" class="logo">
        </div>
        <div class="content">
            <div class="name">Treasure Data</div>
            <div class="category">Customer Data Platform</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Data Warehouse

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/amazon-eventbridge">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/93783ddfa75cf49849085df73055ed5648715c6e5986cda3a2a1c5713ef79b5d-AWS_S3_Eventbridge.jpeg" alt="Amazon EventBridge" class="logo">
        </div>
        <div class="content">
            <div class="name">Amazon EventBridge</div>
            <div class="category">Data Warehouse</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/data-export-to-aws-s3">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/93783ddfa75cf49849085df73055ed5648715c6e5986cda3a2a1c5713ef79b5d-AWS_S3_Eventbridge.jpeg" alt="AWS S3 Export" class="logo">
        </div>
        <div class="content">
            <div class="name">AWS S3 Export</div>
            <div class="category">Data Warehouse</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/bigquery">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/64b5008bd247a0d67e3d8a777a71cc40542c23ff8a2f9baf10a417ff94dad2f7-BigQuery.png" alt="BigQuery" class="logo">
        </div>
        <div class="content">
            <div class="name">BigQuery</div>
            <div class="category">Data Warehousing</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/data-export-to-gcp">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/5d8f65d75d9cfaa7c388beb52805563d3ac83b071eee9ad0138afd672d275577-Google_Cloud_Platform.webp" alt="Google Cloud Platform" class="logo">
        </div>
        <div class="content">
            <div class="name">Google Cloud Platform (GCP)</div>
            <div class="category">Data Warehouse</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/microsoft-azure-export">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/8507d14dd44a824a548d802a530aafde484834cb5f7ccaac3fdbae692fccdaa6-Microsoft_Azure_Portal_idc8nWN0hO_0.svg" alt="Microsoft Azure" class="logo">
        </div>
        <div class="content">
            <div class="name">Microsoft Azure</div>
            <div class="category">Data Warehouse</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Dynamic Content

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/storyly">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/e03ffe21e4cb257fa8239401afb55a0107b184f71794d4a9f97445a8d133e704-Storyly.jpeg" alt="Storyly" class="logo">
        </div>
        <div class="content">
            <div class="name">Storyly</div>
            <div class="category">Dynamic Content</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# E-Commerce

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/shopify">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/5bed2229829e9411ff820f536a100b9592c2eb0d6136109dba98561115e0fb69-Shopify.com_Symbol_0.svg" alt="Shopify" class="logo">
        </div>
        <div class="content">
            <div class="name">Shopify</div>
            <div class="category">E-Commerce</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Email

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/amazon-simple-email-service">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/f7b8c289ace53bf772fc0a8b13ad3a47470e9800bda44e6c1aab9ac9b8e13f1f-Simple_Email_Service.png" alt="Amazon Simple Email Service" class="logo">
        </div>
        <div class="content">
            <div class="name">Amazon Simple Email Service</div>
            <div class="category">Email</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/mandrill">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/f025167126f2b07919e65afb6a72c9c0ade83a75c6190384aded79d3343d1654-Mandrill.jpeg" alt="Mandrill" class="logo">
        </div>
        <div class="content">
            <div class="name">Mandrill</div>
            <div class="category">Email</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/postmark">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/572f6c80eb6165130396b72959d420323abe3017ab6f3f7a3994f7221de0cb93-Postmark.png" alt="Postmark" class="logo">
        </div>
        <div class="content">
            <div class="name">Postmark</div>
            <div class="category">Email</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/sendgrid">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/50520ec5a42cc4331d440fd5a33ad0247585ae414c75871f118eb87d0b8ba3bb-SendGrid_Symbol_0.svg" alt="SendGrid" class="logo">
        </div>
        <div class="content">
            <div class="name">SendGrid</div>
            <div class="category">Email</div>
        </div>
    </div>
</a>
<a href="https://docs.clevertap.com/docs/deeplinking-with-branch">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/311972c7da6cd9956e8110911d763cb514aa30b6354505c4f6a38aea2f011ef6-Branch_idSRMs7jP1_0.svg" alt="Deeplinking with Branch" class="logo">
        </div>
        <div class="content">
            <div class="name">Deeplinking with Branch</div>
            <div class="category">Attribution</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Email Validator

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/clearout">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/f53513e04b71ff3c0aa016155ecf437f136140cfd060a87c7af6359df8f4b6eb-Clearout.png" alt="Clearout" class="logo">
        </div>
        <div class="content">
            <div class="name">Clearout</div>
            <div class="category">Email Validator</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Localization

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/crowdin">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/0b8af82f6aa48ed325357cd7b7ac6106a0a43563407d10dede8abc62d02cba55-Crowdin.jpeg" alt="Crowdin" class="logo">
        </div>
        <div class="content">
            <div class="name">Crowdin</div>
            <div class="category">Localization</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/lokalise">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/a80f7428262717774b0bfe20148e67fc42e5e56a1d2e7b0afc9d536249dcb34d-Lokalise_idlLZ8_ln3_0.svg" alt="Lokalise" class="logo">
        </div>
        <div class="content">
            <div class="name">Lokalise</div>
            <div class="category">Localization</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Loyalty

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/talonone">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/0b8dabb5155d5a9d9d9901a1236fc3691cf193f580643f1759fb89142900168a-Talon.One.png" alt="Talon.One" class="logo">
        </div>
        <div class="content">
            <div class="name">Talon.One</div>
            <div class="category">Loyalty</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/voucherify">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/fd42cbb0b92d6ae2159e0707bdf740f903e1d0bb07215b2ae38d172b0dea7f0d-Voucherify.jpeg" alt="Voucherify" class="logo">
        </div>
        <div class="content">
            <div class="name">Voucherify</div>
            <div class="category">Loyalty</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Messenger

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->

<a href="https://docs.clevertap.com/docs/line-messenger">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/0ec3dc2ff75c076e12f5969e4f47bd9c193f9914ff8989a29e89cf7dadba1951-line.png" alt="LINE" class="logo">
        </div>
        <div class="content">
            <div class="name">LINE</div>
            <div class="category">Messenger</div>
        </div>
    </div>
</a>
      <a href="https://docs.clevertap.com/docs/sendbird-business-messaging">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/b9304e06560e5b56147bc6ab80e2711386f1dfa56a63a1edd70f248adb931a7b-Sendbird.jpeg" alt="Sendbird" class="logo">
        </div>
        <div class="content">
            <div class="name">Sendbird</div>
            <div class="category">Messenger</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Messaging Template

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/stripo">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/5ff9d0c27b076734f3b800277a4cb104730f07c6d4181265170fe917666a08dd-Stripo.jpeg" alt="Taxi for Email" class="logo">
        </div>
        <div class="content">
            <div class="name">Stripo</div>
            <div class="category">Email Templates</div>
        </div>
    </div>
</a>
      <a href="https://docs.clevertap.com/docs/taxi-for-email">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/dde396ef5ccd49f3346ade3aaf754d65e751938a12c463bd24b14e9d034a247a-Taxi_for_Email.jpeg" alt="Taxi for Email" class="logo">
        </div>
        <div class="content">
            <div class="name">Taxi for Email</div>
            <div class="category">Email Templates</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Payments

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/revenuecat">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/0c64232782e0973162f1b629425b5fafee30b3aafc2e5566ff125a2b8e6665e0-RevenueCat.jpeg" alt="RevenueCat" class="logo">
        </div>
        <div class="content">
            <div class="name">RevenueCat</div>
            <div class="category">Payments</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Remarketing

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/facebook-audience-network-1">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/ce9618bf8a67a2eb1cb026cb8603318b81b8218562fa805c333c531403a2a4c9-Facebook_Symbol_0.svg" alt="Facebook Audience Network" class="logo">
        </div>
        <div class="content">
            <div class="name">Facebook Audience Network</div>
            <div class="category">Remarketing</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/google-adwords-remarketing">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/80939fd90693533ee04dc1c06c9fe653386a05712a689ca2aad26fd52b9263ee-Google_Ads.jpeg" alt="Google Ads Remarketing" class="logo">
        </div>
        <div class="content">
            <div class="name">Google Ads</div>
            <div class="category">Remarketing</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/tiktok-remarketing-1">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/14ea9f0f2d1b3edd08dc3ee8df7592acce126e6db2121b7c29e8f72cc5a8b409-TikTok_Logo_Alternative_0.svg" alt="TikTok Remarketing" class="logo">
        </div>
        <div class="content">
            <div class="name">TikTok Remarketing</div>
            <div class="category">Remarketing</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# SMS

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/generic-sms">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/c75a975ae4ba728b9d8f80ea1fd710f1d69f33bb2e9d0b0b373226c5044c9762-BulkSMS.jpeg" alt="BulkSMS" class="logo">
        </div>
        <div class="content">
            <div class="name">BulkSMS</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/exotel">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/89a86c79cf4fe27f746a979545dffce12dc4292a2e42cfc3607aba2cf1315b02-Exotel.jpeg" alt="Exotel" class="logo">
        </div>
        <div class="content">
            <div class="name">Exotel</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/infobip-sms">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/8f8fb96c455eedc6728f420f2b1aba195a148bbfc07cc20f4721a4e3fbc1a802-Infobip_id8JKsF2ld_0.svg" alt="Infobip" class="logo">
        </div>
        <div class="content">
            <div class="name">Infobip</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/msg91">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/4c7f4dfa7b7e264c616f1ebf7ddbd6da15238eb1585e12287eef47a70070bd94-MSG91.png" alt="MSG91" class="logo">
        </div>
        <div class="content">
            <div class="name">MSG91</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/netcore">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/17b93b939ba0a468beb925a169a371cd811f55f415aa5a7828f126c03a912dc9-Netcore_Cloud_idB8rkalPb_0.svg" alt="Netcore" class="logo">
        </div>
        <div class="content">
            <div class="name">Netcore</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/nexmo">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/dfed8a138edd91e7da9627c3c45a7c15968897031e15a4125c80457aea0be73d-Nexmo.png" alt="Nexmo/Vonage" class="logo">
        </div>
        <div class="content">
            <div class="name">Nexmo/Vonage</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/generic-sms">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/f114f9b46a74e7753c5be56aac3c04634e8ce62c8c03731686a6d162cdba5db4-Nimbus_SMS.jpeg" alt="Nimbus SMS" class="logo">
        </div>
        <div class="content">
            <div class="name">Nimbus SMS</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/generic-sms">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/eba88cb6c54c161ff4e417acdd71e75413d9f33eab53bd02add25c1b3e23b944-Plivo.jpeg" alt="Plivo" class="logo">
        </div>
        <div class="content">
            <div class="name">Plivo</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/generic-sms">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/c0d1e9a5f1f7f36f807a2c27bf1ed65435730e321e61a33e758a1f93a52fe9a5-SMSINDIAHUB.png" alt="SMSINDIAHUB" class="logo">
        </div>
        <div class="content">
            <div class="name">SMSINDIAHUB</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/generic-sms">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/1f2a9cbaa50afb424a71f3a29df3e5ddcbbcd1baf65aac6270622d8b271481f1-TextLocal.jpeg" alt="TextLocal" class="logo">
        </div>
        <div class="content">
            <div class="name">TextLocal</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/times-mobile">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/e8484000bcf1c84dbf071c91110c800b9125dee65d53b06a8871465672aa7b2d-TimesMobile.webp" alt="Times Mobile" class="logo">
        </div>
        <div class="content">
            <div class="name">Times Mobile</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/twilio">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/fff6322c139e023770b83e4c0e7d8660178446edf62c842683f2f86877a74152-Twilio_idseuPD28S_0.svg" alt="Twilio" class="logo">
        </div>
        <div class="content">
            <div class="name">Twilio</div>
            <div class="category">SMS</div>
        </div>
    </div>
</a>   
    </div>
</body>
</html>
`}</HTMLBlock>

# Support

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
   <a href="https://docs.clevertap.com/docs/zendesk">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/9222da2a1de0404917acf81a88b05ab8e56881e630ce139976d73eaab562aa7f-Zendesk_Symbol_0.svg" alt="Zendesk" class="logo">
        </div>
        <div class="content">
            <div class="name">Zendesk</div>
            <div class="category">Support</div>
        </div>
    </div>
</a>
  </div>
</body>
</html>
`}</HTMLBlock>

# WhatsApp

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->

<a href="https://docs.clevertap.com/docs/gupshup">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/4139ddd02258c0a239367f32365c632040dd4bdcb0fe0743f9f4eec15fb5d828-Gupshup_copy.jpeg" alt="Gupshup" class="logo">
        </div>
        <div class="content">
            <div class="name">Gupshup</div>
            <div class="category">WhatsApp</div>
        </div>
    </div>
</a>
<a href="https://docs.clevertap.com/docs/nexmo-whatsapp">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/dfed8a138edd91e7da9627c3c45a7c15968897031e15a4125c80457aea0be73d-Nexmo.png" alt="Nexmo" class="logo">
        </div>
        <div class="content">
            <div class="name">Nexmo</div>
            <div class="category">WhatsApp</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/exotel-whatsapp">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/89a86c79cf4fe27f746a979545dffce12dc4292a2e42cfc3607aba2cf1315b02-Exotel.jpeg" alt="Exotel" class="logo">
        </div>
        <div class="content">
            <div class="name">Exotel</div>
            <div class="category">WhatsApp</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/haptik">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/897664a2ce703c15f3b4c316c34b0ae0edb5a0df7a86edf21668ef8f65c65055-Haptik.svg" alt="Haptik" class="logo">
        </div>
        <div class="content">
            <div class="name">Haptik</div>
            <div class="category">WhatsApp</div>
        </div>
    </div>
</a>
<a href="https://docs.clevertap.com/docs/kaleyra">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/5c1d4b35de4b78d5cf5e97bd7bea915847e9507f8d24486c377c7ea590b5adaa-Kaleyra.jpeg" alt="Kaleyra" class="logo">
        </div>
        <div class="content">
            <div class="name">Kaleyra</div>
            <div class="category">WhatsApp</div>
        </div>
    </div>
</a>

<a href="https://docs.clevertap.com/docs/infobip">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/8f8fb96c455eedc6728f420f2b1aba195a148bbfc07cc20f4721a4e3fbc1a802-Infobip_id8JKsF2ld_0.svg" alt="Infobip" class="logo">
        </div>
        <div class="content">
            <div class="name">Infobip</div>
            <div class="category">WhatsApp</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>

# Workflow Automation

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {am
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
<a href="https://docs.clevertap.com/docs/zapier">
    <div class="integration-card">
        <div class="logo-container">
            <img src="https://files.readme.io/9986166ddfb29f93a834963deb0c216be7c1c20b896a77e06fc2531d4d038b08-Zapier.jpeg" alt="Zapier" class="logo">
        </div>
        <div class="content">
            <div class="name">Zapier</div>
            <div class="category">Workflow Automation</div>
        </div>
    </div>
</a>
    </div>
</body>
</html>
`}</HTMLBlock>
