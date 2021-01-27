====================
LCV Dashboard
====================

User profile data
====================
The website should store as part of the user's profile:

* the current number of points earned
* the badges earned with the date the badge was earned
* the current number of words captured
* the current number of articles captured

System Tasks
==============
To generate content for the dashboard, the following scheduled tasks must be executed daily:

* a daily task to award badges
* a daily task to update totals.  We don't want to have to manually update the data every time the page is viewed (technically similar to the voting API module)
