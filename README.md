Contentful Action Example
=====

An example application for how you can integrating content migrations in your continuous delivery pipeline using the Contentful GitHub Actions.

What is this about?
=====

This example deploys a simple flask site integrated with Contentful onto Heroku utilizing GitHub Actions.

You can read our [conceptual guide](https://www.contentful.com/developers/docs/concepts/deployment-pipeline/) on how to utilize Contentful Environments inside your continuous delivery pipeline.

Getting started
=====

### Requirements

To use the continuous delivery pipeline of this project you need accounts for the following services:

- [Contentful](https://www.contentful.com)

### Setup

* Fork and clone this repository

#### The Contentful part (required)

* Create a new space using the Contentful CLI
  * `$ contentful space create --name "continuous delivery example"`
* Set the newly created space as default space for all further CLI operations
  * `$ contentful space use` (this will present you with a list of all available spaces – choose the one you just created)
* Import the provided content model (`./import/export.json`) into the newly created space
  * `$ contentful space import --content-file ./import/export.json`

#### Local development environment (optional)

* Create a virtual environment
  * `$ virtualenv env`
* Activate the virtual environment
  * `source env/bin/activate`
* Install all Python dependencies
  * `pip install -r requirements.txt`
* Start the Flask app
  * `python myapp.py`
* Rename config file `.env.example` to `.env` and add missing keys

#### The continuous delivery pipeline


License
=======

Copyright (c) 2019 Contentful GmbH. Code released under the MIT license. See [LICENSE](LICENSE) for further details.
