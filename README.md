# README

## Name

groonga-normalizer-mysql

## Description

Groonga-normalizer-mysql is a groonga plugin. It provides MySQL
compatible normalizers to groonga. They are `NormalizerMySQLGeneralCI`
and `NormalizerMySQLUnicodeCI`. `NormalizerMySQLGeneralCI` corresponds
to `utf8mb4_general_ci`.  `NormalizerMySQLUnicodeCI` corresponds to
`utf8mb4_unicode_ci`.

## Install

### Debian GNU/Linux

[Add apt-line for the groonga deb package repository](http://groonga.org/docs/install/debian.html)
and install `groonga-normalizer-mysql` package:

    % sudo aptitude -V -D -y install groonga-normalizer-mysql

### Ubuntu

[Add apt-line for the groonga deb package repository](http://groonga.org/docs/install/ubuntu.html)
and install `groonga-normalizer-mysql` package:

    % sudo aptitude -V -D -y install groonga-normalizer-mysql


### CentOS

Install `groonga-repository` package:

    % sudo rpm -ivh http://packages.groonga.org/centos/groonga-release-1.1.0-1.noarch.rpm
    % sudo yum makecache

Then install `groonga-normalizer-mysql` package:

    % sudo yum install -y groonga-normalizer-mysql

### Fedora

Install `groonga-repository` package:

    % sudo rpm -ivh http://packages.groonga.org/fedora/groonga-release-1.1.0-1.noarch.rpm
    % sudo yum makecache

Then install `groonga-normalizer-mysql` package:

    % sudo yum install -y groonga-normalizer-mysql

## Usage

First, you need to register `normalizers/mysql` plugin:

    groonga> register normalizers/mysql

Then, you can use `NormalizerMySQLGeneralCI` and
`NormalizerMySQLUnicodeCI` as normalizers:

    groonga> table_create Lexicon TABLE_PAT_KEY --default_tokenizer TokenBigram --normalizer NormalizerMySQLGeneralCI

## Dependencies

* groonga >= 3.0.0

## Mailing list

* English: [groonga-talk@lists.sourceforge.net](https://lists.sourceforge.net/lists/listinfo/groonga-talk)
* Japanese: [groonga-dev@lists.sourceforge.jp](http://lists.sourceforge.jp/mailman/listinfo/groonga-dev)

## Thanks

* Alexander Barkov \<bar@udm.net\>: The author of
  `MYSQL_SOURCE/strings/ctype-utf8.c`.
* ...

## Authors

* Kouhei Sutou \<kou@clear-code.com\>

## License

LGPLv2 only. See doc/text/lgpl-2.0.txt for details.

This program uses normalization table defined in MySQL source code. So
this program is derived work of
`MYSQL_SOURCE/strings/ctype-utf8.c`. This program is the same license
as `MYSQL_SOURCE/strings/ctype-utf8.c` and it is licensed under LGPLv2
only.
