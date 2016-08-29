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

As a conclusion to ICS 111, Introduction to Computer Science I, our class was required to create an open ended project in groups of 4. The projects had to include the object-oriented programming and Java skills we collected over the semester, including basics like seperate classes, an array (or ArrayList), and reading from/ writing to a file. My group decided to create a karaoke machine, which main ability was to present lyrics in time to a song so that a user may sing to the song using the displayed words. After the song is completed, a randomized score was displayed and organized into the statistics. The machine consisted of a home screen, from which the user may access a statistics screen, a song selection screen, and a random song. From the song selection screen, the user could choose 1 of 8 songs to sing along to.

In this project, I was in charge of storing and displaying the statistics along with creating lyrics timings to 2 songs. I also programmed the buttons so that the other screens would load when they were pressed. For the statistics, I had the random number generated at the end of a song and written to a file. When the statistics page was accessed, the numbers stored in the file were placed in an ArrayList and sorted via bubble sort. Then, only the top 10 scores were displayed on the screen. For the lyrics, the strings were simply translated and hidden using EZ commands, with wait functions to accomodate for timing. 
