# Assignment 01 - Milestone 01

**Due September 22 (W) @ 9 PM**

**Worth 5% of your final grade**

## Your Mark

Straightforward stuffs:

- if you meet **all** the requirements below, your mark is 100%
- if you are missing **one** of the requirements below, your mark is 50%
- if you are missing **two or more** of the requirements below, your mark is 0%

## Non-Perkable Requirements

These requirements **cannot** be postponed through the use of Perks:

- [ ] the web page is hosted through Netlify and connected to your GitHub Classroom Assignment

- [ ] there is _some kind_ of content visible when you go to the web page

- [ ] the landing page's HTML links to an external JS file that displays a (hopefully amusing) message to console

  > **clarification:** _while the general requirements in [assignment-01.md] state that you must have "just a single HTML page", this does not mean you don't need additional types of files, like CSS and JS files_

- [ ] the `README.txt` file contains the name of the student who completed the milestone and the URL Netlify has provided for your app (it'll look like `https://blahblahblah.netlify.app`)

## Perkable Requirements

These requirements **can** be postponed through use of Perks.

By spending one Perk, you can extend your submission deadline **for a single requirement** until **September 24 (F) @ 9 PM**.

> _Yes, you can spend multiple Perks to extend deadlines for multiple requirements._  
> _No, you cannot spend multiple Perks to extend a single deadline longer than 48 hours._  
> _Yes, you probably want to save a few Perks for the next Milestone...and your midterm._

- [ ] all CSS on the site is declared valid by the [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/)

- [ ] all HTML on the site is declared valid by the [W3C Markup Validation Service](https://validator.w3.org/)

- [ ] the **Default View** is presented when a user lands on the page

  - [ ] if the screen size has a width in the 320px to 425px range, a reasonable mobile layout is shown
  - [ ] if the screen size has a width >=1024 px, either the layout shown on the assignment writeup is presented, or if you've gotten approval for a different layout, that desktop layout is shown

    > _Note that the behaviour of your app under 320px and between 426px and 1023px is not being evaluated. This is a nod to time/sanity limitations and not something you could get away with if you were doing this for a living!_

- [ ] every section of the layout must be very clearly distinguishable and labelled (except for the travel photos section, which will have images in it)

- [ ] you must have a layout that uses CSS grid and/or flexbox; no floats or tables can be used

- [ ] the travel photos section of the Default View must have 7 images; you can use any of the travel images you like - you can even use the same one repeatedly - but

  - [ ] `<picture>` elements must be used, and
  - [ ] there must be at least 2 different images used, and
  - [ ] at mobile size, the images should be 75px squares, and
  - [ ] at desktop size, the images should be 150px squares, and
  - [ ] all images are hosted on Cloudinary, and
  - [ ] all images must be dynamically generated via Cloudinary image transformations

## A Demonstration

A demo is worth a thousand checkpoints, so here's a video of me "marking" a sample assignment I made for milestone 1: [walkthrough [17:55]](https://youtu.be/c_Vxsh_AN_s)

## Submission Process

There's a screencast [22:08] of the process here: https://youtu.be/iSiFZ0Vt3jU

If you're comfortable making branches and getting them up to GitHub, here's the process in a nutshell:

1. Set Netlify up to deploy all branches pushed to your GitHub repository
   1. Deploys > Branches > Edit settings => Choose "All" for Branch deploys
2. Create a branch in your local repo called "submit".
3. Push that branch up to GitHub as well.
4. If for whatever reason, you decide you want to submit something else, just repeat the process, naming your branch "submitX", where "X" is some number. (So submit1, submit2, etc). I'll just mark the latest submission.
