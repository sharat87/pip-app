# pip-app

This tool automatically build venvs for your pip apps and link
them in your bin path for ease of use.

## So, what problem is this tool trying to solve?

With more and more apps written in python and packaged with pip, you
can end up with a dependency nightmare if you don't use virtualenvs.

If you use virtualenvs, you'll have to switch to the virtualenv or
give a full path to your installed binary to use it.
This is tedious.

## Aren't there solutions available to fix that (yet)?

I've tried to use autoenv or many different tools, but I still found the
whole thing tedious. autoenv need to drop files to know how to enable/
disable the venv, and other solutions may still require you to build
your venv manually. There are other tools to detect venvs and enable
them, but I found them slow to use, sometimes because they recurse
across sub-directories. This solution is far simpler.

## How to use this:

Install AdvancedSearchDiscovery

    pip-app install AdvancedSearchDiscovery

Use AdvancedSearchDiscovery

    asd linux --query is openstack ready for production

That's for simple pip apps.

You can also have many apps in the same venv. The first app would be
the venv name.

    pip-app install ansible AdvancedSearchDiscovery

That would create a new venv ansible, with the ansible CLI tools, but
also AdvancedSearchDiscovery. Please note that if the venv already
exist, it will update the venv with the new extra apps.

That is really ideal for some apps that fail to ship the proper full
list of dependencies!


This tool was a fork of sharat87's [pip app](http://github.com/sharat87/pip-app)
but is now probably completely defaced.

# Installation with ZSH

## Antigen

If you use [Antigen](https://github.com/zsh-users/antigen), add the following
command to your .zshrc with your other antigen bundle commands.

    antigen bundle evrardjp/pip-app

## Zgen

If you use [Zgen](https://github.com/tarjoilija/zgen), add

    zgen load evrardjp/pip-app

to your .zshrc along with your other zgen load commands.

## Without a Framework

If you aren't using a framework, just clone this repo or just download
the *pip-app.sh* file and add a source line to your `.zshrc`.

    source /path/to/pip-app.sh

# Installation with Bash

Just clone this repo or just download the *pip-app.sh* file and add a
source line to your `.bashrc`.

    source /path/to/pip-app.sh

# Meta

This thing is licensed with MIT License, due to original author license
(http://mitl.sharats.me). Feedback, problems, discussion, tweet at
[@evrardjp](http://twitter.com/evrardjp) or open
up and issue on the [github project page](http://github.com/evrardjp/pip-app/issues).
