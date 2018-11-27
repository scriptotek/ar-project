---
layout: default
title: The Library AR Project
lang: en
ref: home
---

The Library AR Project is a collaborative effort from Mandal public library and Oslo Science Library to find practical application for Augmented Reality usage in a library and see which current available platforms are suitable. If it is practically feasible, we will develop a prototype app with real life usability.

[Read more about the project](about/)

# Testing of different platforms
As of October 2018, there are many available platforms, but not all are as suitable for AR development in a library setting.

## Criteria for choice of platform
The main criteria we use to evaulate the different platforms are:

* Functionality
* Accessibility
* Ease of implementation
* Price

**Functionality**
We see *wayfinding* and *metadata* as the main areas of functionality for AR in a library setting.

**Accessibility**
AR in a public library setting should be easily accessible on many devices. We look both at mobile app based solutions as well as browser integrated solutions.

**Ease of implementation**
Since development is local, the ease of which the different applications can be tested and turned into a workable prototype app is important

**Price**
The Library AR Project will only implement solutions that either offer possibilities of free trials (for off-the-shelf applications) or is free open source. We document the different pricing (or lack of) and evaluate the gains from the pricing.

## Specific platforms tested


### AR.js

`javascript` `browser compatible` `multi device`

AR.js is an open source javascript based development

**Benefits** 
* Functionality: Support for metadata and wayfinding through marker images
* Accessibility: Can be directly implemented in browser, works on 'any' phone and pad
* Ease of implementation: Javascript based, can be implemented and modified relatively easily, with a somewhat active online community
* Price: Free - open source

**Drawbacks**
* Functionality: A bit unstable, jittery augmentation which sometimes disappears altogether. Requires the markers to be very simple in detail and color, with high contrast, so for example a book cover cannot be used as a marker. There will likely be more performance issues when several markers are visible at the same time, which is required for continuous wayfinding. ARjs has no mesh mapping, and no cloud persistence.
* Accessibility: Performance varies between devices, predicted to give unpredictable outcomes when scaled up with more complex code which can in worst case lead to non-functionality on some devices. Future code maintenance might be reduced when WebXR takes over.

**Evaluation**
Possible to develop both wayfinding and metadata on this platform, but might put off users due to performance issues.
Also, might suffer lack of future maintenance support when WebXR arrives.
In short, we perfer looking for other solutions.

**Sources**
* [Source on github](https://github.com/jeromeetienne/AR.js/blob/master/README.md)
* [On our blog](blog/2018/11/05/arjs.html)


### WebXR

`javascript` `browser compatible` `multi device` `under development` `unstable` `experimental`

The WebXR Device API will be the new W3C standard for web based virtual and augmented reality.

**Benefits and drawbaks** 
* Functionality: Responsive and smooth performance, but unstable due to being under development. Also, Chrome Canary (which is required) is often unstable and/or crashes when used with WebXR.
* Accessibility: Currently very low accessiblity, Android Origo 8.0 or later, ARCore and only Chrome Canary can be used and a couple of flags need to be set (see blog post below for details). 
* Ease of implementation: Javascript based, can be implemented and modified relatively easily, there are some good working examples of the API being used
* Price: Free - open source

**Evaluation**
The WebXR Device API is the future of web based AR, but since it is in its very infancy with currently very low accessibility it is not suitable for the Library AR project.

**Sources**
* [WebXR Device API](https://immersive-web.github.io/webxr/)
* [WebAR channel on Slack](https://webvr.slack.com/messages/C3GC60HHN/)
* [Augmented reality samples](https://immersive-web.github.io/webxr-samples/proposals/)
* [Google XR-demo](https://web-education-ar-demo.appspot.com/)
* [Information on setup for the XR-demo](https://developers.google.com/web/updates/2018/06/webar-chacmool)
* [On our blog](blog/2018/11/07/webxr.html)

### 6d.ai

`C++/C#` `mesh` `cloud` `persistance` `app based` `iOS` `under development` `unstable` `Unity`

[6d.ai](https://www.6d.ai/) is a new company creating a "6D Reality Platform" specializing on mesh based AR with cloud based persistence. Currently only app based (no browser implementation available) and at the moment their platform only supports iOS, with Android support scheduled for 2019.

**Benefits and drawbaks** 
* Functionality: Responsive and smooth performance, but can be somewhat unstable due to being under development.
  Has realtime device based meshing with object occlusion and cloud storage for persistence.
* Accessibility: Currently very low accessiblity, only Apple products with a variety of iPhone support, but only for quite new iPads (down to iPhone 7, iPad Pro and iPad 2018 (6th Gen). Android support is planned for 2019, but here will also quite new phones be required.
* Ease of implementation: Expert knowledge required: Experience with C++/C# iOS native app development and experience with Unity or SceneKit
* Price: Beta has free siqn up - will expected to be a paid subscription service

**Evaluation**
6D Reality Platform is the most promnising AR platforms out there, with many features essensial for AR in a library contex such as meshing and cloud persitence. It also hs the added benefit of object occlusion which enhances user experience. For our project it is unfortunately not come far enough for testing (ie. Android support not ready this year) and also does not support javascript/browsers. In addition, the requirement of experience with Unity represents a developmental overhead.

**Sources**

* [Product description](https://www.6d.ai/product/)
* [Developer pages](https://dashboard.6d.ai/user/dashboard/?view=home)
* [6d.ai developer channel on Slack](https://6d-developers.slack.com)
 
### EasyAR


### ARCore

`app based` `iOS/Android` `Unity` `under development`

[ARCore](https://www.wikitude.com/) is Googles platform for developing apps for AR. Unlike Apples ARKit, ARCore works on #both# iOS and Android.

**Benefits and drawbaks** 
* Functionality: Quite stable although being under development. Most apps that use AR (such as IKEA and Amazon) uses ARCore. Lacks support for persistence (no more than 7 days), see source 'Blog testing ARCore' below for details. Centered around hit boxes and anchors, not mesh.
* Accessibility: Only on apps, but supports both iOS and Android.
* Ease of implementation: Quite easy to implement with Unity, but requires knowledge of Unity to get past basic functionality. Decent coverage on tutorials and examples.
* Price: Free - open source

**Evaluation**
Due to lack of persistence (which is needed for stable wayfinding) ARCore is somewhat less applicable for us than both Vuforia and Wikitude (see below). Aside from that, ARCore with Unity is developed and implemented in much the same manner as with Vuforia/Wikitude.

**Sources**

[ARCore quickstart for Android](https://developers.google.com/ar/develop/unity/quickstart-android)
[Blog testing ARCore](https://medium.com/inborn-experience/why-google-cloud-anchors-doesnt-deliver-on-the-hype-e5d0a3fe704d)

### Vuforia

`app based` `iOS/Android` `Unity`

[Vuforia](https://www.vuforia.com/) is one of the most well known app based platforms for AR. Although we did research on Vuforia, we did not test the platform. The reason is that Wikitude, which is very similar, has a free offer for public institutions with more functionalities than Vuforia. Apart from that Vuforia seems to have somewhat more examples of functional apps and code that Wikitude has.

**Benefits and drawbaks** 
* Functionality: Well develped, stable, fast and reliable. Does not have meshing or mesh cloud, but has image based scence cloud with scence and object recognition.
* Accessibility: No support for web/javascript, needs iOS or Android apps.
* Ease of implementation: Well documented with examples and tutorials, experience with Unity is needed, but because of good tutorials the overhead is reduced substantially.
* Price: One-time withot cloud support: $499. Monthy cloud-based subscription: $99. Check link below for details and price updates

**Evaluation**
We chose to use Wikitude instead, see below, the evaluation is very similar.

**Sources**
* [Vuforia pricing](https://developer.vuforia.com/vui/pricing)
* [Vuforia for developers](https://developer.vuforia.com/support)
* [Vuforia Youtube-howto](https://www.youtube.com/watch?v=MtiUx_szKbI)

### Wikitude

`app based` `javascript` `iOS/Android` `Unity`

[Wikitude](https://www.wikitude.com/) .

**Benefits and drawbaks** 
* Functionality: .
* Accessibility: .
* Ease of implementation: .
* Price:  Check link below for details and price updates

**Evaluation**


**Sources**



### Other resources

[Wepage comparing different AR platforms](http://socialcompare.com/en/comparison/ar-frameworks-388frkga)


# Blog

[We have a blog](blog/) which we upate with current findings and tests

