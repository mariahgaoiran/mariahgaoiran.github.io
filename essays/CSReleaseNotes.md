---
layout: essay
type: essay
title: CollaborativeStudy (CS) Release Notes
date: 2017-03-01
labels:
  - Web App
  - Semantic UI
---
# CollaborativeStudy (CS) Release Notes

[Collaborative Study (CS)](https://mariahgaoiran.github.io/projects/CS) is a scheduling app intended for UH Manoa ICS majors to plan study sessions together. Our [organization](https://collaborativestudy.github.io/) began development of CS in Fall 2016 as a project for our ICS 314 Software Engineering course. The latest updates and planned releases are listed below in reverse chronological order. Releases are scheduled for every two weeks.

# 3.1.17

## Updates
*Landing page makeover (in progress)*

  The attempt to make a plain Jane landing page into something a little less textbook and a lot more wow. Considerations include removing the header and replacing the body with more succinct descriptions.
 
## Obstacles
  There has been slow progress for the past two weeks and I attribute it almost entirely to my time management skills. As a student, there is no excuse for being unable to work on an assignment, despite the number of alternate assignments and midterms that may be occupying one's attentions. That is not to say, however, that I did not prioritize other courses instead of developing Collaborative Study. Thus, I cut a significant amount out of the time I usually spend on CS to focus on an algorithms course and C programming course. But, as the midterms have passed, I will return to dedicated work on this project. Furthermore, I have blocked off time in my schedule (six hours a week split between three days: Tuesday, Friday, and Sunday) for work on CS issues so that I will not fall behind again.
  
    I did have a bit of time to work on the landing page, but its current state is a mad jumble of images in what was my attempt to create a slick, photo-blocked description. Unfortunately, aside from having to rustle through the deep bins of CSS properties, my idea of having three columns of images turned out to be a much more cluttered design than I had anticipated. A recent workshop I had attended discussed the importance of usability in user interface design. In this case, the form most certainly did not follow function and I will have to do some rethinking to determine what is most important for a landing page.
    
    Additionally, the workshop got me to question a lot of aspects to our app: are our menus too wordy? Will users have a difficult time navigating to a destinated page? Is the aesthetic quality overwhelming the content or wholly underwhelming? I think the best answer to these questions, actually, would come not from developers, but test users. Our organization has discussed conducting a usability test for some weeks now but have not committed to one. It would be beneficial to hold one in the coming two weeks, so look out for details pertaining to it. 

# 2.15.17

## Updates
*Courses on My Page sorted*

  User profiles were a bit of a mess with the pros and studs list organized by edit timestamps, so we fixed it up to be sorted by course. With this organization, it's easier to determine if a user has experience in a course since it's placement in the list will always be included in the same location.

*Study sessions sortable by course ascending or descending*
 
  Like the above fix, the sessions listing is now sortable by course. Users may select between "Course Number (Low to High)" and "Course Number (High to Low)" to better their session browsing experience. It make still take O(n) time to look through them all, but at least it will be in order.
 
*Empty or duplicate topics prevented*

  Two things all people hate: repeating themselves and an empty agenda. So why did we let users list blank and duplicate topics for a session? Data validation for empty or duplicate topic inputs now forbids either from being added.
 
## Obstacles
  The largest obstacle these past 2 weeks came in the form of updating the study sessions page when a different sort order was selected. Since the sort was being done on the client side instead of the server, I had assumed that the page would not update reactively since the database was not being changed. Thus, I spent hours trying to get the change working with a global variable, reloading with FlowRouter, and partial page loading with jQuery. My efforts were fruitless for many a few days. It came to me while reading through other functions done by my teammates that a variable may be set for a particular session, which could replace the global variable I was using and force the page to update reactively. The issue was solved.

# 2.1.17

## Updates
*Edit and delete courses on profile page*
 
  Life never fails to give second chances and now so do we. If a user happens to list a course on their profile that they would like to edit or delete, there's now an option for that. Just click the little x for deletion, or click on the course number to edit the proficiency level.

*Creating group study sessions*
 
 When on a group page, users can now create a study session that includes all group members, whom users can set to either pros or studs. It's a lot easier than having every member navigate to the details page and join the session.
 
*Add and delete group members*
 
 Our site used to give a funny little message about how members added to a group would be "imaginary". We grew too old for imaginary friends, so users can no longer add any member name they want to a group. All members added are now actual users, who can be added or deleted from a particular group.
  
*Session Cards:*
 
 A table of upcoming study sessions felt too much like a fifth grade math class. So we've changed the listing to display every upcoming session as a card instead, making the site look a lot cleaner and a lot less elementary. 
 
*Search case-insensitive*
 
 Our searches were previously case-sensitive, so even a little capitalization would throw off an otherwise fine search. It's usually a good idea to be specific, but in this CASE, it's a little too much to be overly SENSITIVE. Jokes aside, we've made searches case-insensitive, so a searches like "ICS" and "ics" would return with the same results.  
 
## Obstacles
Reading another person's code is like entering your friend's kitchen. You know that everything must be working because your friend has been eating, but you're just not sure where the cups are or how exactly to use their stove. The same applies to modyifying code written by someone else: you may not know the variable names or how certain functions work at first, but upon use and some directions, one will find themselves familiar to it. 

As I have worked neither on the profile page nor the group page, I was forced to familiarize myself not only with the HTML but also with the databases that each page accessed. In addition, I had to get working with the FullCalendar package, which I had not used prior to these two weeks. It was tedious to understand at first, and while there is nothing more I would like to do than clean up the code to be more my style, when working in collaborative projects, one must be fluid. Programmers must settle for code that is easy for everyone to understand, not just themself.

As a side note, it seems as if with every issue solved, five more are formed. Sometimes you don't realize there's an issue until another one depends on it. I found a lot of minor issues that will be included in future milestones.

# 1.16.17

## Updates
*Fixed Calendar Bug*
 
 Nobody likes when something works half the time. Does a baker want his oven to be hot every other day? Well, we aren't bakers but we don't like half-baked efforts either. That's why we found updating jQuery to 1.11.10 gets rid of all that silly business with the study session creation modal popping up only when it feels like it.

*Required first name and last name*
 
 Future trolls may not be our fans, but we aren't in the business of letting users go willy-nilly with their usernames. (Truthfully, we aren't in any business at all.) Users are now required to enter their first and last names when creating their profile. This will be more convenient when browsing through study sessions. No more wondering if "mjg6" stands for your friend Mike or a complete stranger.

*Prevent creating sessions in the past*
 
 Unfortunately, time travelers aren't on our list of clients either. The calendar now prevents study sessions from being created in a date that has already been passed.

*Join session immediately; empty study sessions warning*
 
 Ever try planning an outing with your friends and it all falls apart within an hour? We understand. However, it isn't pleasant to the eyes to see sessions devoid of participants lying around the public calendar. Users that create a study session must now join the session, with the options of either being a Pro or a Stud. Like before, they may still change their choice or leave entirely on the details page. However, empty sessions are still unacceptable. For those rebels who want to leave sessions empty, we've left a warning in the details page tutorial and next to the "Leave Session" button for them to ponder on their way out. 
 
*Fix remove topic*
 
 The old system for removing topics for a study session was bunk. It expected users to type out the topic to be deleted, in correct spelling and capitalization, no less! It made the developers look stupid for the poor implementation and made users look stupid for making typos. Well, no more. Study session Pros can now simply click the x icon next to the topic to remove it.
 
*"Pro" Renamed*
 
 Out of respect for our professors, we decided to change the definition of "Pro" from "Professor" to "Professional". As much as we'd like to, we can't compare ourselves to be as knowledgeable on the course subject as our actual professors.
 
## Obstacles
MongoDB, for some reason or the other, could not be connected to and left my app hanging when starting up. A simple fix from the interwebs suggested I download and run Mongo seperately, and while this was certainly more tedious, it was not lacking in effectiveness. 

Aside from that, the only other issue appeared when I altered the removing topic function on a study session's detail page. I was having difficulty passing the value of the topic to be removed back and forth between the HTML and JavaScript. Once I understood that the id of the HTML icon tag could be set by and called by JavaScript, I had an easy method for passing the value between them.

# Future Release Updates (2.16.17 - 3.1.17)

### Landing Page
 - New look with informative description

### My Page
- A user's star review rating rounds down instead of up
- Make bio updateable

### Reviews
- Users allowed to view only reviews written about others, not themselbes

### Notifications
- General notificaiton functionality, for group invites, session dates, etc

### Groups
- Groups have an option to be private or public
- Users may post in a group page

### Study Sessions
 - Sessions will be sortable by date in addition to by course
 
### Admin
- Developers will receive administrator priviledges
