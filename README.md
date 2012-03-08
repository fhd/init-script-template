System V init script template
=============================

A simple template for init scripts that provide the start, stop and
status commands.

Handy for [Node.js](http://http://nodejs.org/) apps and everything
else that runs itself.

Getting started
---------------

Just rename _template_ to something meaningful, set the following
three variables and you're ready to go:

### dir ###

The working directory of your process.

### user ###

The user that should execute the command.

### cmd ###

The command line to start the process.

Here's an example for an app called
[algorithms](http://algorithms.ubercode.de):

    dir="/var/apps/algorithms"
    user="node"
    cmd="node server.js"

Script usage
------------

### Start ###

Starts the app.

    /etc/init.d/algorithms start

### Stop ###

Stops the app.

    /etc/init.d/algorithms stop

### Status ###

Tells you whether the app is running. Exits with _0_ if it is and _1_
otherwise.

    /etc/init.d/algorithms status

Logging
-------

By default, standard output goes to _/var/log/scriptname.log_ and
error output to _/var/log/scriptname.err_. If you're not happy with
that, change the variables `stdout_log` and `stderr_log`.
