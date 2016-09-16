---
layout: walkthrough
title:  Create your application - Part 2 - Walkthrough of GeoConcerns"
date:   2016-06-07 11:29:01
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Create your GeoConcerns application. Created as part of a tutorial series given in a Walkthrough of GeoConcerns'
---

Note: If you have issues with any of these steps, a prebuilt version of this application is available within the provided virtual machine. The application can be accessed by SSHing into the virtual maching and then changing directory to `pregenerated/demo_geoconcerns_app`.

## Create your application

Prerequisite: Make sure your [environment is setup]({% post_url 2016-06-07-setting-up-your-environment %}).

  1. [Generate your Rails application](#generating-your-rails-application)
  1. [Install GeoConcerns](#install-geoconcerns)
  1. [Install RSpec](#install-rspec)

<hr>

### Generating your Rails application

For more information about generating a Rails application see the [Getting Started with Rails](http://guides.rubyonrails.org/getting_started.html) guide.

  1. Create a new Rails application

     ```sh
     $ rails new your_app_name
     ```

  1. Switch to its folder

     ```sh
     $ cd your_app_name
     ```

  1. Run the rails server.

     ```sh
     $ rails s -b 0.0.0.0
     ```

     We are running the Rails server with the "-b" option which is binding the server to the 0.0.0.0 IP address. This is only necessary if your are running the application on your Vagrant virtual machine.
     {: .flash-alert}

     Now you can visit the Rails application at [http://127.0.0.1:3000](http://127.0.0.1:3000). You should see Yay! You're on Rails!" CTRL + c will stop server.

     ![rails_welcome](http://guides.rubyonrails.org/images/getting_started/rails_welcome.png "Welcome aboard!")

  1. *Optional* Initialize your git repository and commit your changes

     ```sh
     $ git init
     $ git add .
     $ git commit -m 'initial commit of Rails application'
     ```

<hr>

### Install GeoConcerns

  1. Add CurationConcerns and GeoConcerns to your `Gemfile`

     ```ruby
     # In ./Gemfile
     gem 'curation_concerns', '1.5.0'
     gem 'geo_concerns', '0.0.9'
     ```

  1. Install required gems and their dependencies

     ```sh
     $ bundle install
     ```

  1. Run the CurationConcerns generator

     ```sh
     $ rails g curation_concerns:install
     ```

  1. Run the GeoConcerns generator

     ```sh
     $ rails generate geo_concerns:install
     ```

  1. Run database migrations

     ```sh
     $ rake db:migrate
     ```


     Quick tip: All of these tasks (1 - 5) are included as part of template to generate a new GeoConcerns application. To run that generator just run:
     {: .flash-notice}

     ```sh
     $ rails new app-name -m https://raw.githubusercontent.com/projecthydra-labs/geo_concerns/master/template.rb
     ```

  1. Now start your Rails application again and navigate to [http://127.0.0.1:3000](http://127.0.0.1:3000). You should see the GeoConcerns homepage.

     ```sh
     $ rails s -b 0.0.0.0
     ```

  1. *Optional* Commit your work

     ```sh
     $ git add .
     $ git commit -m 'installed CurationConcerns and GeoConcerns'
     ```

    
     Great job for making it this far. You now have a working GeoConcerns application!
     {: .flash-success}

### Install RSpec
[RSpec](http://rspec.info/) is a behavior-driven development framework for Ruby. It is the recommended way to test your application and is used by both the CurationConcerns and GeoConcerns projects.

  1. Add `rspec-rails` to both the `:development` and `:test` groups in the `Gemfile`

     ```sh
     # In ./Gemfile
     group :development, :test do
       gem 'rspec-rails', '~> 3.0'
     end 
     ```

  1. Download and install RSpec

     ```sh
     $ bundle install
     ```

  1. Initialize the spec/ directory (where specs will reside) with

     ```sh
     $ rails generate rspec:install
     ```

  1. Run your tests (specs) by running

     ```sh
     $ bundle exec rspec
     ```

     Writing tests for your application is outside the scope of this guide, but there are plenty of great examples out there. Check out the <a href="http://robots.thoughtbot.com/how-we-test-rails-applications">Thoughtbot blog</a>.
     {: .flash-notice}

  1. *Optional* Commit your work

     ```sh
     $ git add .
     $ git commit -m 'Installed RSpec'
     ```

### Next Steps

So far you have a working GeoConcerns application with a test framework installed. Now we'll start the app and walk through some of the features.

<div class='flash-notice'>
  <a href="{% post_url 2016-06-07-starting-the-application %}">Next → Part 3 - Starting the application</a>
</div>