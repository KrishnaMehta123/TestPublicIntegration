---
title: Device Previews for A/B Tests
excerpt: Learn how to preview A/B Tests on test devices.
deprecated: false
hidden: true
metadata:
  robots: index
---
<br />

# Overview

Before publishing your A/B tests, you can **preview and test variants across multiple devices** to ensure everything works as expected. CleverTap’s enhanced A/B Test feature allows you to test on registered devices, view live variants, and run multiple tests.

The _Device Previews_ in CleverTap enable you to:

* Mark devices as _test devices_ and target them for QA.
* Assign specific variants to individual devices or user profiles.
* Verify app behavior and visual consistency before rollout.

This feature is designed for QA, marketing, and product teams who want complete control over their A/B testing environment.

# Prerequisites

Before testing an A/B experiment:

* Check that your _CleverTap SDK_ is updated to the latest version that supports test device registration.
* You must have access permissions for _A/B test creation_ and _Device Previews_.
* The devices you plan to use for testing must be part of a test profile.

# Mark a Profile as Test Profile

A Test Profile lists all the devices associated with it. Before assigning test devices to variants, you must first mark the user profile as a Test Profile. To mark a profile as a test profile, do the following:

1. Go to _Segments > Find People_.
2. Search for a user profile using _Identity_ or _CleverTap ID_.
3. Select **mark as test profile**.

For more information, refer to [Mark a user profile as a Test Profile](https://docs.clevertap.com/docs/user-profiles#mark-a-user-profile-as-a-test-profile).

# Assign Test Devices to Variants

1. Go to Product Experiences > A/B Tests
2. [Create a new A/B Test](https://docs.clevertap.com/docs/create-ab-tests) or open an existing A/B Test.
3. Under the _Device Preview_ section, click **Add Preview**. The users and devices are listed. Each entry shows the following:
   * **Test User or Profile Name**
   * **Preview Status** (Active or Inactive)
   * **Preview Devices** (number of devices linked)
   * **Variant** assigned to that device
4. Select the Test Users and Devices.
5. Select the variant for the selected device and click **Save**.

<Callout icon="📘" theme="info">
  Note

  You can mark multiple devices on the same user profile. Only devices marked as test devices appear in the **Test Devices** selector during A/B test setup.

  This allows different devices under the same profile to preview distinct variants, such as:

  * **Variant A** on the _Home screen_ of an iPhone
  * **Variant B** on the _Settings screen_ of a Pixel device
</Callout>

Use this panel to:

* Start or stop previews
* Deselect or clear specific devices
* Quickly compare variant performance in real-time environments

<Callout icon="👍" theme="okay">
  Tip

  You can now conduct **multiple A/B tests simultaneously**, making parallel QA testing possible across teams.
</Callout>

# Stop or Edit a Device Preview

<Image align="center" border={false} caption="Edit Preview Devices" src="https://files.readme.io/1e3c39f86bcf069cbb503baae7999cf4711fbce85a0e833d6c7b628caf2196d9-image.png" />

To modify or stop an active test session:

1. View Running Tests in the A/B Test dashboard.
2. From the _Device Previews_ section, select the profiles and devices.
3. You can either edit the device preview or do the following:

   * **Update Test** – to add or remove devices.
   * **Stop Test** – to end test mode for that session.
   * **Delete** – to remove the device from the preview.

<Callout icon="📘" theme="info">
  Note

  Stopping a preview only removes the device from device list. It does not affect your published A/B test configuration.
</Callout>

# Troubleshooting

| Issue                          | Cause                                     | Solution                                                                            |
| ------------------------------ | ----------------------------------------- | ----------------------------------------------------------------------------------- |
| Test device not visible        | Device not registered                     | Go to **Find People**, mark the device as a test device, and refresh the dashboard. |
| Unable to start multiple tests | Another test is still in single-test mode | Ensure all tests are saved and enable  _Device Preview_ for each individually.      |
| Variant not loading            | Incorrect device linkage                  | Verify the device’s variant assignment in the **Variables** tab and re-publish.     |

# FAQs

**Can I run multiple tests in Test Mode?**
Yes. You can now preview and test multiple A/B experiments simultaneously.

**Do test devices affect production users?**
No. Only registered test devices get variant changes.

**Can I remove the test device later?**
Yes. Remove the device by editing Device Previews.