---
layout: project
type: project
published: true
image: images/cs-logo-s2.png
title: Collaborative Study (CS)
permalink: projects/CS
date: 2016
labels:
  - Web App
  - Meteor
  - JavaScript
  - HTML
  - Semantic UI
  - Teamwork
  - GitHub
summary: A scheduling app made by my GitHub organization CollaborativeStudy as a project for software engineering.

---

Much of my life as a Computer Science major has been an individual ordeal. For the most part, I studied alone, completed assignments alone, learned alone. Computer Science majors often wrongly assume that their major is one of little social interaction, but in truth many of its aspects require the important communication skills gained through them.

Collaborative Study (CS) was a web app made to change that introverted lifestyle. Using [Meteor](https://www.meteor.com/), a team of three other students and I formed the GitHub organization [CollaborativeStudy](https://collaborativestudy.github.io/) and developed CS, a scheduling app made for ICS students to plan study sessions together. Users receive an editable public profile and gain access to a public calendar of upcoming sessions. They can create study sessions or join existing ones, form study groups, view other profiles and review them, and chat with other online users.

<div class="ui medium images">
  <img class="ui image" src="../images/cs-profile.png">
  <img class="ui image" src="../images/cs-my-calendar.png">
</div>

My hand in development was spread amongst a wide variety of areas:
 1. The study sessions database, our main method of storing the details of sessions which users created. Aside from schema design, I created the form used to validate and add to the database, as well as the page that called this database to display a session's details to users. The latter page allows users to join study sessions as either a "Pro" (short for Professor, a tutor) or "Stud" (short for Student, a tutee), then received additional options based on their choice.
 2. The administrator page, where authorized users chose to allow or delete reviews written by other users, based on their discretion
 3. The website tutorial, a collection of informative messages displayed throughout the site that can be turned on and off through the top bar
 4. The logo's design
 5. Minor fixes, such as the top menu's design and search resets

<div class="ui big images">
  <img class="ui image" src="../images/cs-create-study-session.png">
  <img class="ui image" src="../images/cs-study-session-details.png">
</div>
The two pages that add and read from the sessions database.

Though I am quite proud of the result, developing CS was not without its fair share of troubles. Our team was new to Meteor and thus had to learn how to use MongoDB (the database) and Spacebars (Meteor's templating language). In fact, we were new to the common aspects of web app development, like templates, routers and deployment. A lot of time was put into reading the documentation and attempting implementations of them. Test and then retest, the mantra of all software engineers, had become our mantra as well.

The cooperation between my team for this project would not have been possible without GitHub. Anyone who's used this service knows that it's a real monster to get used to, especially when working in a team of amateurs. It wasn't just about learning the motions of merging or committing, it was understanding what every action was really doing. On multiple occasions, I would run the app off the master branch only to find that another member's merge had deleted all the data from my own. After this project, however, I feel much more comfortable using GitHub.

All in all, this project has been one of the biggest I've done so far. If you have the time, please view the homepage of Collaborative Study at [https://collaborativestudy.github.io/](https://collaborativestudy.github.io/).


