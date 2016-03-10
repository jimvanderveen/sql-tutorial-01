# sql-tutorial-01
Material for a 1-hour tutorial on SQLite, geared toward Data Scientists.

# Getting set up
Follow the [software carpentry installation instructions](http://www.thehackerwithin.org/davis/swc-installation.html).
Once that's done, verify that you have sqlite installed:

`sqlite --version`

Define editor?

# Data dictionary

What tables are in the database?
`SELECT name FROM sqlite_master WHERE type='table'`

What columns are in a particular table?
`pragma table_info(table_name)`

# Create a table

# Populate table with data

