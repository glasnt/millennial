[See talk](talk/)

### Hacky way
Link a local clone of django into a virtualenv of an empty folder

Start with a local project, `django-admin startproject MYPROJECT`

Change `LANGUAGE_CODE = 'de-de'` in `settings.py`

Edit: `<djangoclone>/django/contrib/admin/locale/de/LC_MESSAGES/django.po`

In the `<djangoclone>/django/contrib` folder, run `django-admin compilemessages`

Restart django webserver. 

... 💰

### Bugs

`django-admin makemessages -l ur_LC` doesn't work, generates functions that raise ValueErrors with Plurals

Editing local copies of locale versions known to work is a dirty dirty hack
