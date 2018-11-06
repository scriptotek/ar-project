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

**Benefits** 
* Functionality: Support for metadata and wayfinding through marker images
* Accessibility: Can be directly implemented in browser, works on 'any' phone and pad
* Ease of implementation: Javascript based can be implemented and modified relatively easily, with a somewhat active online community
* Price: Free - open source

**Drawbacks**
* Functionality: A bit unstable, jittery augmentation which sometimes disappear altogether. Requires the markers to be very simple in detail and color, with high contrast, so for example a book cover cannot be used as a marker. There will likely be more performance issues when several markers are visible at the same time, which is required for continuous wayfinding. No meshing. No cloud.
* Accessibility: Performance varies between devices, predicted to give unpredictable outcomes when scaled up with more complex code which can in worst case lead to non-functionality on some devices. 

[Source on github](https://github.com/jeromeetienne/AR.js/blob/master/README.md)

[On our blog](blog/2018/11/05/arjs.html)


### WebXR

### 6d.ai

### Vuforia

### Wikitude

### ARCore

### EasyAR

# Blog

[There's a blog](blog/) too, which we upate with current findings

