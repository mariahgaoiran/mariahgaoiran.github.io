---
layout: essay
type: essay
title: CollaborativeStudy (CS) Release Notes
date: 2017-01-16
labels:
  - Web App
  - Semantic UI
---
# CollaborativeStudy (CS) Release Notes

[Collaborative Study (CS)](https://mariahgaoiran.github.io/projects/CS) is a scheduling app intended for UH Manoa ICS majors to plan study sessions together. Our [organization](https://collaborativestudy.github.io/) began development of CS in Fall 2016 as a project for our ICS 314 Software Engineering course. The latest updates and planned releases are listed below in reverse chronological order. Releases are scheduled for every two weeks.

# 1.16.17

## Updates
 - *Fixed Calendar Bug:*
 
 Nobody likes when something works half the time. Does a baker want his oven to be hot every other day? Well, we aren't bakers but we don't like half-baked efforts either. That's why we found updating jQuery to 1.11.10 gets rid of all that silly business with the study session creation modal popping up only when it feels like it.

 - *Required first name and last name:*
 
 Future trolls may not be our fans, but we aren't in the business of letting users go willy-nilly with their usernames. (Truthfully, we aren't in any business at all.) Users are now required to enter their first and last names when creating their profile. This will be more convenient when browsing through study sessions. No more wondering if "mjg6" stands for your friend Mike or a complete stranger.

 - *Prevent creating sessions in the past:*
 
 Unfortunately, time travelers aren't on our list of clients either. The calendar now prevents study sessions from being created in a date that has already been passed.

 - *Join session immediately; empty study sessions warning:*
 
 Ever try planning an outing with your friends and it all falls apart within an hour? We understand. However, it isn't pleasant to the eyes to see sessions devoid of participants lying around the public calendar. Users that create a study session must now join the session, with the options of either being a Pro or a Stud. Like before, they may still change their choice or leave entirely on the details page. However, empty sessions are still unacceptable. For those rebels who want to leave sessions empty, we've left a warning in the details page tutorial and next to the "Leave Session" button for them to ponder on their way out. 
 
 - *Fix remove topic:*
 
 The old system for removing topics for a study session was bunk. It expected users to type out the topic to be deleted, in correct spelling and capitalization, no less! It made the developers look stupid for the poor implementation and made users look stupid for making typos. Well, no more. Study session Pros can now simply click the x icon next to the topic to remove it.
 
 - *"Pro" Renamed:*
 
 Out of respect for our professors, we decided to change the definition of "Pro" from "Professor" to "Professional". As much as we'd like to, we can't compare ourselves to be as knowledgeable on the course subject as our actual professors.
 
## Obstacles
MongoDB, for some reason or the other, could not be connected to and left my app hanging when starting up. A simple fix from the interwebs suggested I download and run Mongo seperately, and while this was certainly more tedious, it was not lacking in effectiveness. 

Aside from that, the only other issue appeared when I altered the removing topic function on a study session's detail page. I was having difficulty passing the value of the topic to be removed back and forth between the HTML and JavaScript. Once I understood that the id of the HTML icon tag could be set by and called by JavaScript, I had an easy method for passing the value between them.

# Future Release Updates (1.16.17 - 2.1.17)

### My Page
 - Courses in the bio will be editable and deletable
 - Invalid image paths will result in a default photo
 - Data validation in the "Interests" field to account for special characters
 
### Groups
 - Private and public group system
 - Invitation system for adding group members
 - Quick creation of study sessions with all group members
 - Posts in group page

### Sessions
 - Past sessions automatically deleted
 - Sessions displayed as cards instead of a table
 - Searches are case-insensitive and not limited to a single field
