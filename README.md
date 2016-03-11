# sql-tutorial-01
Material for a 1-hour tutorial on SQLite, geared toward Data Scientists.

# Getting set up
Follow the [software carpentry installation instructions](http://www.thehackerwithin.org/davis/swc-installation.html).
Once that's done, verify that you have sqlite installed:

`sqlite3 --version`

or `sqlite --version`

I'm using version 3.7 *with readline support* (arrow keys)

We'll be using sample data from the [half-day software carpentry SQL class](http://swcarpentry.github.io/sql-novice-survey/).
We don't have time to go through the software carpentry course, but I encourage you to do it on your own.
Then drop by the DSI space on Wednesday afternoons 15:00-17:00 for open hacking sessions, questions, etc.

But right now, you need the *survey.db* file.
Create a scratch directory on your laptop, and download or move the survey.db file there.
Then fire up sqlite to open the database:

`sqlite3 survey.db`

# First things first
'.quit'

(restart sqlite)

'.help'

# Data dictionary

What tables are in the database?

`.tables` (this is sqlite-specific)

or

`SELECT name FROM sqlite_master WHERE type='table'` (still sqlite-specific, but more "the SQL way")

What columns are in a particular table?

`pragma table_info(table_name)`

# Database CRUD
* Create (INSERT)
* Read (SELECT)
* Update (UPDATE)
* Delete (DELETE)

Be very careful with those last two!!

<pre>
create table Copy as select * from Person;
pragma table_info(Copy);
select * from Copy;
update Copy set ident='Jim';
select * from Copy;
</pre>
<img src="http://vignette2.wikia.nocookie.net/pacificrim/images/0/09/Homer-Simpson-wingnuts-doh.gif/revision/latest?cb=20130909105555" alt="Doh!"/>
