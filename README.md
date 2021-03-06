#lol_dba ![travis](https://api.travis-ci.org/plentz/lol_dba.png?branch=master)

lol_dba is a small package of rake tasks that scan your application models and displays a list of columns that probably should be indexed. Also, it can generate .sql migration scripts. Most of the code come from rails_indexes and migration_sql_generator.

### Quick example

To use lol_dba in the easiest way possible you have to do two things:

	gem install lol_dba

Then run one of the following commands...

To display a migration for adding/removing all necessary indexes based on associations:

	lol_dba db:find_indexes

To generate .sql files for all your migrations inside db/migrate_sql folder:

	lol_dba db:migrate_sql

### Not-so-quick example

If you want to use lol_dba with rake, you should do a few more steps:

Add lol_dba to your Gemfile

    gem "lol_dba"

Run the install command

    bundle install

Use it the same way you use other rake commands

	rake db:find_indexes
	rake db:migrate_sql

### Compatibility

Compatible with Ruby 1.9 and Rails 3.x. I think.

### About primary_key

>The primary key is always indexed. This is generally true for all storage engines that at all supports indices.

For this reason, we no longer suggest to add indexes to primary keys.

### Tests

To run lol_dba tests, just clone the repo and run:

    bundle install && rake

to run the tests.

### Feedback

All feedback, bug reports and thoughts on this gratefully received.

### Contributors

* [Diego Plentz](http://plentz.org)
* [Elad Meidar](http://blog.eizesus.com)
* [Eric Davis](http://littlestreamsoftware.com)
* [Jay Fields](http://jayfields.com/)
* [Muness Alrubaie](http://muness.blogspot.com/)
* [Vladimir Sharshov](https://github.com/warpc)
* [Fabio Rehm](http://fabiorehm.com/)

### License

Lol DBA is released under the MIT license.
