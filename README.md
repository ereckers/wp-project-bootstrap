WP Project Bootstrap
====================

WP Project Bootstap for WordPress and [Varying-Vagrant-Vagrants] is the starting point for every new [WordPress] project at [Red Bridge Internet].

This can be run in a development environment provisioned by [Varying-Vagrant-Vagrants]. It contains [Auto Site Setup] scripts to import an active project or spin up a fresh new WordPress installation.

Getting Started
-----------

### Install Dependencies

If you don't already have [Varying-Vagrant-Vagrants] installed go here <https://github.com/Varying-Vagrant-Vagrants/VVV> and install it. The whole process involves installing VirtualBox, Vagrant, vagrant-hostupdater plugin, and cloning [Varying-Vagrant-Vagrants] to a local directory.


## Miscellaneous

### All Files Modified GIT Status
	
**Running `git status` shows (M)odified files**. VVV uses a liberal permissions scheme which is great for development, but you may have tighter permissions live. Upon your first `vagrant ssh` and `git status` you may notice that all files show as (M)odified. You can ignore permissions by running this GIT command:

	 git config core.fileMode false

### Subdirectory Install Nginx Configuration

Edit the file `vvv-nginx.conf` and add the following before the last closing tag:

	# Subdirectory install
	location /wordpress/ {
		index index.php;
		try_files $uri $uri/ /wordpress/index.php?$args;
	}

### Updating this Project

**Updates for WP Project Bootstrap** -- The way it stands now, these clones are a one time thing. This project will continue to be improved and updated, but once you clone it, it's basically yours. It's a throwaway at the moment. More thinking on allowing for updating needs to be done.

## Some Notes on Special Files

All files at the webroot are typical for the WordPress installations with these exceptions:

	/robots.txt
	/humans.txt	# something I saw that I thought was cool

You may want to place your own versions of these files in the public directory:

	/favicon.ico
	

## The Theme and Plugins

WP Project Bootstrap comes with the default WordPress Twenty series theme. Red Bridge Internet uses it's own starter theme called [feather] that is hosted on GitHub.

## Resources and Documentation

PHP Error Logs

	/tmp/php_errors.log

Websites

* [WordPress]: http://www.wordpress.org
* [Varying-Vagrant-Vagrants]: https://github.com/varying-vagrant-vagrants/vvv/wiki/Auto-site-Setup
* [feather]: https://github.com/ereckers/feather
* [Bootstrap 3]: http://getbootstrap.com
* [humans.txt]: http://humanstxt.org
* [Red Bridge Internet]: http://www.redbridgenet.com

[WordPress]: http://www.wordpress.org
[Varying-Vagrant-Vagrants]: https://github.com/Varying-Vagrant-Vagrants/VVV
[feather]: https://github.com/ereckers/feather
[Auto Site Setup]: https://github.com/varying-vagrant-vagrants/vvv/wiki/Auto-site-Setup
[WordPress]: http://www.wordpress.org
[Red Bridge Internet]: http://www.redbridgenet.com
[Bootstrap 3]: http://getbootstrap.com/
[Plugins]: https://github.com/ereckers/wp-project-bootstrap/public/wp-content/plugins
[humans.txt]: http://humanstxt.org

