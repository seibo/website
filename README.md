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

The domain names [seibostudio.se](http://seibostudios.se) and www.seibostudios.se are set up to point to the IP-adress of the DigitalOcean droplet server.

Hugo and Nginx are installed on the droplet server.

This github repository is cloned on the droplet server.

A github webhook is set up to the droplet server so that the git repository on the droplet server is automatically updated and Hugo is run, whenever a push to the github repository is made.

# How to update contents

## Major changes to layout, theme or contents

Make sure you have the same version of Hugo installed on your local machine as is installed on the droplet server.

Clone the github repo and make changes locally and test them on your local machine with:
```
$ hugo server -D
```

When you're done changing and testing stuff, commit and push.

## Minor changes to contents

Making minor changes or corrections to the contents can be done directly in the web interface on github for this repository.
