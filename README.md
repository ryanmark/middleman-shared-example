# Shared source example

This is an example project that demonstrates sharing assets between middleman
projects without copy-paste duplication.

The project that lives in `shared` is effectively merged into the parent
project on the fly by middleman. This `shared` directory is meant to be a
git submodule or symlink. Copying files into `shared` defeats the purpose.

Folks that frequently create one-off sites need to reuse layouts,
partials and other assets. This rig allows them to do that without copying
and pasting from one project to the next. Components that will be reused
can be added to the shared project and automatically carried forward into
future projects. It also makes it much simpler to retrofit older projects
with updated assets.

The hacked up middleman code can be found
[here](https://github.com/ryanmark/middleman/tree/v3-shared-source) and
[here](https://github.com/ryanmark/middleman-sprockets/tree/v3-shared-source).

## Installation

Just clone this repo, pull in the submodule and set it up like any other
middleman project.

    git clone https://github.com/ryanmark/middleman-shared-example.git
    cd middleman-shared-example
    git submodule update --init
    bundle install
    bundle exec middleman
    open 'http://localhost:4567'
