# Existing Django App
Part of what makes nanobox so useful is you don't have to have python or django installed on your local machine.

This guide will help you get an existing Django app up-and-running with nanobox.

## Build a Ruby Dev Environment
Nanobox will create an isolated virtual environment and mount your local codebase inside of. From within this environment you can run the app, a django console, or even rake tasks as you would normally.

#### Add a boxfile.yml
The boxfile.yml tells nanobox how to build and configure these environments. Create a `boxfile.yml` at the root of your project that contains the following:

```yaml
# tell nanobox to build a python runtime
code.build:
  engine: python
```

#### Build the Environment

```bash
# build a python runtime
nanobox build

# deploy the python runtime into the dev environment
nanobox dev deploy

# add a convenient way to access your app from a browser
nanobox dev dns add django.nanobox.dev
```

## Configure your Django App
WIP

## Django up-and-running
With the app configured the last thing to do is run it:

```bash
# run the app from the nanobox dev console
python manage.py runserver 0.0.0.0:8080
```

Visit the app from your favorite browser at: `django.nanobox.dev:8080`

## Now what?
With an app running in a dev environment with nanobox, whats next? Think about what else your app might need and hopefully the topics below will help you get started with the next steps of your development!

* [Connect a database](/python/django/connect-a-database)
* [Javascript Runtime](/python/django/javascript-runtime)
* [Local Environment Variables](/python/django/local-evars)
* [Back to Django overview](/python/django)