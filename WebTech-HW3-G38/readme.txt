Group id:
G38

Names and student numbers of all authors:
Andreas Meeldijk 0892734
Taha Sebai 5372135
Max Maes 5105269

Link:
http://webtech.science.uu.nl/group38/

A brief explanation of your web-site, the structure of your application, including every content file and every code file, the structure of your database:

Our website was originally a cooking website where users could access various recipes, culinary news, and related content.
However, for this assignment, we extended the website’s functionality by adding social media features.



When a user first visits the website, they land on the index page, where they can either log in (if they already have an account) or register a new account.
Registration happens on a dedicated page, where the user fills out a form with their information: firstName, email, course, etc.
This information is then stored in the database.
Once the user logs in or registers successfully, a session is created (storing the user’s email), and they are redirected to the home page.


From the home page, the user can either explore culinary news (original cooking-related content), or access new social media features via the navigation bar:
- view profile: the user can see all of his information except for their password for security measures.
- edit profile: the user can modifiy their information.
  A pre-filled form is shown with the current data (excluding the email, which serves as the unique ID).
  Once submitted, the new information is saved to the database, and the user is redirected to the profile page.
- My courses: The user can view all courses they are enrolled in.
  Clicking on a course redirects them to a course-specific page (/courses/course/:name) where they can see who else is enrolled,
  send friend requests to other students, or navigate back to the courses list
- Friends: The user can see all their current friends, visit their friends’ profiles (to check which courses they are enrolled in),
  and view and accept friend requests to grow their network
- Check your messages (Inbox): Users can view their full message history.
  Each message displays the sender, the content, and a reply button.
- Write a message: from this page, the user can send a new message to any of their friends.





The SQL definition of your database (the CREATE TABLE statements):

CREATE TABLE IF NOT EXISTS users (firstName TEXT, lastName TEXT, password TEXT, email TEXT, major TEXT, age NUMERIC, photo TEXT, hobbies TEXT)
CREATE TABLE IF NOT EXISTS user_courses (user_email TEXT, course_name TEXT)
CREATE TABLE IF NOT EXISTS friends (user_email TEXT, friend_email TEXT)
CREATE TABLE IF NOT EXISTS messages (sender TEXT, recipient TEXT, message TEXT)
CREATE TABLE IF NOT EXISTS friend_requests (sender TEXT, recipient TEXT)


users: Stores all user information except course enrollments.
    email acts as a unique identifier (ID) for each user.
user_courses: Tracks course enrollments.
    This table allow a user to be enrolled in multiple courses without data redundancy.
friends: Stores established friendships between users.
    This table allows users to have multiple friends without redundancy.
messages: Records all messages exchanged between users.
friend_requests: Keeps track of pending friend requests.


Logins and passwords of all registered users:
XjMTnviJ#7	anna.anderson1@example.com
OCMDJ2Jx!2	anna.brown24@example.com
x*l^cXV*H&	anna.clark6@example.com
jrB2MJOF3B	anna.martinez25@example.com
bkX3BB&XFw	anna.smith48@example.com
FEh1z5eLf9	anna.taylor8@example.com
s2fByoZc1U	david.anderson31@example.com
yBWzrGp4P*	david.clark20@example.com
p%G4aAcVz8	david.garcia23@example.com
cwBuNjSkNz	david.johnson11@example.com
y4uGN3o*LP	david.smith41@example.com
0B4QMdIr@K	ella.anderson18@example.com
&y2@yP!qBE	ella.brown30@example.com
i#g1vrDiwv	ella.garcia15@example.com
euzAxeQNPR	ella.johnson4@example.com
QCDi2iXGwm	john.smith9@example.com
GYY7W*39yt	lena.anderson33@example.com
YK3V!bz&@m	lena.brown35@example.com
yHg%LS^^GM	lena.johnson45@example.com
laCQnu*Tm8	lena.lee47@example.com
jeXFgVckBY	lena.smith12@example.com
PpO&GtMp%6	lena.taylor38@example.com
rOrm&GP*@A	mark.anderson22@example.com
GdFow0tC3S	mark.brown2@example.com
oqLK&SYtUM	mark.johnson43@example.com
ON^69BsjyC	mark.lee40@example.com
BCDrc0!fOG	mark.taylor13@example.com
hOkhVDz7tz	mark.wilson26@example.com
5FbL&b2Xpk	noah.brown27@example.com
3TsoQLCZf$	noah.garcia3@example.com
O2MuCrE0wt	noah.lee34@example.com
bQ*RQX8Ldv	noah.smith17@example.com
$vF^7g$U2S	noah.taylor19@example.com
Q2x3kYE7gZ	sarah.anderson29@example.com
j6BKu0fLWZ	sarah.clark28@example.com
ODToADLNBM	sarah.johnson39@example.com
Kg%k%ZP0Bi	sarah.martinez21@example.com
porKmfS!Gl	sarah.taylor0@example.com
tOr4qGJpe!	sarah.wilson42@example.com
9uNH!Ip#Or	sophie.anderson16@example.com
Y#3DMb9Dm7	sophie.brown5@example.com
h$r&ePjcPG	sophie.clark32@example.com
P#nGx0UijW	sophie.garcia46@example.com
XQmbAYCT71	sophie.lee7@example.com
pZz5&Slxkt	sophie.taylor37@example.com
FQK$LWTcD6	sophie.wilson36@example.com
ceeli$0YAK	tom.lee14@example.com
AOM8yBaU$@	tom.martinez10@example.com
Tae6tkcI#&	tom.taylor49@example.com
0YU1kmmktu	tom.wilson44@example.com




