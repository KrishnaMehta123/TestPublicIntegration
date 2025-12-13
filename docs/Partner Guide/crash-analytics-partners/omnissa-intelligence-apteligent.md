---
title: Omnissa Intelligence (Apteligent)
excerpt: Crash Analytics Partner
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

[Omnissa Intelligence (Apteligent)](http://www.apteligent.com/), a mobile application platform, helps build better and faster applications by providing application performance insights. The CleverTap and Omnissa Intelligence (Apteligent) integration sends crash events to CleverTap. This information helps you with the following:

* Create audiences of application users to engage through in-app and push messages. For example, apologize for a crash instance and let the users know that a fix is on its way.
* Detect if the application is having an outage and stop sending push notifications.

# How does it work?

The Omnissa Intelligence (Apteligent) SDK creates a notification that is triggered when the SDK detects a crash. This notification is fired when an iOS user loads the app after a crash. The notification contains the following information:

* Crash Name: The name of the crash (i.e., NSRangeException).
* Crash Reason: More details on why the crash occurred (i.e., "\*\*\* -[__NSArrayM objectAtIndex:]\: index 18446744073709551615 beyond bounds for empty array")
* Crash Date: The date and time when the crash occurred.

# Integrate Omnissa Intelligence (Apteligent) with CleverTap

This process involves the following two major steps:

1. Register an Observer\
   To register an observer, add the following lines of code:

```objectivec
[[NSNotificationCenter defaultCenter] addObserver:self
                                         selector:@selector(crashDidOccur:)
                                             name:@"CRCrashNotification"
                                           object:nil];
```

> 📘 Note
>
> Ensure that you add this code before you initialize Omnissa Intelligence (Apteligent) SDK.

2. Send an Event Upon Notification

Log the crash event and update the CleverTap user attributes with data from Omnissa Intelligence (Apteligent) crash reporting analytics after receiving the notification. 

To do so, add the following lines of code:

```objectivec
- (void) crashDidOccur:(NSNotification*)notification {
NSDictionary *crashInfo = notification.userInfo;
NSString *crashName = crashInfo[@"crashName"]];
NSString *crashReason = crashInfo[@"crashReason"];
NSDate *crashDate = crashInfo[@"crashDate"];
// CleverTap
[[CleverTap sharedInstance] recordEvent:@"ApteligentCrashEvent" withParameters:crashInfo];
}
```
