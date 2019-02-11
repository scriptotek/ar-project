---
layout: post
title:  "Experiences with Wikitude"
author: kyrretl
date:   2019-01-17 18:15:00
categories: AR web WebXR javascript
---

![Wikitude Studio](https://scriptotek.github.io/ar-project/assets/wikitude_studio.png "Images of book covers and location targets in Wikitude Studio")
Experiences (both positive and negative) when creating an AR app with Wikitude in a libary setting.
<!-- more -->

In this section, we go through the experiences we had when developing the AR prototype specifically with Wikitude, being the platform we decided on. Note that we would probably have had similar with Wikitude as with other platforms (such as Vuforia), since many of the challenges are non-platform specific. We recommend you first read the blog post on [Designing the prototype](https://scriptotek.github.io/ar-project/blog/2019/01/17/wikitude.html) as an intro to our experiences with Wikitude.

##Initial evaluation

As described in the blog post on [evaluating the different platforms](https://scriptotek.github.io/ar-project/platform-evaluation/), we made the following evaluation of Wikitude after some initial testing:

**Benefits and drawbaks** 
* Functionality: Well develped, stable, fast and reliable. Does not have meshing or mesh cloud, but has image based scence cloud with image, scence and object recognition.
* Accessibility: Has a javsacript API for communication SDK for Android (among others).
* Ease of implementation: Well documented with examples and some video tutorials, blogs and forum.
* Price: Free educational license, limited to one Android and one iPhone (in our case only Android as we did not have the opportunity to test with iPhone).

Since no platform (as of october 2018) had a properly functioning mesh cloud, which really is a requirement for proper indoor localization without resorting to some kind of beacon technology, our other most important criterias were price and a programming language that we're familiar with. As Wikitude both offered a free license for educational institutions and also a Javascript SDK, we ended up developing the prototype with Wikitude.

##Wikitude Studio

[Wikitude studio](https://www.wikitude.com/external/doc/documentation/studio/introduction.html#introduction-to-studio) is a site for developers to upload images they want as targets (what the AR-app reacts to), in our case this would be images of book covers.

Since the collections we wanted to include in our prototype typically has thousands of books, the largest having 10 000, so we wondered if we could upload these images to Wikitude studio by bulk from our vendor (ExLibris or ProQuest). Wikitude's educational license allows us to have up to 50 000 images so this seemed very possible. 

We tested first by uploading a couple of covers from our vendor to check how the prototype app responded when shown the physical books.
We uploaded first the image provided by our vendor, but this image had too low quality (128 pixels x 199 pixels, Wikitude recommends between 500 and 1000 px). Since we couldn't user our vendor's image, we downloaded a similar higher resolution from a web search just to test. 

![Sapiens inital book cover images](https://scriptotek.github.io/ar-project/assets/sapiens_bad_covers.png)






The 

##Javascript SDK



