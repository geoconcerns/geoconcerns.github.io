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

  1. Switch to the root user

     ```sh
     $ sudo -i
     $ cd /home/vagrant
     ```

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

  1. Add GeoConcerns to your `Gemfile`. Add this line to the end:

     ```ruby
     # In ./Gemfile
     gem 'geo_concerns', git: 'https://github.com/projecthydra-labs/geo_concerns.git', branch: 'workshop'
     ```

  1. Install required gems and their dependencies

     ```sh
     $ bundle install
     ```

  1. Run the CurationConcerns generator

     ```sh
     $ rails generate curation_concerns:install -f
     ```

  1. Run the GeoConcerns generator

     ```sh
     $ rails generate geo_concerns:install -f
     ```

  1. Run database migrations

     ```sh
     $ rake db:migrate
     ```


     Quick tip: All of these tasks (1 - 5) are included as part of template to generate a new GeoConcerns application. To run that generator just run:
     {: .flash-notice}

     ```sh
     $ rails new app-name -m https://raw.githubusercontent.com/projecthydra-labs/geo_concerns/workshop/template.rb
     ```

  1. Change ActiveJob to queue adapter to inline. This is workaround for some issues with running background jobs on the Vagrant image. Add this line to the end of the development environment file:

     ```ruby
     # In ./config/environments/development.rb
     Rails.application.config.active_job.queue_adapter = :inline
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


### Next Steps

So far you have a working GeoConcerns application with a test framework installed. Now we'll start the app and walk through some of the features.

<div class='flash-notice'>
  <a href="{% post_url 2016-06-07-starting-the-application %}">Next → Part 3 - Starting the application</a>
</div>