# heroku-buildpack-django-sass

Designed to be added as an additional buildpack after the standard
`heroku/python` buildpack:

    $ heroku buildpacks:add --index 2 https://github.com/drpancake/heroku-buildpack-django-sass.git

It runs `python manage.py compilescss` to generate CSS files and then
runs `python manage.py collectstatic --noinput` again to copy them to the
expected directory.
