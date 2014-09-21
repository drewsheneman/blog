---
layout: post
title: "My Journey Upgrading to Rails 4"
date: 2013-05-31 16:14
comments: true
categories: [rails,ruby-on-rails]
keywords: rails,ruby,rails-4,ruby-on-rails
description: My Journey Upgrading to Rails 4
---
Upgrading to Rails 4 in an existing application can be quite a switch. I decided to make the jump and handle any complications as they come. After about an hour or so I was mostly up and running, with a few issues here and there with gems I am using and their various versions.

## Resources ##

As is often the case, the <a href="http://railscasts.com/episodes/415-upgrading-to-rails-4" target="_blank">Railscast</a> on the subject proved invaluable. There is also a robust compilation of Rails 4 links being maintained <a href="http://blog.wyeworks.com/2012/11/13/rails-4-compilation-links/" target="_blank">here</a>.

## RubyMine ##

If you use RubyMine, you may run across an error when trying to start your development server.

```
Error running Development: Rails 3.x launcher script was found instead of Rails 4.x one.
```

When a new Rails 4 application is created, it generates a 'bin' folder. Creating a new, blank Rails 4 application and copying its 'bin' folder into the existing project will resolve the error and allow the server to be started in RubyMine.

## Gems ##

One gem that gave me a few errors was simple form. I updated my Gemfile to:

```
gem 'simple_form', '~> 3.0.0.rc'
```

However, when loading my forms in the browser, I received another error:

```
wrong number of arguments (3 for 2)
```

After doing some digging I found that this was actually related to the client_side_validations gem, which I was no longer using and safely removed this from the project. If you need this gem, there is a <a href="https://github.com/bcardarella/client_side_validations/tree/rails-4.0-quick-fixes" target="_blank">branch</a> for Rails 4 which should help.

Looking forward to implementing the great additions in Rails 4.
