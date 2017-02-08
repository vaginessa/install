<img src="https://avatars2.githubusercontent.com/u/514566?v=3&u=4615dfc4970d93dea5d3eaf996b7903ee6e24e20&s=140" align="right" />
---

![Logo of install](docs/logo-large.png)

Installer for **installing binary-, phar-, shell- or batch-files from local or remote** source.

| [![CircleCI branch](https://img.shields.io/circleci/project/github/clickalicious/install/master.svg)](https://circleci.com/gh/clickalicious/install) 	| [![Codacy branch grade](https://img.shields.io/codacy/grade/8c129b9effb64446a8d2d30eaf305679/master.svg)](https://www.codacy.com/app/clickalicious/install?utm_source=github.com&utm_medium=referral&utm_content=clickalicious/install&utm_campaign=Badge_Grade) 	| [![Codacy coverage](https://img.shields.io/codacy/coverage/8c129b9effb64446a8d2d30eaf305679.svg)](https://www.codacy.com/app/clickalicious/install?utm_source=github.com&utm_medium=referral&utm_content=clickalicious/install&utm_campaign=Badge_Grade) 	| [![clickalicious open source](https://img.shields.io/badge/clickalicious-open--source-green.svg?style=flat)](https://www.clickalicious.de/) 	|
|---	|---	|---	|---	|
| [![GitHub release](https://img.shields.io/github/release/clickalicious/install.svg?style=flat)](https://github.com/clickalicious/install/releases) 	| [![](https://img.shields.io/github/issues-raw/clickalicious/install.svg)](https://github.com/clickalicious/install/issues)  	| [![Issue Stats](https://img.shields.io/issuestats/i/github/clickalicious/install.svg)](https://github.com/clickalicious/install/issues) 	| [![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://opensource.org/licenses/MIT)  	|


## Table of Contents

- [Features](#features)
- [Example](#example)
- [Requirements](#requirements)
- [Philosophy](#philosophy)
- [Versioning](#versioning)
- [Roadmap](#roadmap)
- [Security-Issues](#security-issues)
- [License »](LICENSE)


## Features

 - CLI- and Composer-Interface for installing files (binary-, phar-, shell- or batch-files) from local or remote source (URL)
 - High-quality & stable codebase (following PSR standards e.g. `PSR-0,1,4`)
 - Built on top of good PHP libraries
 - PHP 7.1 & HHVM ready
 - Clean + well documented code
 - Unit-tested with a good coverage


## Example

Use `clickalicious\install` in `composer.json` context for downloading and installing a binary:
```js
{
    "require": {
        "clickalicious/install": "^0.1"
    },
    "scripts": {
        "post-install-cmd": [
            "Install\\ScriptHandler::installFiles"
        ],
        "post-update-cmd": [
            "Install\\ScriptHandler::installFiles"
        ]
    },
    "extra": {
        "install-configuration": [{
            "source": "https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar"
        }]
    }
}
```

Use `clickalicious\install` in `CLI` context for downloading and installing a binary:
```shell
> vendor/bin/install --filename=FOO
```


## Requirements

 - `PHP >= 5.6` (compatible up to version 5.6 as well as 7.1 and HHVM)


## Philosophy

This library provides a state of the art `PRNG` (**P**seudo **R**andom **N**umber **G**enerator) implementation to generate secure `Pseudo Random Numbers` with PHP. The generation is either based on `Open SSL` or `MCrypt` or as fallback on PHP's internal functionality. The library also provides a very good `Seed generator` on puplic API. If you are interested in the difference between real and pseduo randomness then you could start at [https://www.random.org/randomness/](https://www.random.org/randomness/ "https://www.random.org/randomness/").


## Versioning

For a consistent versioning i decided to make use of `Semantic Versioning 2.0.0` http://semver.org. Its easy to understand, very common and known from many other software projects.


## Roadmap

- [ ] Target stable release `1.0.0`
- [ ] `>= 90%` test coverage

[![Throughput Graph](https://graphs.waffle.io/clickalicious/Rng/throughput.svg)](https://waffle.io/clickalicious/install/metrics)


## Security Issues

If you encounter a (potential) security issue don't hesitate to get in contact with us `opensource@clickalicious.de` before releasing it to the public. So i get a chance to prepare and release an update before the issue is getting shared. Thank you!


## Participate & Share

... yeah. If you're a code monkey too - maybe we can build a force ;) If you would like to participate in either **Code**, **Comments**, **Documentation**, **Wiki**, **Bug-Reports**, **Unit-Tests**, **Bug-Fixes**, **Feedback** and/or **Critic** then please let me know as well!
<a href="https://twitter.com/intent/tweet?hashtags=&original_referer=http%3A%2F%2Fgithub.com%2F&text=Rng%20-%20Random%20number%20generator%20for%20PHP%20%40phpfluesterer%20%23Rng%20%23php%20https%3A%2F%2Fgithub.com%2Fclickalicious%2FRng&tw_p=tweetbutton" target="_blank">
  <img src="http://jpillora.com/github-twitter-button/img/tweet.png"></img>
</a>

## Sponsors

Thanks to our sponsors and supporters:

| JetBrains | Navicat |
|---|---|
| <a href="https://www.jetbrains.com/phpstorm/" title="PHP IDE :: JetBrains PhpStorm" target="_blank"><img src="https://resources.jetbrains.com/assets/media/open-graph/jetbrains_250x250.png" height="55"></img></a> | <a href="http://www.navicat.com/" title="Navicat GUI - DB GUI-Admin-Tool for MySQL, MariaDB, SQL Server, SQLite, Oracle & PostgreSQL" target="_blank"><img src="http://upload.wikimedia.org/wikipedia/en/9/90/PremiumSoft_Navicat_Premium_Logo.png" height="55" /></a>  |


###### Copyright
<div>Icons made by <a href="http://www.flaticon.com/authors/google" title="Google">Google</a> from <a href="http://www.flaticon.com" title="Flaticon">www.flaticon.com</a> is licensed by <a href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a></div>
