index-group=Spring
type=page
status=published
title=Spring
~~~~~~
{note}
This document and the related feature is considered a prototype and will
change based on user feedback.	All comments suggestions welcome.
{note}

<a name="Spring-Introduction"></a>
# Introduction

The OpenEJB Spring integration makes all Spring defined beans injectable to
Java EE components, and all Java EE components can be injected to Spring beans. 
The injection system supports arbitrarily complex nesting (e.g., Spring
bean injected into a Java EE component, which is then injected into another
Spring bean), including:

 * @Resouce injection of any Spring bean into EJB
 * Injection of any Java EE resource into a Spring bean, including:
   ** EJB 3.0 beans
   ** EJB 3.1 Singleton Bean
   ** JDBC Connector
   ** JMS Connector
   ** JMS Queue and Topic
   ** Generic Java EE Connector (JCA)

In addition, the OpenEJB Spring integration add support for discovery and
deployment of standard Java EE packages within a Spring context, including:

 * EAR
 * EJB Jar
 * Persistence Unit
 * RAR 

*Requirements:*
 * OpenEJB 3.1+
 * Spring X.X
 * Java 1.5 or 1.6

<a name="Spring-SpringBeans"></a>
#  Spring Beans

The following beans are usable in any spring xml file.

<table class="mdtable">
<tr><th> Class </th><th> Description </th></tr>
<tr><td> org.apache.openejb.spring.ClassPathApplication </td><td> Scrapes the classpath
for all EJB, RAR, and Persistence applications, deploys them, and imports
them into the current ApplicationContext.  All applications found are
treated as one big EAR unless the _classpathAsEar_ property is set to
_false_ </td></tr>
<tr><td> org.apache.openejb.spring.Application </td><td> Scrapes an individual jar file
for EJB, RAR, and Persistence applications, deploys them, and imports them
into the current ApplicationContext.  The 'jarFile' property is required. 
The application is treated as it's own self-contained EAR, separate from
other uses of 'Application' </td></tr>
<tr><td> org.apache.openejb.spring.Resource </td><td> Allows an OpenEJB <Resource> to be
declared in the Spring ApplicationContext </td></tr>
<tr><td> org.apache.openejb.spring.OpenEJBResource </td><td> A FactoryBean that imports a
Resource from OpenEJB into the Spring ApplicationContext.  Has the
following properties: _type_ such as javax.sql.DataSource, and
_resourceId_.  In the future this bean will not be required and all OpenEJB
Resources will automatically be imported into the Spring ApplicationContext
</td></tr>
<tr><td> org.apache.openejb.spring.BmpContainer </td><td> Allows an OpenEJB BMP
<Container> to be declared in the Spring ApplicationContext.  Has the
following properties: _poolSize_ </td></tr>
<tr><td> org.apache.openejb.spring.CmpContainer </td><td> Allows an OpenEJB CMP
<Container> to be declared in the Spring ApplicationContext. </td></tr>
<tr><td> org.apache.openejb.spring.SingletonContainer </td><td> Allows an OpenEJB
Singleton <Container> to be declared in the Spring ApplicationContext.	Has
the following properties: _accessTimeout_ </td></tr>
<tr><td> org.apache.openejb.spring.StatefulContainer </td><td> Allows an OpenEJB Stateful
<Container> to be declared in the Spring ApplicationContext.  Has the
following properties: _timeOut_</td></tr>
<tr><td> org.apache.openejb.spring.StatelessContainer </td><td> Allows an OpenEJB Stateful
<Container> to be declared in the Spring ApplicationContext.  Has the
following properties: _timeOut_, _poolSize_, and _strictPooling_ </td></tr>
<tr><td> org.apache.openejb.spring.MdbContainer </td><td> Allows an OpenEJB Message-Driven
<Container> to be declared in the Spring ApplicationContext.  Has the
following properties: _resourceAdapter_, _messageListenerInterface_,
_activationSpecClass_, and _instanceLimit_ </td></tr>
<tr><td> org.apache.openejb.spring.EJB </td><td> A FactoryBean that imports an EJB from
OpenEJB into the Spring ApplicationContext.  One of these is automatically
created for each interface of each EJB, but explicit use can be nice if you
desire to import an EJB with a specific name.  Has the following
properties: _deploymentId_, _interface_ </td></tr>
</table>

<a name="Spring-Examples"></a>
# Examples

See the [Spring EJB and JPA](spring-ejb-and-jpa.html)
 page for example code and a working Spring xml file.

<a name="Spring-{anchor:problems}Problems?"></a>
# {anchor:problems} Problems?

If you are having problems with the installation, please send a message to
the OpenEJB users [mailing list](mailing-lists.html)
 containing any error message(s) and the following information:

* OpenEJB Version
* Spring Version
* Java Version (execute java -version)
* Operating System Type and Version

<a name="Spring-Limitations"></a>
# Limitations

 *JavaAgent* - OpenEJB uses OpenJPA to provide JPA and CMP persistence, and
OpenJPA currently requires a JavaAgent to function properly in a Java 1.5
environment.  OpenJPA does not require a JavaAgent in Java 1.6.  Use
Hibernate as your the provider in your persistence.xml files if you wish to
avoid this requirement.

 *EntityManager* - Having an OpenEJB created EntityManager or
EntityManagerFactory injected into Spring beans is currently not supported.
 This will be added to the next release.  A small workaround for this is to
use an EJB as a factory by adding a 'getEntityManager' method an using it
as a [Spring instance factory method](http://static.springframework.org/spring/docs/2.5.x/reference/beans.html#beans-factory-class-instance-factory-method)
.
