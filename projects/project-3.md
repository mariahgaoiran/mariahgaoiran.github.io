---
layout: project
type: project
published: true
image: images/pKara.png
title: Karaoke Machine
permalink: projects/Kara
date: 2015
labels:
  - Java
summary: A karaoke machine game my team developed in ICS 111.
---

<img class="ui image" src="../images/KARA1.png">

As a conclusion to ICS 111, Introduction to Computer Science I, our class was required to create an open ended project in groups of 4. The projects had to include the object-oriented programming and Java skills we collected over the semester, including basics like seperate classes, implementing an array (or ArrayList), and reading/writing a file. My group decided to create a karaoke machine, which main ability was to present lyrics in time to a song so that a user may sing to the song using the displayed words. After the song is completed, a randomized score was displayed and organized into the statistics. The machine consisted of a home screen, from which the user may access a statistics screen, a song selection screen, and a random song. From the song selection screen, the user could choose 1 of 8 songs to sing along to.

<div class="ui small rounded images">
  <img class="ui image" src="../images/KARA2.png">
  <img class="ui image" src="../images/KARA3.png">
</div>

In this project, I was in charge of storing and displaying the statistics along with creating lyrics timings to 2 songs. I also programmed the buttons so that the other screens would load when they were pressed. For the statistics, I had a random integer generated at the end of a song and written to a file. When the statistics page was accessed, a file containing the generated number swas read and placed these integers in an ArrayList. After the integers were sorted using bubble sort, the top 10 scores were displayed on the screen. For the lyrics, the strings were simply translated and hidden using EZ commands, with wait functions to accomodate for timing. 

Being the first programming assignment I've worked on in a group, I have gained experience in cooperative code writing. It was complicated to divide roles equally. But even more difficult was controlling versions without a source control software or website, which in retrospect, would have been an optimal choice. Nevertheless, we found ways to work around this, mainly emailing one person all versions of the code for them to piece together. As I became this person at the end of the project, it helped me practice parsing code along with finding ways to combine them fluidly. For my own code writing, I secured more practice with Java, specifically using FileWriter and Scanner for reading/writing a file.
