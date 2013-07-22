=====================
django_localflavor_in
=====================

Country-specific Django helpers for India.

=======
WARNING
=======

This app has been superseded by the newly created django-localflavor_ app
which recombines all the different country locaflavors again (after having
been removed from Django). Development and maintenance of this app has
stopped and is only left online as a reminder for the users of those apps.
It will be removed after grace period of 1 Django release (~spring 2014).

.. _django-localflavor: https://github.com/django/django-localflavor/

What's in the India localflavor?
================================

* forms.INStateField: A form field that validates input as an Indian
  state/territory name or abbreviation. Input is normalized to the
  standard two-letter vehicle registration abbreviation for the given
  state or territory.

* forms.INZipCodeField: A form field that validates input as an Indian
  zip code, with the format XXXXXXX.

* forms.INStateSelect: A ``Select`` widget that uses a list of Indian
  states/territories as its choices.

* forms.INPhoneNumberField: A form field that validates that the data
  is a valid Indian phone number, including the STD code. It's normalised
  to 0XXX-XXXXXXX or 0XXX XXXXXXX format. The first string is the STD code
  which is a '0' followed by 2-4 digits. The second string is 8 digits if
  the STD code is 3 digits, 7 digits if the STD code is 4 digits and 6
  digits if the STD code is 5 digits. The second string will start with
  numbers between 1 and 6. The separator is either a space or a hyphen.

See the source code for full details.

About localflavors
==================

Django's "localflavor" packages offer additional functionality for particular
countries or cultures.

For example, these might include form fields for your country's postal codes,
phone number formats or government ID numbers.

This code used to live in Django proper -- in django.contrib.localflavor -- but
was separated into standalone packages in Django 1.5 to keep the framework's
core clean.

For a full list of available localflavors, see https://github.com/django/
