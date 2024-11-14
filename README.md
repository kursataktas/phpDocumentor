[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
![Qa workflow](https://github.com/phpDocumentor/phpDocumentor/workflows/Qa%20workflow/badge.svg)
![Packagist Version](https://img.shields.io/packagist/v/phpdocumentor/phpdocumentor?label=packagist%20stable)
![Packagist Pre Release Version](https://img.shields.io/packagist/vpre/phpdocumentor/phpdocumentor?label=packagist%20unstable)
[![Downloads](https://img.shields.io/packagist/dm/phpDocumentor/phpDocumentor.svg)](https://packagist.org/packages/phpDocumentor/phpDocumentor)
[![Gurubase](https://img.shields.io/badge/Gurubase-Ask%20phpDocumentor%20Guru-006BFF)](https://gurubase.io/g/phpdocumentor)


phpDocumentor
=============

What is phpDocumentor?
----------------------

phpDocumentor stands as the de-facto documentation tool for PHP projects, offering a robust solution for generating
comprehensive documentation effortlessly. By analyzing your PHP source code and DocBlock comments, phpDocumentor
generates a complete set of API documentation, making it an indispensable tool for developers striving
for clear and well-documented codebases.

Beyond its prowess in API documentation, phpDocumentor goes further by providing additional features.
It is equipped with the ability to create UML diagrams, making it a versatile tool for visualizing code structure.
Additionally, phpDocumentor offers a full-featured markup language parser, supporting both RestructuredText
and Markdown syntax. This flexibility allows you to document your project using the markup language that best suits
your preferences.

A notable feature of phpDocumentor is its capability to include parts of your API documentation directly into your
RestructuredText documentation. This integration ensures that your documentation and code remain in sync, saving you
time and effort in maintaining accurate and up-to-date project documentation.

Inspired by its predecessors, phpDocumentor 1 and JavaDoc, phpDocumentor continues to innovate, staying up-to-date with
the latest technologies and PHP language features. This commitment ensures that developers have access to the best
possible documentation experience, aligning with modern development practices.

In this guide, we will explore the various features of phpDocumentor, from its core functionality in generating
API documentation to its advanced capabilities in parsing markup languages. Whether you're a beginner or an
experienced developer, phpDocumentor is your ally in creating well-documented, maintainable,
and understandable PHP projects.

phpDocumentor v3 (Stable)
------------------------------------

v3 is the latest stable release. 

Documentation
-------------

For more detailed information, you can check our online documentation at https://docs.phpdoc.org/.

Features
--------

phpDocumentor supports the following:

* *PHP 7.0+ compatible*, full support for Namespaces, Closures and more are provided.
* *Docblock over types*, docblocks can be more explicit about types not all formats are supported by native php.
* *Shows any tag*, some tags add additional functionality to phpDocumentor (such as @link).
* *Low memory usage*, peak memory usage for small projects is less than 20MB, medium projects 40MB, and large frameworks 100MB.
to 80% on top of the mentioned processing speed increase above.
  to 80% on top of the mentioned processing speed increase above.
* *Easy template building*, if you want to make a branding you only have to call 1 task and edit 3 files.
* *Two-step process*, phpDocumentor first generates a cache with your application structure before creating the output.
  If you'd like you can use that to power your own tools or formatters!
* *Generics support*, with more static analysis in php types have become more complex. phpDocumentor understand these types. 
  And will render them as first class types.

Installation
------------

PhpDocumentor requires PHP 8.1 or higher to run.
However, code of earlier PHP versions can be analyzed.

All templates provided with phpDocumentor have support for Class diagrams based on the read code base.
This will require the application [PlantUml] to be installed on the machine running phpDocumentor.
Rendering the class diagrams using [PlantUml] is optional, and warnings about missing [PlantUml] can be ignored.
However, your documentation will contain some dead links in this case. 
Class diagram will be created with option `--setting=graphs.enabled=true`.

There are 4 ways to install phpDocumentor:

1. Using phive (recommended)
2. Using the PHAR (manual install)
3. Via [Docker]
4. Via [Composer]

### Using Phive

`$ phive install phpDocumentor --trust-gpg-keys 8AC0BAA79732DD42`

For more information about phive have a look at their [website](https://phar.io/).
Now you have phpDocumentor installed, it can be executed like this:

`php tools/phpDocumentor`

### Using the PHAR

1. Download the phar file from https://github.com/phpDocumentor/phpDocumentor/releases
2. You can execute the phar like this: `php phpDocumentor.phar`

### Via Docker

1. `$ docker pull phpdoc/phpdoc`
2. `$ docker run --rm -v $(pwd):/data phpdoc/phpdoc`

### Via Composer (not recommended)

But wait? What about composer?

Ah, you discovered our secret. There is a phpdocumentor composer package that you can use to install phpDocumentor.

However: phpDocumentor is a complex application, and its libraries are used in countless other libraries and applications (2 of our libraries have more than 150 million downloads each); and this means that the chances for a conflict between one of our dependencies and yours is high. And when I say high, it is really high.

So, because of the above: we do not endorse nor actively support installing phpDocumentor using Composer.

How to use phpDocumentor?
-------------------------

The easiest way to run phpDocumentor is by running the following command:

    $ phpdoc run -d <SOURCE_DIRECTORY> -t <TARGET_DIRECTORY>

This command will parse the source code provided using the `-d` argument and output it to the folder indicated by the `-t` argument.

phpDocumentor supports a whole range of options to configure the output of your documentation.
You can execute the following command, or check our website, for a more detailed listing of available command-line options.

    $ phpdoc run -h

Configuration file(s)
---------------------

phpDocumentor also supports the use of configuration files (named phpdoc.xml or phpdoc.dist.xml by default).
Please consult the documentation to see the format and supported options.

### Nightly builds

PhpDocumentor doesn't have nightly releases.
However, during each pipeline a phar artifact is built.
If you want to test the bleeding edge version of phpDocumentor, have a look in the [actions] section of this repository.
Each successful QA workflow has an Artifacts section at the bottom with the phar artifact built.

Contact
-------

Reaching out to us is easy, and can be done with:

* Twitter: [@phpDocumentor]
* Website: https://www.phpdoc.org
* GitHub:  https://www.github.com/phpDocumentor/phpDocumentor
* E-mail:  [mike@phpdoc.org]

[@phpDocumentor]: https://twitter.com/phpDocumentor
[v2 branch]: https://github.com/phpDocumentor/phpDocumentor/tree/2.9
[Graphviz]: https://www.graphviz.org/download/
[actions]: https://github.com/phpDocumentor/phpDocumentor/actions?query=workflow%3A%22Qa+workflow%22+is%3Asuccess
[Docker]: https://hub.docker.com/r/phpdoc/phpdoc/
[Composer]: https://getcomposer.org/
[mike@phpdoc.org]: mailto:mike@phpdoc.org
