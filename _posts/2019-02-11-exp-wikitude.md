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

In this section, we go through the experiences we had when developing the AR prototype specifically with Wikitude, being the platform we decided on. Note that we would probably have had similar issues with other platforms (such as Vuforia) as with Wikitude, since many of the challenges are non-platform specific. We recommend you first read the blog post on [Designing the prototype](https://scriptotek.github.io/ar-project/blog/2019/01/17/wikitude.html) as an intro to our experiences with Wikitude.

## Initial evaluation

As described in the blog post on [evaluating the different platforms](https://scriptotek.github.io/ar-project/platform-evaluation/), we made the following evaluation of Wikitude after some initial testing:

**Benefits and drawbaks** 
* Functionality: Well develped, stable, fast and reliable. Does not have meshing or mesh cloud, but has image based scence cloud with image, scence and object recognition.
* Accessibility: Has a javsacript API for communication SDK for Android (among others).
* Ease of implementation: Well documented with examples and some video tutorials, blogs and forum.
* Price: Free educational license, limited to one Android and one iPhone (in our case only Android as we did not have the opportunity to test with iPhone).

Since no platform (as of october 2018) had an adequate mesh cloud for our needs, which really is a requirement for proper indoor localization without resorting to some kind of beacon technology, our other most important criterias were price and a programming language that we're familiar with. As Wikitude both offered a free license for educational institutions and also a Javascript SDK, we ended up developing the prototype with Wikitude.

## Wikitude Studio

[Wikitude studio](https://www.wikitude.com/external/doc/documentation/studio/introduction.html#introduction-to-studio) is a site for developers to upload images they want as targets (what the AR-app reacts to), in our case this would be images of book covers.

### Working with book covers

Since the collections we wanted to include in our prototype typically has thousands of books, the largest having 10 000, we wondered if we could upload these cover images to Wikitude studio by bulk from our vendor (ExLibris or ProQuest). Wikitude's educational license allows us to have up to 50 000 images in Wikitude Studio. 

We uploaded a couple of covers from our vendor to check how the prototype app responded when shown the physical books.
First we tested the image provided by our vendor, but this image had too low quality (128 pixels x 199 pixels, Wikitude recommends between 500 and 1000 px). Since we couldn't use our vendor's image, we downloaded a similar, higher resolution image from a web search. 

![Sapiens inital book cover images](https://scriptotek.github.io/ar-project/assets/sapiens_bad_covers.png)

The app did not react to the high resolution image at all, and we noticed that it was slightly different than our cover, for example the top text "The Sunday Times Top Ten bestseller" was replaced by "The Million Copy Bestseller" and also the bottom praise text was different.

We managed to find a clear, high resolution replica of our book's cover, but the app still would not respond. In fact, the only way to get the app to recognize the book cover was to take a picture of our physical book (with a camera or phone) and upload this image to Wikitude!

In order to accomodate different lighting situations and maximize the chance of recognition, we took four different images of the book and uploaded these:

![Sapiens manual cover images](https://scriptotek.github.io/ar-project/assets/sapiens_all_real_covers.png)

Fortunately, these images proved to be responsive, and the app quickly reacted to them.

Due to the time requirements capturing and editing four differently lighted images of one single book, we had to give up the idea of testing entire collections and rather limit ourselves to a handful books. As the app is only meant to be a prototype, it didn't really affect our project, but it is obviously rather disheartening for future, larger projects.

### Working with wayfinding

As described in the section on the development of the prototype, we had hoped to be able to use Scence Recognition as a substitute for mesh cloud localization. Unfortunately, Scence Reconition proved to be highly unstable and we had to come up with an image target based solution.

We ended up using image recogntion on three different "AR Light house"-image targets that users would need to scan to get directions.
We made one of these light houses for each collection in the project:

* The Main Book Collection (a collection of all science fields), approx. 8 000 books
* The 42 Collection (a collection of popular science), approx. 5 000
* The Science Fiction collection, approx 10 000 books

![The three AR Light houses](https://scriptotek.github.io/ar-project/assets/AR_lighthouses.png)

The only issue we ran into is that Wikitude renders all images in greyscale, and we initially had the images identical except for the color of the paint on the lighthouse. After adding individual text placed in different areas of the image, the app managed to separate them and correctly identify the corresponding collection.

![AR Light Houses remade](https://scriptotek.github.io/ar-project/assets/AR-lighthouses_corrected.png)

A final note is that we had to print out the light house images and take a picture of them the same way we did for the books with regards to lighting in order for the app to consistently recognize the images. To simply use the image from the computer was not reliable.

## Javascript SDK

For javascript development we downloaded the [Wikitude SDK for Android](https://www.wikitude.com/download-wikitude-sdk-for-android/), the version we worked with was 8.1 (october 2018).
Over all it was quite easy to get out own version up and running, the [documentation](https://www.wikitude.com/external/doc/documentation/latest/android/gettingstartedandroid.html) is good and there is a [reference](https://www.wikitude.com/external/doc/documentation/latest/Reference/JavaScript%20API/index.html) as well.
It basically allows you to program an app entirely in javascript and then package it to an android phone as APK using [Android Studio](https://developer.android.com/studio/).

Here is a good [Youtube tutorial](https://www.youtube.com/watch?v=ux4HbnUjNMc&t=23s) on how to set up Wikitude Android SDK with Android studio.

## Summary
Creating an AR app in a library setting with Wikitude was over all a good experience, but with regards to practical solutions offered by their platform (and other platforms) it is at the moment (fall 2018) not realistic to implement full scale AR in a library today. The main reasons are:

* Unreliable detection of book covers
  * Leads to extensive and unrealistic work load for taking multiple photographs of all books in different lighting conditions.
  * A better AI for recognizing images/items is needed, so that automated adding of target images from API's can be done.
* Lacks proper wayfinding or localization
  * A persistent point cloud mesh is a better solution than having potentially hundreds of target images that users have to get up and close to. 

As side-note on accessibility: A web based platform that can seamlessly be integrated into a web page without having to install an app will ease accessiblity and promt usage, such as Google's [ARCore](https://developers.google.com/ar/) and Apple's [ARKit](https://developer.apple.com/arkit/). Currently (as of late 2018) they have not come far enough for this purpose, but might well have in a few years.






