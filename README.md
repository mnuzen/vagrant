
Everbridge - Site reliability Engineering Tech Exercise
======================


## Challenge

Everbridge has adopted SRE principles that requires our engineers to think of infrastructure and systems as code. Please work through the below exercise as it aims at challenging your in general SDLC practices, project design, System Administration, Config Management and Infrastructure as code.  There are many tools that serve the Config Management space so there are a lot of choices.  However,  Everbridge has standardize on Saltstack.  Using saltstack,  configure an ubuntu web webserver to yield a working web page at http://localhost:8080 with a single invocation of `vagrant up`.
 
Your deliverable is to check in your Vagrantfile along with any other code into your own git repo.  That way I can check out your code do a vagrant up and verify if your web server is working.


Directions

   * Using the supplied Vagrantfile, modify it as you wish but the leave vm.box type as is
   * Install and configure PHP-FPM
   * Install and configure NGINX to proxy web requests to PHP-FPM
   * Deploy the supplied app.php to web root
   * Services must survive a reboot (`vagrant reload`).  Minimize the use of sequencing shell scripts and instead focusing on how Saltstack will aid in accomplishing this.
