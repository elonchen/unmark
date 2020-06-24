Unmark
============

The open source to-do application for bookmarks.

**NOTICE June 15, 2020:** The new default branch is named "trunk". ✊

We offer this source code for Unmark completely free. We do so in hopes that Unmark will live on for many years even if we stop maintaining it. You can also use it for free (with a paid upgrade) at [Unmark.it](https://unmark.it/)

To support its further development please consider [subscribing to Unmark.it](https://unmark.it/), [donating via Paypal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=XSYNN4MGM826N). Or, you can contribute to the code.

- [Download the latest release](https://github.com/cdevroe/unmark/releases) - Grab the latest and greatest version of Unmark.

If you need assistance beyond what is provided in this Readme [create an issue on Github](https://github.com/cdevroe/unmark/issues). Before creating a new issue we recommend [search through the issues on GitHub](https://github.com/cdevroe/unmark/issues) to see how others have solved their problems.


## Installation

Installation of Unmark locally is easier than ever using Docker.

### Installation using Docker-Compose

- Install [Docker](http://docker.com/)
- Clone the repository or, download [the latest release](https://github.com/cdevroe/unmark/releases)
- Open Terminal and navigate to Unmark's location
- Run `docker-compose up -d` to start Unmark
- Install Unmark at localhost/setup]

To shut down the containers that run Unmark run `docker-compose down`.

### Installation using Apache, PHP, mySQL

#### Minimum Version Information

- Apache 2.x
- PHP 5.6 or greater
- mySQL 5.7 or greater

#### Common Issues with manual installs

Some common issues have been reported. Some are trying to load Unmark in a sub-directory, using different versions of PHP or Apache, or using completely different databases. While it may be possible to do so, expect issues, and we do not currently support these types of installations.

Other common things that come up:
- PHP mod_rewrite isn't enabled
- PHP mysqli extension not installed

#### Installation Instructions

#### From Zip
- Download [the latest release](https://github.com/cdevroe/unmark/releases)
- Unpack the archive into your desired location
- Rename the file `/application/config/database-sample.php` to `/application/config/database.php`
- Create a database for Unmark to use in mySQL
- Fill in proper database credentials in `/application/config/database.php`
- Point your browser to `your-local-url/setup`
- If succesfull, you'll be asked to register a username and password

#### From git repository (used for development)
- Run `git clone https://github.com/cdevroe/unmark.git` (Or, if you've forked the repo, use your URL)
- Copy the file `/application/config/database-sample.php` to `/application/config/database.php` (leave `database-sample.php` in place)
- Create a database for Unmark to use in mySQL
- Fill in proper database credentials in `/application/config/database.php`
- Run `npm install`
- Run `grunt` [more info on Grunt](http://gruntjs.com/)
    - To run Grunt you'll need to also install Ruby and the SASS gem
- Point your browser to `your-local-url/setup`
- If successful, you'll be asked to register a username and password

### Upgrading to the latest release

#### From Zip (binary)
- Download [the latest release](https://github.com/cdevroe/unmark/releases)
- Replace all Unmark files (keeping your local `/application/config/database.php` intact.)
- Navigate to `your-local-url/upgrade`
- Unmark will then make any needed database updates
- That's it!

#### From git repository
- Run `git pull origin master`
- Run `npm update` in the app's root directory
- Run `grunt` in the app's root directory
- Navigate to `your-local-url/upgrade`
- Unmark will then make any needed database updates
- That's it!

### Importing bookmarks

Unmark currently supports importing from Unmark's hosted version, any self-hosted version of Unmark, Readability, Pinboard, Delicious, Pocket and many other services. To ensure this works properly be sure that your PHP.ini file's "max_upload_size" setting is larger than the file you're trying to import.

## How to contribute to Unmark

Please consider donating. Another major way you can contribute is to report any issues you find with Unmark on Github and being as detailed as possible about the issue you're having.

Another way is to contribute your own code via Pull Requests. Here are some notes on how to do that.

### Forking and Pull Requests

- Fork [the repository on GitHub](https://github.com/cdevroe/unmark/) into your own account
- Create your own branch of the trunk branch `git checkout -b your-branch-name`
- Update your code and push those code changes back to your fork's branch `git push origin your-branch-name`
- [Submit a Pull Request](https://github.com/cdevroe/unmark/pulls) using that branch
- And please accept our _thanks_!

This makes it easy for us to test your code locally and also allows the community to have a discussion around it.

We use [Grunt](http://gruntjs.com/) to compile our SASS files into CSS and concatenate and compress our JavaScript files for use and a few other small tasks. For any updates to JavaScript or styles you will need to use Grunt too. See the Grunt web site for help.

## History

Unmark was originally created by [Colin Devroe](http://cdevroe.com/). It was a side-project called Nilai (the Indonesian word for "mark") and rebuilt from the ground up in 2013 by Plain, a small software company, which included Jeff Johns, Kyle Ruane, Tim Whitacre, Chris Fehnel, Jakub Jakubiec and Colin Devroe.

Now it is being maintained by Colin, Kyle and the community in their spare time. We still use it every day and we want it to be around forever. Please consider donating or contributing code in order to keep Unmark alive and well.

## Contributors

Currently being maintained by: [@cdevroe](https://github.com/cdevroe) and [@kyleruane](https://github.com/kyleruane).

Also contributions by [@thebrandonallen](https://github.com/thebrandonallen), [@simonschaufi](https://github.com/simonschaufi), [@williamknauss](https://github.com/williamknauss), [@hewigovens](https://github.com/hewigovens)

Extra special thanks to: [@phpfunk](https://github.com/phpfunk) (who wrote most of Unmark), [@twhitacre](https://github.com/twhitacre), [@kip9](https://github.com/kip9) (wrote the languages and migration back-up bits), [@cfehnel](https://github.com/cfehnel) (who handled support for the app).
