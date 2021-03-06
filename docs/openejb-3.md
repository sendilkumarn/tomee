index-group=Unrevised
type=page
status=published
title=OpenEJB 3
~~~~~~

<a name="OpenEJB3-Past,Present,andFuture"></a>
# Past, Present, and Future

The goal of OpenEJB 3 is to merge our past, present, and future into one
codebase.  OpenEJB 3 will take the excellent features in OpenEJB 1.0
(tomcat integration, testability, embeddibility, ease of use, etc), move
towards an IoC architecture based on Gbean.org and Spring, bring in the
OpenEJB 2 code, and implement the EJB 3.0 specification.

<a name="OpenEJB3-ThePlan"></a>
# The Plan

We will start on OpenEJB 3 by taking the 1.0 code (pretty much the same as
0.9.2), merging in the 2.0 code, and ensuring that the entire time the code
we write is code you can use!  We will never drop a feature, even
temporarily.  We will start from code that users are now using and always
keep, maintain, and improve those features as we add new features. 
Releasing early and often.

<a name="OpenEJB3-Past"></a>
## Past

OpenEJB 1.0 (from 0.9.2 lineage) has some great features and many people
that depend on them.  Tomcat integration, Collapsed EARs, Container Driven
Testing, easy embedding, and other features make OpenEJB a unique EJB
implementation.  We're going to take this code, kill all the static
old-school techniques, modernize it with and IoC architecture based on the
gbean.org kernel.  The gbean kernel is an IoC kernel compatible with both
Spring and Geronimo.  

<a name="OpenEJB3-Present"></a>
## Present

OpenEJB 2.0 is an awesome fast implementation of EJB 2.1 that runs in
Apache Geronimo.  As the gbean.org kernel is both Spring and Geronimo
compatible, it provides a great way for us to take the Geronimo-compatible
EJB containers and deployers in OpenEJB 2 and start hammering them out and
releasing them to long-time OpenEJB users.  It will also allow people using
OpenEJB to start experimenting with Spring's sophisticated IoC features.

<a name="OpenEJB3-Future"></a>
## Future

EJB 3.0 is a new direction for EJB and we're going to do it with style.  A
focus on simplicity is where OpenEJB shines.  Combining the EJB 3.0
Simplified specification with our existing lightweight features, like
Container Driven Testing, is just the beginning.  We plan to go way beyond
the planned additions and into areas the J2EE spec groups won't go such as
deployment descriptors with attributes, simpler packaging, more flexible
classloader setup, more powerful IoC support, simpler web services support
and more.

<a name="OpenEJB3-ReleaseonDayOne"></a>
# Release on Day One

Keep it working, keep it progressing, keep releasing.  The 3.0 version
number won't be the finishing line, but the starting line.  Our work will
start out as 3.0 on day one and keep incrementing the version number as we
get further along our feature list.  The EJB 3.0 spec is not completed and
the OpenEJB 3.0 code line will be equally dynamic and best suited for
adventurous developers who enjoy reading release notes and participating on
user lists.  There will be an incredible focus on keeping things stable
enough to use the entire time as we work towards feature completion.  

The effect of all this is that you get a fixed-up, far more extensible,
version of the code you are already using delivered to you right away.
