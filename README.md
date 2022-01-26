# Thumbalizr (PHP)

[![Git](https://app.soluble.cloud/api/v1/public/badges/4790d3cd-3809-4ff1-ab37-816563524deb.svg?orgId=234270307752)](https://app.soluble.cloud/repos/details/github.com/juliensobrier/thumbalizr-php?orgId=234270307752)  

Thumbalizr (https://www.thumbalizr.com/) is a web service to easily embed live screenshots of any URL in your website. Thumbalizr has full support for Flash, JavaScript, CSS, & HTML5.

The latest API version is detailed at https://thumbalizr.com/api/documentation.



## Requirements

    PHP 5.1.6 or abaove
    PhpUnit 3.3.5 or above (to run unit tests)


## Use Thumbalizr

	### Install manually
	git clone https://github.com/juliensobrier/thumbalizr-php
	include "src/thumbalizr.php"
	
	### Install with Composer
	composer.json can be found at https://raw.githubusercontent.com/juliensobrier/thumbalizr-php/master/composer.json
	run composer update: `php composer.phar update` or `php composer.phar install`
	
	include composer packages and libraries:
			
	require "vendor/autoload.php";
	
	
	### code sample
	$thumbalizr = new Thumbalizr('MY_KEY', 'MY_SECRET');

	$url = $thumbalizr->url('https://www.google.com/');
	echo("$url\n");

	$res = $thumbalizr->download_wait($url, "google.png");
	echo($res[0]);


## Contributing to Browshot
 
* Check out the latest master to make sure the feature hasn't been implemented or the bug hasn't been fixed yet
* Check out the issue tracker to make sure someone already hasn't requested it and/or contributed it
* Fork the project
* Start a feature/bugfix branch
* Commit and push until you are happy with your contribution
* Make sure to add tests for it. This is important so I don't break it in a future version unintentionally.
* Please try not to mess with the Rakefile, version, or history. If you want to have your own version, or is otherwise necessary, that is fine, but please isolate to its own commit so I can cherry-pick around it.

## Copyright

Copyright (c) 2019 Julien Sobrier
