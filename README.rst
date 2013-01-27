========================
django-startproject
========================

A project template for Django 1.5.

Creating your project
=====================

To create a new Django project called '**myproject**' using django-startproject, run the following command (this assumes you have Django 1.5 or 1.4 installated aready)::

    $ django-admin.py startproject --template=https://github.com/leveille/django-startproject/zipball/master --extension=py,rst,html myproject

You can choose a different name by running the same command but replacing the word '**myproject**' with something else.

Installation of Dependencies
============================

First, make sure you are using virtualenv (http://www.virtualenv.org)::

    $ mkvirtualenv --distribute myproject

You will also need to ensure that the virtualenv has the project directory
added to the path. Adding the project directory will allow `django-admin.py` to be able to change settings using the `--settings` flag.

In Linux and Mac OSX, you can install virtualenvwrapper (http://http://virtualenvwrapper.readthedocs.org/en/latest/), which will take care of adding the project path to the `site-directory` for you::

    $ cd myproject && add2virtualenv `pwd`

Then, depending on where you are installing dependencies:

In development::

    $ pip install -r requirements/local.txt

For production::

    $ pip install -r requirements.txt

Acknowledgements
================

I'm working through the `twoscoops book`_.  Thanks to those guys for the push I needed to finally put together some startproject files.  Most of what's here has been hijacked from them.

.. _twoscoops book: https://django.2scoops.org/
