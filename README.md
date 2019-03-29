# Readme file for Seibo website

The Seibo website is created and maintained with the following tools:

 * [Hugo](https://gohugo.io), a static website generator, installed with:
```
$ sudo apt-get install hugo
```
 * [Nginx](https://www.nginx.com) installed with:
```
$ sudo apt-get install nginx
```
 * This github repository which contains this README.md file, the Hugo website config, theme and contents files.
 * A [DigitalOcean](https://www.digitalocean.com) droplet server.

# Setup

The website is maintained in the git project [https://github.com/seibo/www.seibostudios.se].

The project is cloned on the droplet server **seibo-01** and the static pages are served from /var/www/website/www.seibostudios.se/public.

The domain names [seibostudio.se](http://seibostudios.se) and www.seibostudios.se are set up to point to the IP-adress of the DigitalOcean droplet server.

Hugo and Nginx are installed on the droplet server.

## Todo

Set up a github webhook to ping the droplet server whenever a push to master is done to the github repository, and add a script that then rebuilds the website on the droplet server. Possibly by using webhook by adnanh.

See:

 * https://github.com/adnanh/webhook
 * https://developer.github.com/webhooks/

# How to update contents

## Major changes to layout, theme or contents

Make sure you have the same version of Hugo installed on your local machine as is installed on the droplet server.

Clone the github repo and make changes locally and test them on your local machine with:
```
$ hugo server -D
```

When you're done changing and testing stuff, commit and push.
