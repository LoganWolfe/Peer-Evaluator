# README
This is a web application that streamlines the collection, collation, and analysis of peer evaluations.   
It is important to note that this was not a solo project, but a collaboration between five members (found below). 

*This project completed and submitted for credit at Ohio State University.*   
Thus, I am unable to publicly post the code. Images of the application can be found below.  
**I can and will happily review the code privately**.  

I (Logan Wolfe) am responsible for the Group and Roster models, controllers, views, forms, routes, db tables, etc.  
I contributed elsewhere but most of my work is seen there.  

Language-wise, I used Ruby, SQL, HTML, CSS, and JavaScript to achieve all functionality.   
Tools/technologies I used include Rails, Bootstrap, Devise, jQuery, jQuery UI, SQLite (dev), and PostgreSQL (prod).  

# Work Examples
##### Landing page for teachers. User log in and authentication is done using Devise.
![Teacher Landing Page](https://github.com/LoganWolfe/Peer-Evaluator/blob/06d68612a95f5c2d4e9a2e1f1c52c100f702f7cd/TeacherLandingPage.png)  
  

##### Group assignment page for teachers. Drag N' Drop lists from students enrolled in the class and currently in the group.
![Teacher Group Assignment](https://github.com/LoganWolfe/Peer-Evaluator/blob/06d68612a95f5c2d4e9a2e1f1c52c100f702f7cd/TeacherGroupDragNDrop.png)  
  

##### Teacher's review of evaluations and average score received by each student. Teacher can assign/change scores if needed.
![Teacher Review of Evaluations](https://github.com/LoganWolfe/Peer-Evaluator/blob/06d68612a95f5c2d4e9a2e1f1c52c100f702f7cd/TeacherReviewOfEvalulations.png)  
  

##### Landing page for students. Only option they have is to create new or view existing evaluations.
![Student Landing Page](https://github.com/LoganWolfe/Peer-Evaluator/blob/06d68612a95f5c2d4e9a2e1f1c52c100f702f7cd/StudentLandingPage.png)  

## Design
This application is designed to give the functionality of evaluating
peers in the classroom for particular projects. Teachers can add students to the roster, 
add students to groups, create groups, edit groups, delete groups, 
as well as assign projects to the groups. Teachers can also add additional 
teachers to the class if they choose to do so.

We chose to use Devise because of its ease of use when it comes to creating
everything we need for user authentication, resetting passwords, 
and more.

We chose to use Bootstrap because it seemed like a good framework to use
for styling after the Tech Task presentation and we, as a group, felt 
it was the best choice.

We added a Users_groups table to support the has_many_and_belongs_to_many 
relationship between users and groups.

We wanted to add a drag-and-drop functionality to add existing students
to groups, but we had some issue with it, so we had to settle for a textbox
to copy and paste existing students' emails to the textbox to add them to groups.

Another choice we made was to have teachers add more teachers as they 
please, rather than having some users sign up as teachers. The only catch in 
this is that we would have to manually create the first teacher in rails console
to begin, however we deemed this acceptable for greater security.

Since our initial version we have fixed a multitude of bug fixes to streamline the application

We added the ability for teacher to assign scores to students based on their average evaluation score, and added the student's current average score as given by their peers in parentheses next to each student's name 
on the teacher evaluation form.

We have created some test data to experiment with here are the accounts (you can also create your own account but in order to see admin views 
use the example teacher account)

## Extensions:
We have multi-group functionality for a teacher to add a student 
to multiple groups if they please.

We added a password extension that allows a user to set a password
 of length 8-20 characters as opposed to the default Devise 6 
character minimum.

We added the extension that handles a student dropping out cleanly 
by deleting all evaluations done for or by that student, as well as 
deleting the teacher evaluation of that student. 

We added an easy method of adding and removing group members by
implementing jQuery and jQuery UI to create draggable lists of group
members and students.

## Authors (The Goofy Goobers)
* Snigdha Kalluri
* Sharanya Vojjala
* Alex Haas
* Derek Nelson
* Logan Wolfe
