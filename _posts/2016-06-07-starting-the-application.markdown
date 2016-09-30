---
layout: walkthrough
title:  "Starting the Application - Part 3 - Walkthrough of GeoConcerns"
date:   2016-06-07 14:51:00
categories: tutorial
author: 'Eliot Jordan'
author_link: 'https://github.com/eliotjordan'
snippet: 'Starting the GeoConcerns application and loggin in. Created as part of a tutorial series given as Walkthrough of GeoConcerns'
---

## Starting the application
  1. Vagrant instructions (skip if the VM was started in part 3)
  1. Start Solr, Fedora, and Rails
  1. Create a new user

   If you have just completed parts 1 and 2, you can skip to Create a New User.
   {: .flash-notice}


### Vagrant instructions

1. If another vagrant box is running, it needs to be stopped first.

   ```sh
   $ vagrant halt
   ```

1. Navigate to the geo-concerns vagrant directory and start the machine.

   ```sh
   $ cd ../geo-concerns-demo
   $ vagrant up
   ```

1. Navigate to the geo-concerns vagrant directory and start the machine.

   ```sh
   $ cd ../geo-concerns-demo
   $ vagrant up
   ```

1. SSH into the VM

   Mac and Linux

   ```sh
   $ vagrant ssh
   ```

   Windows

   ```
   Use PuTTY
   ```

### Start the demo application

After logging into the server and navigating to the geo concerns demo directory, you will need to start the application.

```sh
$ sudo -i
$ cd /home/vagrant/demos/geo-concerns-demo
$ rails s -b 0.0.0.0
```

You can now navigate to the web pages for each of the services we just started. It might be useful to open a new browser tab for each service.

- [Demo App](http://127.0.0.1:3000)
- [Fedora](http://127.0.0.1:8984)
- [Solr](http://127.0.0.1:8983/solr)
- [GeoServer](http://127.0.0.1:8181/geoserver)

### Create a new user

Since this is a brand new application, we have to create a user in order to continue.

1. Open the demo app link in a browser tab.
1. Click on **Log in** in the upper right-hand corner.
1. Click on the **Sign up** link direcly below the **Log in** button.
1. Add an email address (can be fake) and a password. `123456` works fine.

   ![sign_up](/images/sign_up.png)
1. Click on the **Sign up** button and you're in!

<div class='flash-notice'>
  <a href="{% post_url 2016-06-07-create-an-image-work %}">Next → Create an image work</a>
</div>
