Using South with Django-CMS
===========================

South is an incredible piece of software that lets you handle database migrations.
This document is by no means meant to replace the excellent documentation available online,
but rather to give a quick primer on how and why to get started quickly with South.

Once you go South, you never look back :)

Installation
------------

Using Django and Python is, as usual, a joy: installing South should mostly be as easy as typing::

	pip install South

Then, simply ad "South" to the list of installed apps in your ``settings.py`` file.
That's it!

Basic usage
-----------

For a very short crash course:

#. Instead of the initial manage.py syncdb command, simply run ``manage.py schemamigration --initial <app name>``. \
   This will create a new migrations package, along with a new migration file (in the form of a python script).
#. Run the migration using manage.py migrate. Your tables have now been created in the database, Django will 
   work as usual
#. Whenever you make changes to your models.py file, run ``manage.py schemamigration --auto <app name>`` 
   to create a new migration file, then ``manage.py migrate`` to apply the newly created migration!

That's it!

More information about South
----------------------------

Obviously, South is a very powerful tool and this simple crash course is only the very tip of the iceberg.
Readers are highly encouraged to have a quick glance at the excellent official South documentation::

	http://south.aeracode.org/docs/index.html
