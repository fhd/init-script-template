System V init script template
=============================

A simple template for init scripts that provide the start, stop and
status commands.

Getting started
---------------

Just rename _template_ to something meaningful, set the following
variables and you're ready to go:

### dir

The working directory of your process.

### user

The user under which to execute the command.

### cmd

The actual command line.

Here's an example for a Node.js app called
[algorithms](http://algorithms.ubercode.de):

    dir="/var/apps/algorithms"
    user="node"
    cmd="node server.js"
