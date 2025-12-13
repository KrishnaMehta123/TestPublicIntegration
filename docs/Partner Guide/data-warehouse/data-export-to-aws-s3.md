---
title: AWS S3
excerpt: Data Warehousing and Analytics Platform
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

The data export feature enables you to bulk export your CleverTap event data to your AWS S3 bucket. You can use this for analysis in BI tools or storage in your data warehouse for analysis in the future.

> 📘 Feature Availability
> 
> This capability is a part of the _Enterprise_, _Advanced_, and _Cutting Edge_ plan. To activate this for your account, contact your Account Manager.

# Setup

The following are the two major steps involved in enabling this feature for your account:

1. [Create an AWS S3 Bucket](doc:data-export-to-aws-s3#create-an-aws-s3-bucket).
2. Configure Buckets details on the CleverTap Dashboard using one of the following methods:
   - [Using Access Key](doc:data-export-to-aws-s3#using-access-key)
   - [Using IAM Policy](doc:data-export-to-aws-s3#using-iam-policy)

> 📘 Data Export
> 
> Once you have set up both dashboards, you can configure export from the CleverTap dashboard. For more information, refer to the following: 
> 
> - [Data Exports](doc:data-exports) for Legacy Profile and Event Export flow
> - [Profile Exports](doc:profile-exports) for Enhanced Profile Export flow

## Create an AWS S3 Bucket

To create an AWS S3 bucket:

1. Log in to your AWS account, then search for _S3_ in the AWS services box. 
2. Select _S3_ from the search results. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb8d83c-Selecting_S3_from_the_list.png",
        "Select S3 from AWS account",
        891
      ],
      "align": "center",
      "border": true,
      "caption": "Select S3 from AWS Account "
    }
  ]
}
[/block]


   Upon clicking, the _Bucket_ page is displayed.

3. Click **Create bucket**. On clicking, the _Create bucket_ page displays:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/111a267-Bucket_page.png",
        "Click Create bucket from Buckets page",
        2876
      ],
      "align": "center",
      "border": true,
      "caption": "Click Create Bucket"
    }
  ]
}
[/block]


4. Enter a bucket name, region, logging, versioning, and encryption preferences. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/407acf4-Create_bucket_page.png",
        "Enter General Configuration for S3 bucket and click Create bucket",
        1628
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Configure S3 Bucket Settings and Click Create Bucket "
    }
  ]
}
[/block]


> 📘 Recommendation for Setup
> 
> For this integration, you need not modify the default settings; however, you must check your internal organization's policies to verify if you need to modify any of these settings.

Based on your CleverTap account settings, we host your data in Europe (EU), the United States (US), Singapore (SG), or India (IN). To identify the region of your account and the corresponding region that you must select when configuring the bucket settings, refer to the following table:

[block:parameters]
{
  "data": {
    "h-0": "CleverTap Dashboard URL",
    "h-1": "Region",
    "h-2": "AWS S3 Bucket Region",
    "0-0": "[https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html#/)",
    "0-1": "EU",
    "0-2": "EU (Ireland) eu-west-1",
    "1-0": "[https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html#/)",
    "1-1": "India",
    "1-2": "Asia Pacific (Mumbai) ap-south-1",
    "2-0": "[https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html#/)",
    "2-1": "US",
    "2-2": "US West (Oregon) us-west-2",
    "3-0": "[https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html#/)",
    "3-1": "Singapore",
    "3-2": "Asia Pacific (Singapore)  \nap-southeast-1",
    "4-0": "<https://mec1.dashboard.clevertap.com/login.html>",
    "4-1": "Middle East (UAE)",
    "4-2": " Middle East (UAE) me-central-1",
    "5-0": "<https://aps3.dashboard.clevertap.com/login.html>",
    "5-1": "Indonesia",
    "5-2": "Asia Pacific (Jakarta) ap-southeast-3"
  },
  "cols": 3,
  "rows": 6,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


> 📘 Set Up AWS Bucket Region
> 
> When setting up the AWS bucket region for your AWS account, ensure that the AWS bucket region matches your CleverTap account region. To identify the region of your CleverTap account, refer to the above table. 
> 
> Also, you can set up the CleverTap account region only once during registration.

5. Click **Create bucket**. On successful bucket creation, the following message displays in the snack bar at the top:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/681e832-Successful_bucket_creation.png",
        "S3 Bucket created successfully message displays at the top",
        2770
      ],
      "align": "center",
      "border": true,
      "caption": "S3 Bucket Created Successfully"
    }
  ]
}
[/block]


The bucket you just created now appears in your S3 console. We recommend you note down the name of your new bucket, as you will need it for the next step.

## Configure S3 Bucket Details on CleverTap Dashboard

### Using IAM Policy

The following are the two major steps to configure S3 bucket details on the CleverTap dashboard using IAM Policy

i. [Copy IAM Policy from the CleverTap dashboard](doc:data-export-to-aws-s3#copy-iam-policy-from-the-clevertap-dashboard)

ii. [Add IAM Policy to S3 Bucket from AWS console](doc:data-export-to-aws-s3#add-iam-policy-to-s3-bucket-on-aws-console) 

#### Copy IAM Policy from the CleverTap Dashboard

To copy the IAM policy from the CleverTap dashboard:

1. Navigate to _Settings_ > _Partners_ and click **View Details** against Amazon S3. The _Integrate analytics partner - Amazon S3_ window displays on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/27118b6-Integrate_Analytics_Partner_-_AWS_S3.png",
        "Click View Details against Amazon S3 from Partner page",
        1500
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Click View Details against Amazon S3 from Partner Page"
    }
  ]
}
[/block]


2. Click **+ Amazon S3 Bucket** to create a new bucket.
3. Enter the _Bucket name_. 
4. Select _IAM (Identity and Access Management) Policy_ option under _Configure with_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/475094f-Select_IAM_Policy_option.png",
        "Enter Bucket URL and select IAM Policy option",
        1446
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Configure S3 Bucket with IAM Policy"
    }
  ]
}
[/block]


5. Click the ![](https://files.readme.io/2bd537e-Copy_icon.png) icon to copy the policy to the clipboard and keep this window open for saving these details later.

#### Add IAM Policy to S3 Bucket on AWS Console

To add IAM policy to the S3 bucket:

1. Select the bucket from the Bucket page of the AWS console.
2. Select the _Permissions_ tab.
3. Click **Edit** under the _Bucket policy_ section and enter the policy that you copied in Step _4_ of [Copy IAM Policy from the CleverTap dashboard](doc:data-export-to-aws-s3#copy-iam-policy-from-the-clevertap-dashboard):

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/438b0da-Add_IAM_policy_to_S3_Bucket.png",
        "Click Edit to edit S3 bucket policy",
        2052
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Edit S3 Bucket Policy"
    }
  ]
}
[/block]


```json IAM Policy
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::062484260092:root"
            },
            "Action": "s3:PutObject*",
            "Resource": "arn:aws:s3:::bucket-name/*"
        },
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::062484260092:root"
            },
            "Action": "s3:PutObject*",
            "Resource": "arn:aws:s3:::bucket-name"
        }
    ]
}
```

> 🚧 IMPORTANT
> 
> Ensure that you replace all the occurrences of `bucket-name` in the above JSON payload with your actual bucket name.

4. Click **Save Changes** to save the policy.
5. Go back to the same window opened in _Step 4_ of [Copy IAM Policy From CleverTap Dashboard](doc:data-export-to-aws-s3#copy-iam-policy-from-the-clevertap-dashboard) and click **Save Credentials**.

The Amazon S3 bucket is now configured on both the AWS S3 console and the CleverTap dashboard. 

### Using Access Key

The following are the two major steps to configure S3 bucket details on the CleverTap dashboard using Access Key:

i. [Create an API Key for Your S3 Bucket](doc:data-export-to-aws-s3#create-an-api-key-for-your-s3-bucket).

ii. [Add Your S3 Bucket Details to CleverTap](doc:data-export-to-aws-s3#add-your-s3-bucket-details-to-clevertap).

#### Create an API Key for Your S3 Bucket

This section demonstrates the creation of an AWS API key with write access to the bucket we created in the above step. CleverTap uses this API key to export data to your S3 bucket.

1. Click on your account name on the top right of the AWS console.
2. Select _Security credentials_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/152163f-Security_credentials.png",
        "Select Security credentials option",
        388
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Select Security credentials"
    }
  ]
}
[/block]


3. Select _Users_ from the left navigation and click **Add user**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8b81e57-Click_Add_users.png",
        "Click Add users from the User page",
        2878
      ],
      "align": "center",
      "border": true,
      "caption": "Add Users"
    }
  ]
}
[/block]


On clicking, the _Add user_ page displays.

4. Enter the _User name_ and select the _Programmatic access_ checkbox.
5. Click **Next:Permissions**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7840a59-Add_user.png",
        "Enter the User name, select AWS credential type and click Next: Permissions",
        2878
      ],
      "align": "center",
      "border": true,
      "caption": "Select AWS Access Type and Click Next: Permissions"
    }
  ]
}
[/block]


On clicking, _Set permissions_ page displays.

6. Click **Create group** under _Add user to group_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/592634b-Create_group.png",
        "Click Create group under Add user to group tab",
        2872
      ],
      "align": "center",
      "border": true,
      "caption": "Add User to Group"
    }
  ]
}
[/block]


On clicking, _Create group_ page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5cfd145-Create_group_page.png",
        "Assign policy to group",
        2482
      ],
      "align": "center",
      "border": true,
      "caption": "Assign Policy to Group"
    }
  ]
}
[/block]


7. Click **Create policy**. On clicking, _Create policy_ page opens in a new tab.
8. Select the **JSON** tab and then paste the JSON code given below in the box. 
9. Replace `clevertap-example` in the JSON code with the name of the S3 bucket you created in the above step.  
   The permissions defined in this policy allow CleverTap to get information about your bucket and upload files to it.

> 📘 AWS API Access Policies
> 
> _IP Whitelisting_ is not supported with S3 exports. For more information about AWS API access policies, refer to [this post](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_s3_rw-bucket-console.html) from the AWS blog.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc21bb7-Replace_JSON_code.png",
        "Bucket policy in JSON format",
        2874
      ],
      "align": "center",
      "border": true,
      "caption": "Bucket Policy in JSON Format"
    }
  ]
}
[/block]


```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:ListBucket"
            ],
            "Resource": [
                "arn:aws:s3:::clevertap-example"
            ]
        },
        {
            "Effect": "Allow",
            "Action": [
                "s3:PutObject"
            ],
            "Resource": [
                "arn:aws:s3:::clevertap-example/*"
            ]
        }
    ]
}
```

10. Click **Next: Tags**  and then click **Next: Review**. On clicking, the _Create policy_ page opens.
11. Enter the policy _Name_ and click **Create policy**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f81305a-Create_policy.png",
        "Enter policy name and click Create policy",
        2648
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Policy Name and Click Create policy"
    }
  ]
}
[/block]


On successful policy creation, the following message displays in the snack bar at the top:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc7b89a-Policy_created_successfully.png",
        "Policy created successfully message displays at the top",
        2870
      ],
      "align": "center",
      "border": true,
      "caption": "Bucket  Policy Created Successfully"
    }
  ]
}
[/block]


12. Go back to the _Create group_ page (opened in _Step 6_), search for the policy you just created, and assign it to the new group by selecting the checkbox.
13. Click **Create group**. On clicking, the _Add user_ page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c28e813-Search_policy.png",
        "SSelect Policy and Click Create Group",
        2486
      ],
      "align": "center",
      "border": true,
      "caption": "Select Policy and Click Create Group"
    }
  ]
}
[/block]


14. Click **Next: Tags** and then click **Next: Review**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/15f1ead-Click_Next_Tags.png",
        "Click Next: Tags.png",
        2012
      ],
      "align": "center",
      "border": true,
      "caption": "Click Next: Tags"
    }
  ]
}
[/block]


15. Click **Create user**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d88007d-Create_user.png",
        "Click Create user",
        1980
      ],
      "align": "center",
      "border": true,
      "caption": "Click Create user"
    }
  ]
}
[/block]


On successful user creation, the following page displays. You will see your _Access key ID_ and the _Secret access key_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3b1def-Access_key_and_secret_access_key.png",
        "Copy or download Access key ID and Secret access key",
        2878
      ],
      "align": "center",
      "border": true,
      "caption": "Copy or Download User Security Credentials"
    }
  ]
}
[/block]


These credentials allow CleverTap to upload files to your S3 bucket. We recommend you note down these values as you will require them for the next step. Otherwise, you can also click **Download .csv** to save these details for future use.

#### Add Your S3 Bucket Details to CleverTap

To add your S3 bucket details to Clevertap, perform the following steps:

1. Go to _Settings_ > _Partners_ and click **View Details** against Amazon S3. The _Integrate analytics partner - Amazon S3_ window displays on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6ab03f2-Integrate_Analytics_Partner_-_AWS_S3.png",
        "Integrate Analytics Partner - AWS S3.png",
        1500
      ],
      "align": "center",
      "border": true,
      "caption": "Click View Details against Amazon S3 from Partners Page"
    }
  ]
}
[/block]


2. Click **+ Amazon S3 Bucket** to create a new bucket. The _Integrate Amazon S3 Bucket_ window opens on the right side of the screen. 
3. Enter the _Bucket nickname_ and _Bucket URL_. 
4. Select the _User details_ option under _Configure with_ section.
5. Enter your _Access key ID_ and the _Secret access key_ obtained earlier and click **Save Credentials**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5f44e48-Select_User_details_option.png",
        "Select User details and enter the user security credentials",
        1494
      ],
      "align": "center",
      "border": true,
      "caption": "Enter User Security Credentials and Click Save Credentials "
    }
  ]
}
[/block]


# FAQs

### What permission is required for CleverTap to export data to your AWS S3 bucket?

A. CleverTap needs write permission to be able to export data to your AWS S3 bucket, as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7bed273-Select_IAM_Policy_option.png",
        "IAM Policy to provide CleverTap with write access",
        1446
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "IAM Policy to Provide CleverTap with Write Access"
    }
  ]
}
[/block]


### What should I do if I already have an existing IAM policy for the AWS S3 bucket?

Ensure that you modify the current IAM policy to provide CleverTap with write access to export data to your AWS S3 bucket.