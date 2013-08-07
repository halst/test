Urlbeat—simple URL shortener web app
======================================

Urlbeat provides a single resource called Redirection.

 * Redirection is created by submitting a POST request to
   `/` with `url` parameter.

 * Redirection is accessed by submitting a GET request to
   `/<key>` where key is the short URL identifier.

All responses are non-negotiable HTML.

A demo is available at <http://urlbeat.heroku.com>.

To run locally you need to export `DATABASE_URL`
environment variable pointing to your SQLite or PostgreSQL
database, for example:

    export DATABASE_URL=postgresql+psycopg2://databaseuser:P@ssw0rd@localhost/the_database

Then install Python requirements:

    pip install -r requirements.txt

Use [foreman](http://blog.daviddollar.org/2011/05/06/introducing-foreman.html)
to start the app:

    foreman start
