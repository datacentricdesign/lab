---
layout: post
comments: false
title:  "Releasing a Flutter App"
date:   2020-03-24 13:30:00 +0000
description:
main-class: 'tutorial'
color:
author: /staff_members/elvis
tags:
- platform
- app
- release
- Android
- iOS
categories:
twitter_text:
introduction:
---

First, have an [apple](https://developer.apple.com/programs/) and [google developer](https://support.google.com/googleplay/android-developer/answer/6112435) account, with the right setups.



## Versioning

Then go the the root project folder and configure the versioning:

Go to the pubspec.yaml in the root of the flutter project,  and edit the versioning/building of the app (in the version parameter):

 * The version number (0.2.0)  in this case, where you can edit the the current app version
 * The build number (after the +) - you just need to increase this for the app bundle.

![image-20200324134508781](/assets/img/posts/pubspec.png)



Now we can build our final executable and release them in the specific stores: 

## Android

You can find the full official guide [here.](https://flutter.dev/docs/deployment/android)

The recommended executable in Android is in the format of an AppBundle:

#### Create an app bundle 

From the command line in project's path, (after you select the release variant in the build submenu - by default "release" should be fine):

```bash
flutter build appbundle
```

The release bundle for your app is created at `/build/app/outputs/bundle/release/app.aab`.

You can now upload this .aab file in [google play](https://developer.android.com/studio/publish/upload-bundle). You can use the google play launch guide to see all checklists and other further [details.](https://developer.android.com/distribute/googleplay/start)

## iOS

You can find the full official guide [here.](https://flutter.dev/docs/deployment/ios)

Firs of all, register your app with [App Store Connect](https://developer.apple.com/support/app-store-connect/) 



### Register a Bundle ID

Every iOS application is associated with a Bundle ID, a unique identifier registered with Apple. To register a Bundle ID for your app, follow these steps:

1. Open the [App IDs](https://developer.apple.com/account/ios/identifier/bundle) page of your developer account.
2. Click **+** to create a new Bundle ID.
3. Enter an app name, select **Explicit App ID**, and enter an ID.
4. Select the services your app will use, then click **Continue**.
5. On the next page, confirm the details and click **Register** to register your Bundle ID.

### Create an application record on App Store Connect

Next, you’ll register your app on App Store Connect:

1. Open [App Store Connect](https://appstoreconnect.apple.com/) in your browser.
2. On the App Store Connect landing page, click **My Apps**.
3. Click **+** in the top-left corner of the My Apps page, then select **New App**.
4. Fill in your app details in the form that appears. In the Platforms section, ensure that iOS is checked. Since Flutter does not currently support tvOS, leave that checkbox unchecked. Click **Create**.
5. Navigate to the application details for your app and select **App Information** from the sidebar.
6. In the General Information section, select the Bundle ID you registered in the preceding step.

For a detailed overview, see [Add an app to your account](https://help.apple.com/app-store-connect/#/dev2cd126805).



### Create a build archive

In this step, you’ll create a build archive and upload your build to App Store Connect.

During development, you’ve been building, debugging, and testing with *debug* builds. When you’re ready to ship your app to users on the App Store or TestFlight, you’ll need to prepare a *release* build.

On the command line, follow these steps in your application directory:

1. Run `flutter build ios` to create a release build (`flutter build` defaults to `--release`).
2. To ensure that Xcode refreshes the release mode configuration, close and re-open your Xcode workspace. For Xcode 8.3 and later, this step is not required.

In Xcode, configure the app version and build:

1. In Xcode, open `Runner.xcworkspace` in your app’s `ios` folder.
2. Select **Product > Scheme > Runner**.
3. Select **Product > Destination > Generic iOS Device**.
4. Select **Runner** in the Xcode project navigator, then select the **Runner** target in the settings view sidebar.
5. In the Identity section, update the **Version** to the user-facing version number you wish to publish.
6. In the Identity section, update the **Build** identifier to a unique build number used to track this build on App Store Connect. Each upload requires a unique build number.

Finally, create a build archive and upload it to App Store Connect:

1. Select **Product > Archive** to produce a build archive.
2. In the sidebar of the Xcode Organizer window, select your iOS app, then select the build archive you just produced.
3. Click the **Validate App** button. If any issues are reported, address them and produce another build. You can reuse the same build ID until you upload an archive.
4. After the archive has been successfully validated, click **Distribute App**. You can follow the status of your build in the Activities tab of your app’s details page on [App Store Connect](https://appstoreconnect.apple.com/).

You should receive an email within 30 minutes notifying you that your build has been validated and is available to release to testers on TestFlight. At this point you can choose whether to release on TestFlight, or go ahead and release your app to the App Store.

For more details, see [Upload an app to App Store Connect](https://help.apple.com/xcode/mac/current/#/dev442d7f2ca).



### Release your app to the App Store

When you’re ready to release your app to the world, follow these steps to submit your app for review and release to the App Store:

1. Select **Pricing and Availability** from the sidebar of your app’s application details page on [App Store Connect](https://appstoreconnect.apple.com/) and complete the required information.
2. Select the status from the sidebar. If this is the first release of this app, its status will be **1.0 Prepare for Submission**. Complete all required fields.
3. Click **Submit for Review**.

Apple will notify you when their app review process is complete. Your app will be released according to the instructions you specified in the **Version Release** section.

For more details, see [Distribute an app through the App Store](https://help.apple.com/xcode/mac/current/#/dev067853c94).

