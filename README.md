Unison Cronjob
==============

Unison Cronjob is an helper to schedule file synchronization using [Unison](https://github.com/bcpierce00/unison). Per default it invokes Unison every 15 minutes.

Package building
----------------

First install the packages for building:

    ~# apt-get install git devscripts

Then clone this repository:

    ~$ git clone https://github.com/philippmeisberger/unison-cronjob.git

Build the package:

    ~$ cd ./unison-cronjob/
    ~$ dpkg-buildpackage -uc -us

Installation
------------

Install Unison:

    ~# apt-get install unison-gtk

Install package:

    ~# dpkg -i ../unison-cronjob*.deb

Install missing dependencies:

    ~# apt-get -f install

Configuration
-------------

* Edit file */etc/unison-cronjob.conf* and specify the user and the Unison profile name
* Edit file */etc/cron.d/unison-cronjob* and replace "user" by your username (not root!)
