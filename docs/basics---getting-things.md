index-group=Unrevised
type=page
status=published
title=Basics - Getting Things
~~~~~~
<a name="Basics-GettingThings-GettingStufffromtheContainer"></a>
# Getting Stuff from the Container

Generally speaking the only way to get a [Container-Managed Resource](container-managed-resource.html)
 is via *dependency injection* or *lookup* from within a [Container-Managed Component]
.

The *unbreakable rules*.  Read these over and over again when things don't
work.

1. java:comp/env is the spec defined namespace for lookup of any [Container-Managed Resource](container-managed-resource.html)
1. java:comp/env is *empty* by default
1. java:comp/env is *read-only* at runtime
1. java:comp/env is populated by [Declaring References](declaring-references.html)
 to [Container-Managed Resource]
 via xml or annotation
1. only [Container-Managed Component](container-managed-component.html)
s, *not* their libraries, can [Declare References|Declaring References]
 via xml or annotation
1. only [Container-Managed Component](container-managed-component.html)
s, *not* their libraries, can get dependency injection of [Container-Managed Resource]
s
1. only [Container-Managed Component](container-managed-component.html)
s, *and* their libraries, may lookup from java:comp/env
1. you *must* use the *no-arg* 'new InitialContext()' constructor to
lookup something from java:comp/env
1. the annotations and xml for [Declaring References](declaring-references.html)
 are *identical* in functionality, both *always* configure lookup with
*optional* dependency injection

<a name="Basics-GettingThings-Commonmistakes,misunderstandings,andmyths"></a>
##  Common mistakes, misunderstandings, and myths

- *_"I tried it via annotation and it didn't work, so I used xml and then
it did work"_*

See rule 9.  If one form worked and the other didn't, it means you simply
made a mistake in using one versus the other.  Use what works for you, but
understand both annotations or xml will work for either lookup or injection
if used correctly.

- *_"I need to use lookups, so I can't use the annotation"_*

See rule 9.  Annotations are not just for injection, that is just how they
are typically used.  Know that when you use an annotation for injection, it
will *always* create an entry in java:comp/env.  As well you can use the
annotation at the *class level* and it will cause no dependency injection
and only the entry creation in java:comp/env.

- *_"I don't want injection, so I can't use the annotation"_*

See rule 9 and the above.  You can use the annotation at the *class level*
and it will cause no dependency injection and only the entry creation in
java:comp/env.

- *_"I tried to list java:comp/env but it's empty?!"_*

See rule 2 and rule 4.	There will be nothing in java:comp/env unless you [Declare a Reference](declaring-references.html)
 to it.  It does not matter if is a DataSource configured at the server
level, etc.  Nothing is bound into java:comp/env unless you explicitly
declare a reference to it.  The Java EE 5 TCK (Technology Compatibility
Kit) tests for this extensively and is a rule we cannot break.	Java EE 6
does finally offer some new namesaces (java:global, java:app, and
java:module) which will offer some great new options for more global-style
lookups.

- *_"I deployed the EJB but can't look it up, it's name is Foo"_*

See rule 2 and the above.  Just creating an EJB doesn't cause it to be
added to java:comp/env.  If a [Container-Managed Component](container-managed-component.html)
 wants to lookup the EJB they must [Declare a Reference|Declaring References]
 to it via the @EJB annotionation or &lt;ejb-local-ref&gt; or &lt;ejb-ref&gt; in xml. 
In Java EE 6, however, EJBs will be automatically bound to
"java:global[/&lt;app-name&gt;]/&lt;module-name&gt;/&lt;bean-name&gt;[!&lt;fully-qualified-interface-name&gt;]"
and can be looked up without declaring a reference first.

- *_"Which InitialContextFactory do I use for java:comp/env?"_*

See rule 8.  You are not allowed to use an InitialContextFactory for
java:comp/env lookups.	Setting an InitialContextFactory via
'java.naming.factory.initial' in either System properties, InitialContext
properties, or a jndi.properties file is illegal and will cause
java:comp/env lookups to fail.

- *_"My Client can't lookup the EJB from java:comp/env"_*

See rule 7.  A plain, standalone, Java application cannot use
java:comp/env. There is the official concept of a Java EE Application
Client which can be packaged in an ear and deployed into the Container.  In
practice, most people find them restrictive, cumbersome, and hard to use
and are therefore rarely employed in "real world" projects.  Most people
opt to use the non-standard, vendor-specific, approach to looking up EJBs
from their plain java clients.	In OpenEJB this can be done via either the
RemoteInitialContextFactory (for remote clients) or the
LocalInitialContextFactory (for local clients of an embedded container). 
The JNDI names can be configured as [shown here](jndi-names.html)
.

- *_"I declared the reference, but still can't look it up"_*

See all of the above and reread the rules a few times.	Always check the
log output as well.
