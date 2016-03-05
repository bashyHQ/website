---
layout: project
project: launchpage
permalink: /projects/launchpage/
---

## Features

 - Easy to Setup
 - Beautifully designed Launchrock Page
 - Zero-Cost Hosting (using Github-Pages and Mailchimp)
 - Easy yet flexible YAML-Based Configuration
 - 100% FLOSS
 - User-Data Collection (using Mailchimp) and Social-Sharing (with tracking)

## Setup

Do the following steps to get your very own launchpage off the ground:

1. Fork this Repo
2. Configure the Project
3. Profit!

## Project Configuration

### Describe and Configure the Project Website

### Setup Mailchimp for User Data collection

Sign up for or log in into [Mailchimp](https://login.mailchimp.com/), then go on an create [a new list](http://kb.mailchimp.com/lists/growth/create-a-new-list?) for the email addresses you want to collect.

Next, make sure you have the right fields set up. For that, navigate to `Settings -> List Fields and *MERGE* tags`. Add, change and remove fields until you have the following list of merge keys: `EMAIL`, `NAME`, `CODE`, `REFERRER`, and `SOURCE`. The last three are used for tracking and aren't strictly necessary but are very good to have (see below)!

Save the settings. [Now follow their guide on how to find out your list number](http://kb.mailchimp.com/lists/signup-forms/host-your-own-signup-forms) and such and use it to configure mailchimp in the `_config.yml`.

For the example given by them, the setting would look the following:

```yaml
mailchimp:
  # the _HOSTNAME_ (!!ONLY!!) from the post-action
  server: mailchimp.us8.list-manage.com
  # found in the hidden "u"-value
  user: a123cd45678ef90g7h1j7k9lm
  # found in the hidden 'id'-value
  id: ab2c468d10
```

**RESTART jekyll**, as changes to the config aren't picked up automatically. Now try to sign up using the form on the bottom of your website.


#### Understanding the Fields

For your understanding, the keys have the following function: `EMAIL` and `NAME` should be self-explanatory, `CODE` is an MD5-Hash of the email-address and is used for tracking: it is appended to the URL they are asked to share with others and if someone records from any of those links, we record that in the `SOURCE`-field. `REFERRER` holds the `window.referrer`-Reference of which page the person came from/found the link on. If the user has localStorage on and comes to that page from multiple sources over time, each one will be recorded and once they submit all of them will be submitted as a `|`-separated list.

As we aren't actively checking whether `SOURCE` matches any code in our database, you can also use that to track sources from pages you post somewhere. For example, append `#hackernews` to the URL you submit to hackernews and you'll see in your database, who signed up from hacker news. **Note**: Just make sure TO NOT use the `|` as it is used as a storage facilitator.


# Develop locally

Clone the repo to your local system. Then install [jekyll](http://jekyllrb.com) through bundler:

```
  bundle install --path .vendor/bundle
```

## Run

Now you can run the server by running:

```
bundle exec jekyll serve
```

and experience the auto-recompiling server at

`http://localhost:4000`

# Contributing

Just Fork, Change and send a PR. If you want to make bigger changes you aren't sure are wanted, start an issue first and we'll happily discuss what you are up to.

By contributing you agree to having the code licensed as specified below.

# License

Please understand that this repo is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE. For more information please look at the LICENSE file in the root of this project!
