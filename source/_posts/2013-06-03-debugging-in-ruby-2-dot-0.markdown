---
layout: post
title: "Debugging in Ruby 2.0"
date: 2013-06-03 13:55
comments: true
categories: [debugging,rubymine,ruby-on-rails]
keywords: rails,ruby,rails-4,ruby-on-rails, ruby 2.0.0, debug, debugging
description: Debugging in Ruby 2.0
---

When trying to debug Rails applications that have been updated to use Ruby 2.0, you may run across some errors either via 'bundle update' or when trying to migrate the database. To resolve these and enable debugging, replace the ruby-debug-base19x gem with 'debase'.

```
group :development, :test do
  gem 'debase'
  gem 'ruby-debug-ide', '0.4.17'
end
```


