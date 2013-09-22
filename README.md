heroku-buildpack-nikola
=======================

A buildpack for Nikola on Heroku.

New site:

    $ ls
    conf.py  stories  posts # etc...
    $ heroku create --stack cedar --buildpack git://github.com/getnikola/heroku-buildpack-nikola.git
    $ git push heroku master

Existing site (you likely do not want it):

    $ heroku config:add BUILDPACK_URL=git://github.com/getnikola/heroku-buildpack-nikola.git

The buildpack will work only if you have a `conf.py` file.

Caveat: `nikola serve` is used by the site.  Sorry if this bothers you
(you are free to roll your own buildpack if you do not like that).
