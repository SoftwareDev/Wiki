Setting up the Database (SQLite3)
=================================

Installing the Database
-----------------------

### GNU/Linux

On Debian and Ubuntu, a simple

    #> aptitude install sqlite3 libsqlite3-dev


Configuring SQLite3
-------------------

If you are using SQLite3, save the following text as \`config/database.yml\` (in the MarkUs root directory). You can use \`config/database.yml.sqlite3\` as example:

    # SQLite version 3.x
    #   gem install sqlite3-ruby (not necessary on OS X Leopard)
    development:
      adapter: sqlite3
      database: db/development.sqlite3
      pool: 5
      timeout: 5000

    # Warning: The database defined as "test" will be erased and
    # re-generated from your development database when you run "rake".
    # Do not set this db to the same as development or production.
    test:
      adapter: sqlite3
      database: db/test.sqlite3
      pool: 5
      timeout: 5000

    production:
      adapter: sqlite3
      database: db/production.sqlite3
      pool: 5
      timeout: 5000

