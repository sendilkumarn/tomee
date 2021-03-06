index-group=Testing Techniques
type=page
status=published
title=Embedded Configuration
~~~~~~

<a name="EmbeddedConfiguration-Defaults,OverridesandOrder"></a>
#  Defaults, Overrides and Order

When booting up OpenEJB for testing via the `LocalInitialContextFactory`
or the newer `EJBContainer.createEJBContainer()` API part of EJB 3.1 there
is quite a bit of flexibility to how things are configured.

OpenEJB will function fine with no configuration at all and will happily
create things as needed and select defaults for everything.  So in a real
sense configuration is all about overriding those defaults.  There are
several places to put your overrides and an a specific order how they are
applied.  Here they are in order of preference; 1 = highest, 5 = lowest.

{row
{span8
**InitialContext**

1. InitialContext properties
1. jndi.properties from the classpath
1. System properties
1. openejb.xml declarations/properties
1. service-jar.xml declarations/properties (internal concept)
}

{span8
**EJBContainer API**
1. EJBContainer.createEJBContainer(Map) entries
1. System properties
1. openejb.xml declarations/properties
1. service-jar.xml declarations/properties (internal concept)

}
}

It opens up some interesting possibilities in how you configure your
environment.  You could do 100% of your configuration in your test case via
InitialContext propertes, or you could do say 80% in a jndi.properties file
or openejb.xml file and 20% in your test case via InitialContext
properties.  You can put 100% of your configuration in a `jndi.properties` or
`openejb.xml` file and override them via `InitialContext` properties.

You can manage the properties how you wish and there is no need for
redundant definitions if you do not want them.

<a name="EmbeddedConfiguration-Whatisconfigurable?"></a>
#  What is configurable?

Everything you can configure via an openejb.xml (minus the <Deployment>
element) can be configured/overridden via properties. See [Configuring Containers in Tests](configuring-containers-in-tests.html)
 and [Configuring DataSources in Tests](configuring-datasources-in-tests.html).

Everything in your logging.properties can be configured/overridden via
properties.  See [Configuring Logging in Tests](configuring-logging-in-tests.html).

The properties of persistence units declared in a persistence.xml can be
configured/overridden via properties.  See [Configuring PersistenceUnits in Tests](configuring-persistenceunits-in-tests.html).

OpenEJB has many flags that can also be set as properties.  See [OpenEJB Properties](properties-listing.html)
 for details on those.

<a name="EmbeddedConfiguration-ExampleofusingInitialContextproperties"></a>
# Example of using InitialContext properties


    Properties p = new Properties();
    
    // set the initial context factory
    p.put("java.naming.factory.initial ", "org.apache.openejb.client.LocalInitialContextFactory");
    
    // change some logging
    p.put("log4j.category.OpenEJB.options ", " debug");
    p.put("log4j.category.OpenEJB.startup ", " debug");
    p.put("log4j.category.OpenEJB.startup.config ", " debug");
    
    // create some resources
    p.put("movieDatabase", "new://Resource?type=DataSource");
    p.put("movieDatabase.JdbcDriver ", " org.hsqldb.jdbcDriver");
    p.put("movieDatabase.JdbcUrl ", " jdbc:hsqldb:mem:moviedb");
    
    // override properties on your "movie-unit" persistence unit
    p.put("movie-unit.hibernate.dialect ", "org.hibernate.dialect.HSQLDialect");
    
    // set some openejb flags
    p.put("openejb.jndiname.format ", " {ejbName}/{interfaceClass}");
    p.put("openejb.descriptors.output ", " true");
    p.put("openejb.validation.output.level ", " verbose");
    
    InitialContext initialContext = new InitialContext(p);


<a name="EmbeddedConfiguration-Exampleofusingjndi.properties"></a>
# Example of using jndi.properties

Here's an example of the same properties being specified via a
`jndi.properties file`.  This file just needs to be placed in the classpath,
not in a subdirectory of a path in the classpath such as META-INF, but at
the root of any of the paths in the classpath.

    # set the initial context factory
    java.naming.factory.initial = org.apache.openejb.client.LocalInitialContextFactory
    
    # change some logging
    log4j.category.OpenEJB.options = debug
    log4j.category.OpenEJB.startup = debug
    log4j.category.OpenEJB.startup.config = debug
    
    # create some resources
    movieDatabase = new://Resource?type=DataSource
    movieDatabase.JdbcDriver = org.hsqldb.jdbcDriver
    movieDatabase.JdbcUrl = jdbc:hsqldb:mem:moviedb
    
    # override properties on your "movie-unit" persistence unit
    movie-unit.hibernate.dialect = org.hibernate.dialect.HSQLDialect
    
    # set some openejb flags
    openejb.jndiname.format = {ejbName}/{interfaceClass}
    openejb.descriptors.output = true
    openejb.validation.output.level = verbose


Then OpenEJB can be booted via the `InitialContext` as normal.  Properties
can still be used to override any of the above properties:


    Properties p = new Properties();
    
    p.put("openejb.validation.output.level ", " medium");
    
    InitialContext initialContext = new InitialContext(p);
