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
* Functionality: A bit unstable, jittery augmentation which sometimes disappears altogether. Requires the markers to be very simple in detail and color, with high contrast, so for example a book cover cannot be used as a marker. There will likely be more performance issues when several markers are visible at the same time, which is required for continuous wayfinding. ARjs has no mesh mapping, and no cloud persistance.
* Accessibility: Performance varies between devices, predicted to give unpredictable outcomes when scaled up with more complex code which can in worst case lead to non-functionality on some devices. Future code maintenance might be reduced when WebXR takes over.

**Evaluation**
Possible to develop both wayfinding and metadata on this platform, but might put off users due to performance issues.
Also, might suffer lack of future maintenance support when WebXR arrives.
In short, we perfer looking for other solutions.

[Source on github](https://github.com/jeromeetienne/AR.js/blob/master/README.md)

[On our blog](blog/2018/11/05/arjs.html)


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


[WebXR Device API](https://immersive-web.github.io/webxr/)

[WebXR channel on Slack](https://webvr.slack.com/messages/C3GC60HHN/)
 
[Augmented reality samples](https://immersive-web.github.io/webxr-samples/proposals/)
 
[Google XR-demo](https://web-education-ar-demo.appspot.com/) - [Information on setup for the XR-demo] (https://developers.google.com/web/updates/2018/06/webar-chacmool)

[On our blog](blog/2018/11/07/webxr.html)


### 6d.ai

### Vuforia

### Wikitude

### ARCore

### EasyAR

### Other resources

[WebAR channel on slack WebVR](https://webvr.slack.com/messages/C3GC60HHN/)

# Blog

[We have a blog](blog/) which we upate with current findings and tests

