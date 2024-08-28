# Prepare environment

Install ruby from https://rubyinstaller.org/

When the command prompt shows up select option 1 and click send.

create a python virtual interpreter with jupyter installed:

    python -m venv al_folio_venv

Activate

    al_folio_venv/scripts/Activate.ps1

Install requirements:

    python -m pip install -r requirements.txt

# Execute

Jekyll project to generate the static version of the website

Todo:

    gem install bundler jekyll
    bundle install

    bundle exec jekyll serve --force_polling --incremental --watch --livereload


If you get the following error:

    There was an error while loading `minimal-mistakes-jekyll.gemspec`: No such file or directory @ rb_sysopen - ./package.json. Bundler cannot continue.

Delete the whole _site folder.

# REMOVE SECTIONS

In _config.yml add to exclude the folder related to the section you want to remove, if it is a collection also disable it by searching the "collection" section in _config.yml then set the corresponding flag "enabled" to false.
Also, to remove it from the menu go to _includes folder and remove those pages from the header.html (or header .liquid). [Documented in this answer](https://github.com/alshedivat/al-folio/issues/67).