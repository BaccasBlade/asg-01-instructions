# Assignment 01 - Milestone 02

**Due October 13 (W) @ 9 PM**

## Overview

With a number of weeks of JS under your belt, you're now in a position to make your SPA a bit more interactive.

We don't want to get too far ahead of ourselves, though - much of the assignment talks about APIs:

- the Country List API
- the City List API
- the Images API
- the Languages API
- the Google Maps API

This is a bit of a problem for us, since we haven't yet covered the topics of Chapter 10 which would help us consume these APIs!

This isn't a BIG problem, though - there's always a way around temporary setbacks like this!

### Getting 'round the prob

For the Country, City, Images, and Languages APIs, we'll bring the data typically delivered via an API request into our app using JSON data in files as covered in Exercise 8.14 in Lab 8 and Section 8.7.4 in the text.

For the Google Maps API - it's not part of this milestone's requirements. You can just use a placeholder of some sort there. That was easy!

#### Cleaning Up

Data gets dirty. When you're making your faux-API files, be careful of things like nested double quotes - they're going to cause problems with your `JSON.parse` calls.

For example, if you pull down all the countries via https://www.randyconnolly.com/funwebdev/3rd/api/travel/countries.php?iso=ALL, you get a few of those nested suckers, like this one in the entry for Bahamas:

> "The Bahamas, officially the Commonwealth of the Bahamas, is a country consisting of more than 3,000 islands, cays and islets in the Atlantic Ocean, north of Cuba and Hispaniola (the Dominican Republic and Haiti), northwest of the Turks and Caicos Islands and southeast of the US state of Florida. Its capital is Nassau on the island of New Providence. Geographically, the Bahamas lie in the same island chain as Cuba, Hispaniola and the Turks and Caicos Islands; **the designation of "Bahamas" usually** refers to the country and not the geographic chain. The country's population, numbering around 354,000, lives on a land area of 13,939 km2 (5,382 sq mi)."

Depending on your Chrome extensions, you might see something like this instead:

> "...Islands; **the designation of `\"Bahamas\"` usually** refers to ..."

In either case, see that bolded part? That's gonna make your JSON.parse unhappy. And that will make you unhappy. And that will make me unhappy.

You'll need to escape those things properly using a double-backlash (`\\"`). So in the js/json file you create, make sure the previous Bahamas example becomes:

> "...Islands; **the designation of \\\\"Bahamas\\\\" usually** refers to ...."

Use your tools wisely - find and replace is your friend here!

## Your Mark

Just like milestone 1:

- if you meet **all** the requirements below, your group's mark is 100%
- if you are missing **one** of the requirements below, your group's mark is 50%
- if you are missing **two or more** of the requirements below, your group's mark is 0%

## Non-Perkable Requirements

These requirements **cannot** be postponed through use of a Perk:

- [ ] the web page is hosted through Netlify

- [ ] the HTML links to at least one external JS file that contains the JS necessary to complete the Perkable Requirements below.

  > _Though not necessary for this milestone, you will want to start thinking of reasonable ways to split up your JS into separate files - putting all your JS in one file will be unacceptable for your final submission of this assignment!_

- [ ] the `README.txt` file contains the names of the students who completed this milestone and the URL Netlify has provided for your app (it'll look like `https://blahblahblah.netlify.app`)

- [ ] **all** JS must be in external files. No inline or embedded JS can be used.

## Perkable Requirements

These requirements **can** be postponed through use of a Perk.

By spending one Perk, you can extend your submission deadline **for a single requirement** until **October 8 (F) @ 9 PM**.

> _Yes, you can spend multiple Perks to extend deadlines for multiple requirements._  
> _No, you cannot spend multiple Perks to extend a single deadline longer than 48 hours._ > _Yes, you probably want to save a few Perks for the next Milestone...and your midterm._

### requirements from milestone 1 that are still in effect

- [ ] all CSS is declared valid by the [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/)

- [ ] all HTML is declared valid by the [W3C Markup Validation Service](https://validator.w3.org/)

- [ ] the **Default View** is presented when a user lands on the page

  - [ ] if the screen size has a width in the 320px to 425px range, a reasonable mobile layout is shown
  - [ ] if the screen size has a width >=1024 px, either the layout shown on the assignment writeup is presented, or if you've gotten approval for a different layout, that desktop layout is shown

- [ ] the travel photos section of the Default View must follow these requirements:

  - [ ] `<picture>` elements must be used, and
  - [ ] at mobile size, the images should be 75px squares, and
  - [ ] at desktop size, the images should be 150px squares, and
  - [ ] all images are hosted on Cloudinary, and
  - [ ] all images must be dynamically generated via Cloudinary URLs

- [ ] you must have a layout that uses CSS grid and/or flexbox; no floats or tables can be used

### new requirments for milestone 2

- [ ] the place where the Google Map should appear should display a placeholder of some kind, like an image from a placeholder service (like placeholder.com)

- [ ] when the user arrives at the page, the Country Cist section of the Default View must display a alphabetically sorted list of all country names

- [ ] **at least one** country filter (name, image available, continent) must be working and displaying results in alphabetical order:

  - [ ] a properly-working **name filter** will show only the names of those countries that start with the letters (case-insensitive) that are entered by the user. This list must change each time a key is pressed.
  - [ ] a properly-working **image available** filter will only show the names of those countries that have images available. (There should be 21 such countries.)
  - [ ] a properly-working **continent** filter will only show the names of those countries from continents that have been selected by the user. Remember that multiple such continent selections can be active: for example, if the user selects Antarctica **and** Oceania, there should be 32 country names displayed.

- [ ] clicking on a country name in the Country List section must cause at least the name of the country to appear in the Country & City Details section, though you can show further info if you want

- [ ] clicking on a country name in the Country List section must cause a change in the Travel Photos section:

  - [ ] if there are no photos available for the selected country, then a reasonable message should be shown, or
  - [ ] if there are photos available for the selected country, all of them should be displayed.

## A Demonstration

I **_was_** originally going to show another demo like I did for milestone 1, but then reckoned such a screencast would influence your work more than I wanted. Being able to picture in your mind what a client is (probably) thinking is a necessary skill to develop, so we might as well develop it.

This might seem like a cop-out, but it truly is not.

Naturally, if you have any questions about these requirements, I am very happy - honestly! - to chat with you about them!
