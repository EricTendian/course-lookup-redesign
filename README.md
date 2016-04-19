# course-lookup-redesign
Redesigning the way Illinois Tech students search for courses on MyIIT.
For ITMD 362, HCI and Web Design.

Team members: Jordan Mynes, Zdenek Jaks, Eric Tendian

## About the project

View the site live: http://myiit-course-lookup-redesign.s3-website-us-east-1.amazonaws.com/

View the repository: https://github.com/ITMD362-JaksMynesTendian/course-lookup-redesign

We started out by making a very simple login page, that had little unnecessary
information. Our login page has a username and password field, with a security
message at the bottom to keep the user informed of best practices. If we were
to hook this login page up to MyIIT for real, we would want it to submit the
credentials via POST instead of GET, so the username and password doesn't show
up in the URL.

Once the user logs in they are greeted with a simple welcome screen. This page
has a navigation bar which allows the user to quickly navigate to popular MyIIT
pages. One of our design principles was to feature popular information prominently.
Looking at the modules on the welcome page, we wanted to feature events and news
as that is often sought by students. For the IIT Today module, we plan to have
a couple featured stories and then a list of other recent stories which users
can click to view more. Finally, we have Public Safety contact info, and would
have other contact info available, include a method to search for a specific
student or staff/faculty member.

Looking at the academics page after clicking on it from the navigation bar, we
have more important student information. First, the ID numbers of the student,
which are useful for registration. Next, we have a link to our course search
page, which will be discussed in a bit. After that, we have two modules carried
over from the old Academics tab on MyIIT, the academic profile and student grades.
Eventually we would have more modules available, changing the single column
layout to a two-column layout if the viewport was large enough.

On the course lookup page, we have a search module that has a search field, plus
additional options which allow the user to change how the search works. This
would allow the user to have additional control, which is one of the principles
we employed. The reason the search field doesn't have a search button is because
the search is instant. Typing a course name would automatically show new results
and remove old ones. We were not able to get the search working, so the field
does not do anything at the moment.

Taking a look at the actual results, we put all the important info about a course
in one place, and used separation with proximity to distinguish the attributes
of the course. For the table of sections, this was challenging to show at small
viewport sizes, so we made use of a jQuery plugin called FooTable to change
columns of the table which were overflowing into separate rows. This allows
easy browsing at almost any screen size. As not all information is on the course
panel, users can click links and get directed back to MyIIT where they will find
additional information on the course and section.

Users are able to add sections to their cart and have it update their schedule
as well - by clicking the add buttons on the course panel, or by clicking the
remove button on the cart with a list of sections. Adding or removing sections
from the cart would update the schedule. We did not have time to implement
this functionality, but we have shown an example of a cart with four courses
added to it. Once the user has all their courses, they can register for the
courses by clicking the button, which will take them back to MyIIT and
automatically input the CRN numbers, then request the user to input their PIN
to confirm.

Overall, our site is quite minimal, but the simple design makes it much more
cleaner than the old MyIIT design. We would like to improve the color scheme
as well as add more content, but this gives an idea of our prototype for a new
course search process. Eventually filtering and sorting would have been added
to the course search page, so the user has even more control over the data.

Some of our sources are listed below.

## Sources

- MyIIT/Banner for course data
- Icon source: https://www.iconfinder.com/iconsets/very-basic-android-l-lollipop
- Responsive table plugin: http://fooplugins.github.io/FooTable/index.html
