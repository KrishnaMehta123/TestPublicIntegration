---
title: 'A/B Test: FAQs'
excerpt: Learn about the frequently asked questions around A/B Tests.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# FAQs

Listed below are some FAQs that help you find answers to critical questions about A/B Tests.

### Q. What role does the control variant play in an A/B test?

The control variant functions as the benchmark used for comparison within an A/B test. It embodies the standard user experience, whether it pertains to a specific app interaction or message.

When testing a variable, the control variant aligns with the override values on the Remote Config Dashboard. If no override value has been set, it reverts to the default value defined in the code.

### Q. Can a user participate in multiple tests simultaneously?

Yes, if a user meets the targeting criteria for more than one test, they might be included in multiple tests at the same time.

### Q. What happens when a user qualifies for multiple A/B Tests?

When a user qualifies for multiple A/B tests that impact the same variable, CleverTap displays the experience from the test published first. To ensure that users see the experience of the newer test instead, perform either of the following steps:

Ensure that the targets for the two tests are mutually exclusive.

OR

Complete any other tests that influence the variable before creating a new test.

### Q. How can I target an A/B test exclusively to new users?

To target new users specifically, go to the *Targets* section and select *Behavioral* > *First-time users*. By default, the targeting is *Sticky*, meaning new users who see the A/B test continue to be a part of the test beyond their first session. If you prefer new users only to experience the A/B test during their initial session, clear the [*Sticky*](doc:create-ab-tests#sticky-target) option to disable sticky targeting. 

### Q. What happens when a user logs in to two devices and is a part of an A/B test?

As long as we have identified this as the same user but with a different device, the user will continue to be part of the A/B Test.\
In case the A/B Test has device-level target rules, such as "OS = iOS" but the user has logged in from an Android device, then whether the user will remain in the test or exit depends on the [Sticky Target](doc:create-ab-tests#sticky-target) configuration of the A/B Test.

### Q. What happens to users in a variant if the percentage allocation changes?

 Currently, modifying the percentage distribution for the variant is not allowed while the test is running.

### Q. Is it possible for a user to encounter multiple distinct variants within one test?

We use the User ID and A/B test ID as inputs for the logic determining the Variant in which a user will be placed. This ensures that users remain consistently assigned to the same Variant throughout the duration of a given A/B test, even if they exit and re-enter the test multiple times.
