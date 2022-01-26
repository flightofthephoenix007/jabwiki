---
layout: default
title: Jab.Wiki | README
description: A community-managed GitHub repository keeping track of the companies, events, and universities requiring Covid jabs.
tags: covid jab vaccine covid-19
---
# Who's requiring COVID-19 jabs?

This is a running list of companies that are requiring their employees to get Covid-19 jabs. Pull requests gratefully accepted, especially
around design or data formatting or correctness. If you are a
journalist and would like to speak to someone about the list, email
flightofthephoenix@protonmail.com.  View the live website here:
[jab.wiki](https://jab.wiki).


## How do I add my company?

The short version is: the website is generated from the
[`companies.yml`](_data/companies.yml) file.  Add the details of your
company by mimicking what others have done, and create a PR.  If
you're not familiar with Git or Pull Requests, here are the steps.
You will need a Github account.

1. Make sure you're editing the main repository which hosts the
    website.  It is here on Github:
    [`https://github.com/flightofthephoenix007/jabwiki`](https://github.com/flightofthephoenix007/jabwiki).

1. Find the `companies.yml` file, and click the "Edit" button.  Here's
   a [direct link to the Edit
   page](https://github.com/flightofthephoenix007/jabwiki/edit/master/_data/companies.yml).

1. Add the brand/company, or update its details if something has changed.  Please try
   to put your new entry in roughly alphabetical order, by name, relative to existing companies.

1. Click "Propose File Change", the big green button at the bottom of
   the page.

1. This will take you to a page where you can click "Create pull
   request".  Once you do that, one of the maintainers of the website
   will attend to your update ASAP.

1. Thank you for helping us keep this site up-to-date! 🙏

## For developers

You may want to run the site locally, to see what it looks like while
you're making changes.  A full tutorial is out of scope here, but
these are the basic steps.  We assume you know a little bit of Ruby.

First, you'll need Ruby Bundler, which manages this project's
dependencies.

```shell
gem install bundler -v 2.1.4
```

Now, install the required Gems.

```shell
bundle install
```

When that's done, run the development server.

```shell
bundle exec jekyll serve
```

Jekyll will print a URL where you can see your local version running,
as it would on the web.  Usually that's
[`http://127.0.0.1:4000/`](http://127.0.0.1:4000/).
