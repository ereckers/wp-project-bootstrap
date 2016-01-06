# WP Project Bootstrap

WP Project Bootstap for WordPress and [Varying-Vagrant-Vagrants] is the starting point for every new [WordPress] project at [Red Bridge Internet].

## Software Requirements

The whole setup relies on a few things:

* Node+NPM
* Homebrew
* Gulp
* Grunt
* Compass
* Bower

## Getting Started

Install [Varying Vagrant Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV). This is a MAMP replacement. The steps to install are under **"The First Vagrant Up"** on the Github README. Along with installing VirtualBox and Vagrant, you'll want to install the "vagrant-hostsupdater" and "vagrant-triggers" plugins.

Install @topdown's [VVV Dashboard](https://github.com/topdown/VVV-Dashboard). Just follow the 2 steps under "Instructions". It's a nicer dashboard to work with for Varying Vagrant Vagrants.

Install [Variable VVV][https://github.com/bradp/vv], a site creation tool which automates setting up new sites, setting up deployments, and more.. This is a command line site creation tool that makes setting up new sites in VVV much simpler. If you install [Homebrew](http://brew.sh/), it makes the install of this a 1 liner.

These will give you the tools to create a WordPress development environment and custom development WordPress installs.

I'll send you a command later today to create a new development site for the Religious Studies project. Then we can finish up setting up the dev site on our call.

## Getting Started

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

## Special Files

All files at the webroot are typical for the WordPress installations with these exceptions:

	/robots.txt
	/humans.txt	# something I saw that I thought was cool

You may want to place your own versions of these files in the public directory:

	/favicon.ico

## Theme and Plugins

WP Project Bootstrap comes with the default WordPress Twenty series theme. Red Bridge Internet uses it's own starter theme called [feather] that is hosted on GitHub.

## Notes

VVV Log Locations

```
/tmp/php_errors.log
```

## References

* [WordPress](http://www.wordpress.org)
* [Varying-Vagrant-Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV)
* [feather](https://github.com/ereckers/feather)
* [Auto Site Setup](https://github.com/varying-vagrant-vagrants/vvv/wiki/Auto-site-Setup)
* [WordPress](http://www.wordpress.org)
* [Red Bridge Internet](http://www.redbridgenet.com)
* [Bootstrap](http://getbootstrap.com/)
* [Plugins](https://github.com/ereckers/wp-project-bootstrap/public/wp-content/plugins)
* [humans.txt](http://humanstxt.org)

