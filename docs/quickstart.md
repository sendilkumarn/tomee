index-group=Unrevised
type=page
status=published
title=Quickstart
~~~~~~
<a name="Quickstart-Installation"></a>
# Installation


To install OpenEJB, simply [download the latest binary](downloads.html)
 and unpack your zip or tar.gz into the directory where you want OpenEJB to
live.

Windows users can download the zip and unpack it with the WinZip program.

Linux users can download the tar.gz and unpack it with the following
command:

*tar xzvf openejb-3.0.tar.gz*


Congratulations, you've installed OpenEJB.

If you've unpacked OpenEJB into the directory C:\openejb-3.0, for example,
then this directory is your OPENEJB_HOME directory. The OPENEJB_HOME
directory is referred to in various parts of the documentation, so it's
good to remember where it is.

<a name="Quickstart-UsingOpenEJB"></a>
# Using OpenEJB


Now all you need to do is move to the bin directory in OPENEJB_HOME, the
directory where OpenEJB was unpacked, and type:

*openejb*

For Windows users, that looks like this:

*C:\openejb-3.0> bin\openejb*

For UNIX/Linux/Mac OS X users, that looks like this:

`[user@host openejb-3.0](user@host-openejb-3.0.html)
# ./bin/openejb`

You really only need to know two commands to use OpenEJB, [deploy](openejbx30:deploy-tool.html)
 and [start|OPENEJBx30:Startup]
. Both are completely documented and have examples.

For help information and command options, try this:

> openejb deploy --help
> openejb start --help

For examples on using the start command and options, try this:

> openejb start --examples

That's it!

If you don't have any EJBs or clients to run, try the ubiquitous [Hello World](openejbx30:hello-world.html)
 example.

<a name="Quickstart-Jointhemailinglist"></a>
# Join the mailing list

The OpenEJB User list is where the general OpenEJB community goes to ask
questions, make suggestions, chat with other users, and keep a finger on
the pulse of the project. More information about the user list and dev list
can be found [here](mailing-lists.html)
