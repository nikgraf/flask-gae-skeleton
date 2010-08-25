# Motivation

We are currently migrating our projects from [django](http://www.djangoproject.com) to [flask](http://flask.pocoo.org).
Since we also intend to use flask for entirely new projects, it made sense to save on initial setup time.
So we created a project skeleton which includes some of the things (libs and configuration) that we pick for most projects.

# Includes

here is a list of assembled components

* flask 0.6
* flask decorators for (cache_page, login_required)
* jinja 2.5.2
* werkzeug 0.6.2
* gae specific monkeypatch for werkzeug debugger (http://dev.pocoo.org/projects/werkzeug/wiki/UsingDebuggerWithAppEngine)
* a simple user model
* google appengine specific development/production environment switch
* google appengine appstats configured
* google appengine memcache caching backend configured
* favicon.ico stub to avoid unneeded error logs
* deck module with 26 char uuid generator
* deck module with JsonProperty for the datastore
* facebook python sdk (commit 2da0f678f0c0c5a5ddc77b7456dde232e9b98bd9)
* facebook javascript sdk (loaded async from facebook servers)
* jQuery 1.4.2 (loaded async from google servers)
* lib directory for external dependencies prepended to syspath

# Setup

* change the 'secret_key' in main.py
* set your own appengine application id in app.yaml
* add facebook configuration to main.py

# TODO

things we still need to extract and clean up from other projects

* facebook auth via oauth2 redirection (for mobile support)
