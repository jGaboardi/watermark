watermark
=========

An IPython magic extension for printing date and time stamps, version numbers, and hardware information.
<br>


#### Sections

- [Examples](#examples)
- [Installation and updating](#installation-and-updating)
- [Usage](#usage)
- [Changelog](#changelog)

<br>

## Examples
[[top](#sections)]

![](https://github.com/rasbt/watermark/blob/master/images/ex1.png)

![](https://github.com/rasbt/watermark/blob/master/images/ex2.png)

![](https://github.com/rasbt/watermark/blob/master/images/ex3.png)

More examples can be found in this [IPython notebook](http://nbviewer.ipython.org/github/rasbt/watermark/blob/master/docs/watermark.ipynb).

<br>

## Installation and updating
[[top](#sections)]

The `watermark` line magic can be installed by executing

    %install_ext https://raw.githubusercontent.com/rasbt/watermark/master/watermark.py

<br>

## Usage
[[top](#sections)]

After successful installation, the `watermark` magic extension can be loaded via:

	%load_ext watermark

<br>

To get an overview of all available commands, type:

	%watermark?

<br>



	%watermark [-a AUTHOR] [-d] [-n] [-t] [-z] [-u] [-c CUSTOM_TIME] [-v]
	                 [-p PACKAGES] [-h] [-m] [-g]


	IPython magic function to print date/time stamps
	and various system information.

		watermark version 1.2.3

		optional arguments:
		  -a AUTHOR, --author AUTHOR
		                        prints author name
		  -d, --date            prints current date as YYYY-MM-DD
		  -n, --datename        prints date with abbrv. day and month names
		  -t, --time            prints current time as HH-MM-DD
		  -z, --timezone        appends the local time zone
		  -u, --updated         appends a string "Last updated: "
		  -c CUSTOM_TIME, --custom_time CUSTOM_TIME
		                        prints a valid strftime() string
		  -v, --python          prints Python and IPython version
		  -p PACKAGES, --packages PACKAGES
		                        prints versions of specified Python modules and
		                        packages
		  -h, --hostname        prints the host name
		  -m, --machine         prints system and machine info
		  -g, --githash         prints current Git commit hash
		  -w, --watermark       prints the current version of watermark


<br>

## Changelog
[[top](#sections)]

#### v. 1.2.3 (Jan 29, 2016)
- Changed date format to the unambiguous ISO-8601 format
- Ditched the deprecated %install_ext function and made watermark a proper Python package
- Released the new version under a more permissive newBSD [license](./LICENSE)

#### v. 1.2.2 (Jun 17, 2015)
- Changed the default date-format of `-d`, `--date` to MM/DD/YYYY, the format DD/MM/YYYY can be used via the shortcut `-e`, `--eurodate`.

#### v. 1.2.1 (Mar 3, 2015)
- Small bugfix to allow custom time string formatting.

#### v. 1.2.0 (Oct 01, 2014)
- `--watermark` command added to print the current version of watermark.
- Print author name on a separate line
- Fixed bug that day takes the same value as the minute if the `-n` flag is used.
