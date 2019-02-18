---
layout: page
title: The finalized app
permalink: /finalized-app/
---


![All targets used in AR app](https://scriptotek.github.io/ar-project/assets/all_targets.png "All targets used in AR app")

Here we describe the final version of the AR Libray Project's app and its practical use in the library.

## The physical items used in the app
We took pictures of covers of four books, and created three location targets for three collections.

### The books
![All books used in app](https://scriptotek.github.io/ar-project/assets/all_covers.png "All books used in app")

The books we chose are books from three different collections, sharing at least one subject heading.
These books are:

Title | Author | Collection | Subject headings
------ | ------ | ---------- | ----------------
Sapiens | Yuval Noah Harari | 42 Collection | Human evolution, Society, Human behavior
Homo Deus | Yuval Noah Harari | 42 Collection | Futurology, Society, Human behavior
Brave New World | Aldous Huxley | Scifi Collection | Futurology, Society, Human behavior
Human Biology | Sara Stinson *et al.* (editors) | Main Book Collection|Human evolution, Human genetics, Human biology

### The collections
![All AR location targets used in the app](https://scriptotek.github.io/ar-project/assets/AR-lighthouses_corrected.png "All AR location targets used in the app")

These targets which we called AR Light Houses are located next to a collection which can be scanned to get collection information, book shelf location and direction to other collections.

This a typical placement of an AR Light House next to the 42 Collection:
![Typical placement of an AR Light House next to the 42 Collection](https://scriptotek.github.io/ar-project/assets/42-collection-lighthouse-small.png "Typical placement of an AR Light House next to the 42 Collection")

The collections the books were chosen from are:

Collection name | Approx. size | Type
--------------- | ---- | ----
42 Collection | 5000 | Popular science, philosphy of science, history of science
Main Book Collection| 8000 | Natural science
SciFi Collection | 10000 | Science fiction

## Overview of app functionality

**The main functionality of the app is to give the user:**

1. AR collection information:
   1. Decription of collection
   2. Wayfinding to collection of interest
   3. Shelf location of book of interest
2. AR Book information:
   1. Sleeve description
   2. Related books - similar books that share at least one subject heading
   3. More books - more books from same author
   4. Video (as file on server or from Youtube)
   5. Wikipedia 

**Expected procedure using the app is as follows:**

1. User gets information about the collection from an AR Light House:
![Get info about collection](https://scriptotek.github.io/ar-project/assets/app_desc_1.png "Scans AR Light House to get info about collection")
2. After finding a book of interest, the user scans the book with the app and gets AR metadata information:
![Get info about collection](https://scriptotek.github.io/ar-project/assets/app_desc_2.png "Finds and scans book for metadata related to book")
3. After finding a related book from the AR metadata, the user scans the AR Light House again and gets directions to the location of related book:
![Get info about collection](https://scriptotek.github.io/ar-project/assets/app_desc_3.png "Gets waypoint for book located in another collection")
4. Arriving at the collection, the user scans this collection's AR Light House and gets shelf location of related book:
![Get info about collection](https://scriptotek.github.io/ar-project/assets/app_desc_4.png "Gets shelf location of book")

## Demonstration video
We have a [Youtube video](https://www.youtube.com/watch?v=jSfdG_45iqA) demonstrating actual use of the prototype.

## Screenshots
These are four screenshots of the functioning prototype:

1) Scanning book cover displaying metadata available for the book (Sapiens by Yuval Harari), 2) Browsing related books, 3) Getting directions to a different collection containing related book (Brave New World is in the Scifi Collection) and 4) Arriving at the Scifi Collection getting information about the collection and shelf location of book:
![Screenshost of app](https://scriptotek.github.io/ar-project/assets/screenshot_1.png "Screenshost of app")


## Blog
* Read our [blog](https://scriptotek.github.io/ar-project/blog/) on how we developed the app.

## Downloads
* Download the [app](https://github.com/scriptotek/ar-project-app/blob/master/README.md)
* Download [target images](https://scriptotek.github.io/ar-project/assets/targets.zip) (the book covers and AR Light Houses)
