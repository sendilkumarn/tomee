index-group=Configuration
type=page
status=published
title=JNDI Names
~~~~~~

<a name="JNDINames-What'sMyBean'sJNDIName?"></a>
# What's My Bean's JNDI Name?
There are two things to keep in mind before you start reading:
       
1   OpenEJB provides a default JNDI name to your EJB.     
2   You can customize the JNDI name.

<a name="JNDINames-DefaultJNDIname"></a>
## Default JNDI name 
The default JNDI name is in the following format:

    {deploymentId}{interfaceType.annotationName}

Lets try and understand the above format. Both *deploymentId* and
*interfaceType.annotationName* are pre-defined variables. There are other
pre-defined variables available which you could use to customize the JNDI
name format.

<a name="JNDINames-JNDINameFormatting"></a>
#  JNDI Name Formatting

The *openejb.jndiname.format* property allows you to supply a template for
the global JNDI names of all your EJBs.  With it, you have complete control
over the structure of the JNDI layout can institute a design pattern just
right for your client apps.  See the [Service Locator](service-locator.html)
 doc for clever ways to use the JNDI name formatting functionality in
client code.
<table class="mdtable">
<tr><td>variable</td><td>	 description</td></tr>
<tr><td>moduleId</td><td>	 Typically the name of the ejb-jar file<br> or the <ejb-jar id=""> id value if specified</td></tr>
<tr><td>ejbType</td><td>	 STATEFUL, STATELESS, BMP_ENTITY, CMP_ENTITY, or MESSAGE_DRIVEN</td></tr>
<tr><td>ejbClass</td><td>	 for a class named org.acme.superfun.WidgetBean results in org.acme.superfun.WidgetBean</td></tr>
<tr><td>ejbClass.simpleName</td><td>	 for a class named org.acme.superfun.WidgetBean results in WidgetBean</td></tr>
<tr><td>ejbClass.packageName</td><td>	 for a class named org.acme.superfun.WidgetBean results in org.acme.superfun</td></tr>
<tr><td>ejbName</td><td>	 The ejb-name as specified in xml or via the 'name' attribute in an @Stateful, @Stateless, or @MessageDriven annotation</td></tr>
<tr><td>deploymentId</td><td>	 The unique system id for the ejb. Typically the ejbName unless specified in the openejb-jar.xml or via changing the openejb.deploymentId.format</td></tr>
<tr><td>interfaceType</td><td>	 see interfaceType.annotationName</td></tr>
<tr><td>interfaceType.annotationName</td><td>	 Following the EJB 3 annotations @RemoteHome, @LocalHome, @Remote and @Local
RemoteHome (EJB 2 EJBHome)
LocalHome (EJB 2 EJBLocalHome)
Remote (EJB 3 Business Remote)
Local (EJB 3 Business Local)
Endpoint (EJB webservice endpoint)</td></tr>
<tr><td>interfaceType.annotationNameLC</td><td>	 This is the same as interfaceType.annotationName, but all in lower case.</td></tr>
<tr><td>interfaceType.xmlName</td><td>	 Following the ejb-jar.xml descriptor elements <home>, <local-home>, <business-remote>, <business-local>, and <service-endpoint>:
home (EJB 2 EJBHome)
local-home (EJB 2 EJBLocalHome)
business-remote (EJB 3 Business Remote)
business-local (EJB 3 Business Local)
service-endpoint (EJB webservice endpoint)</td></tr>
<tr><td>interfaceType.xmlNameCc</td><td>	 Camel-case version of interfaceType.xmlName:
Home (EJB 2 EJBHome)
LocalHome (EJB 2 EJBLocalHome)
BusinessRemote (EJB 3 Business Remote)
BusinessLocal (EJB 3 Business Local)
ServiceEndpoint (EJB webservice endpoint)</td></tr>
<tr><td>interfaceType.openejbLegacyName</td><td>Following the OpenEJB 1.0 hard-coded format:
(empty string) (EJB 2 EJBHome)
Local (EJB 2 EJBLocalHome)
BusinessRemote (EJB 3 Business Remote)
BusinessLocal (EJB 3 Business Local)
ServiceEndpoint (EJB webservice endpoint)</td></tr>
<tr><td>interfaceClass</td><td>	
(business) for a class named org.acme.superfun.WidgetRemote results in org.acme.superfun.WidgetRemote<br>
(home) for a class named org.acme.superfun.WidgetHome results in org.acme.superfun.WidgetHome</td></tr>
<tr><td>interfaceClass.simpleName</td><td>
(business) for a class named org.acme.superfun.WidgetRemote results in WidgetRemote
(home) for a class named org.acme.superfun.WidgetHome results in WidgetHome</td></tr>
<tr><td>interfaceClass.packageName</td><td>	 for a class named org.acme.superfun.WidgetRemote results in org.acme.superfun</td></tr>
</table>
<a name="JNDINames-SettingtheJNDIname"></a>
#  Setting the JNDI name

It's possible to set the desired jndi name format for the whole server
level, an ejb-jar, an ejb, an ejb's "local" interface
(local/remote/local-home/home), and for an individual interface the ejb
implements.  More specific jndi name formats act as an override to any more
general formats.  The most specific format dictates the jndi name that will
be used for any given interface of an ejb.  It's possible to specify a
general format for your server, override it at an ejb level and override
that further for a specific interface of that ejb.

<a name="JNDINames-ViaSystemproperty"></a>
## Via System property

The jndi name format can be set on a server level via a _system property_,
for example:


    $ ./bin/openejb start
    -Dopenejb.jndiname.format=\{ejbName}/\{interfaceClass}"


As usual, other ways of specifying system properties are via the
conf/system.properties file in a standalone server, or via the
InitialContext properties when embedded.

<a name="JNDINames-Viapropertiesintheopenejb-jar.xml"></a>
## Via properties in the openejb-jar.xml

It's possible to set the openejb.jndiname.format for an ejb-jar jar in a
META-INF/openejb-jar.xml file as follows:


    <openejb-jar>
      <properties>
         openejb.deploymentId.format = {ejbName}
         openejb.jndiname.format = {deploymentId}{interfaceType.annotationName}
      </properties>
    </openejb-jar>


<a name="JNDINames-Viathe<jndi>tagforaspecificejb"></a>
## Via the <jndi> tag for a specific ejb

The following sets the name specifically for the interface
org.superbiz.Foo.


    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <jndi name="foo" interface="org.superbiz.Foo"/>  
      </ejb-deployment>
    </openejb-jar>


Or more generally...


    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <jndi name="foo" interface="Remote"/> 
      </ejb-deployment>
    </openejb-jar>


Or more generally still...


    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <jndi name="foo"/> 
      </ejb-deployment>
    </openejb-jar>


The 'name' attribute can still use templates if it likes, such as: 


    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <jndi name="ejb/{interfaceClass.simpleName}" interface="org.superbiz.Foo"/> 
      </ejb-deployment>
    </openejb-jar>


<a name="JNDINames-Multiple<jndi>tags"></a>
###  Multiple <jndi> tags

Multiple <jndi> tags are allowed making it possible for you to be as
specific as you need about the jndi name of each interface or each logical
group of iterfaces (Local, Remote, LocalHome, RemoteHome).  

Given an ejb, FooBean, with the following interfaces:
 - business-local: org.superbiz.LocalOne
 - business-local: org.superbiz.LocalTwo
 - business-remote: org.superbiz.RemoteOne
 - business-remote: org.superbiz.RemoteTwo
 - home: org.superbiz.FooHome
 - local-home: org.superbiz.FooLocalHome

The following four examples would yield the same jndi names.  The intention
with these examples is to show the various ways you can isolate specific
interfaces or types of interfaces to gain more specific control on how they
are named.

    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <jndi name="LocalOne" interface="org.superbiz.LocalOne"/>
        <jndi name="LocalTwo" interface="org.superbiz.LocalTwo"/>
        <jndi name="RemoteOne" interface="org.superbiz.RemoteOne"/>
        <jndi name="RemoteTwo" interface="org.superbiz.RemoteTwo"/>
        <jndi name="FooHome" interface="org.superbiz.FooHome"/>
        <jndi name="FooLocalHome" interface="org.superbiz.FooLocalHome"/>
      </ejb-deployment>
    </openejb-jar>

Or

    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <!-- applies to LocalOne and LocalTwo -->
        <jndi name="{interfaceClass.simpleName}" interface="Local"/> 
    
        <!-- applies to RemoteOne and RemoteTwo -->
        <jndi name="{interfaceClass.simpleName}" interface="Remote"/> 
    
        <!-- applies to FooHome -->
        <jndi name="{interfaceClass.simpleName}" interface="RemoteHome"/> 
    
        <!-- applies to FooLocalHome -->
        <jndi name="{interfaceClass.simpleName}" interface="LocalHome"/> 
      </ejb-deployment>
    </openejb-jar>

Or

    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <!-- applies to RemoteOne, RemoteTwo, FooHome, and FooLocalHome -->
        <jndi name="{interfaceClass.simpleName}"/>

        <!-- these two would count as an override on the above format -->
        <jndi name="LocalOne" interface="org.superbiz.LocalOne"/>
        <jndi name="LocalTwo" interface="org.superbiz.LocalTwo"/>
      </ejb-deployment>
    </openejb-jar>

or
    
    <openejb-jar>
      <ejb-deployment ejb-name="FooBean">
        <!-- applies to LocalOne, LocalTwo, RemoteOne, RemoteTwo, FooHome, and FooLocalHome -->
        <jndi name="{interfaceClass.simpleName}"/> 
      </ejb-deployment>
    </openejb-jar>


<a name="JNDINames-ChangingtheDefaultSetting"></a>
# Changing the Default Setting

*You are responsible for ensuring the names don't conflict.*  
 
<a name="JNDINames-Conservativesettings"></a>
### Conservative settings

A very conservative setting such as    

 "{deploymentId}/{interfaceClass}"    

would guarantee that each and every single interface is bound to JNDI.	If
your bean had a legacy EJBObject interface, three business remote
interfaces, and two business local interfaces, this pattern would result in    
*six* proxies bound into JNDI.      
<pre>  
 - {deploymentId}/{interfaceClass.simpleName}    
 - {moduleId}/{ejbName}/{interfaceClass}    
 - {ejbName}/{interfaceClass}    
 - {moduleId}/{ejbClass}/{interfaceClass}    
 - {ejbClass}/{interfaceClass}    
 - {ejbClass}/{interfaceClass.simpleName}    
 - {ejbClass.simpleName}/{interfaceClass.simpleName}    
 - {interfaceClass}/{ejbName}    
</pre>
Bordeline optimistic:    
<pre>
 - {moduleId}/{interfaceClass}    
 - {interfaceClass}    
</pre>
The above two settings would work if you the interface wasn't shared by
other beans.

<a name="JNDINames-Pragmaticsettings"></a>
### Pragmatic settings    

A more middle ground setting such as
"{deploymentId}/{interfaceType.annotationName}" would guarantee that at
least one proxy of each interface type is bound to JNDI.  If your bean had
a legacy EJBObject interface, three business remote interfaces, and two
business local interfaces, this pattern would result in *three* proxies
bound into JNDI: one proxy dedicated to your EJBObject interface; one proxy
implementing all three business remote interfaces; one proxy implementing
the two business local interfaces.

Similarly pragmatic settings would be    
<pre>
 - {moduleId}/{ejbClass}/{interfaceType.annotationName}    
 - {ejbClass}/{interfaceType.xmlName}    
 - {ejbClass.simpleName}/{interfaceType.xmlNameCc}    
 - {interfaceType}/{ejbName}    
 - {interfaceType}/{ejbClass}    
</pre>
<a name="JNDINames-Optimisticsettings"></a>
### Optimistic settings

A very optimistic setting such as "{deploymentId}" would guarantee only
one proxy for the bean will be bound to JNDI.  This would be fine if you
knew you only had one type of interface in your beans.	For example, only
business remote interfaces, or only business local interfaces, or only an
EJBObject interface, or only an EJBLocalObject interface.

If a bean in the app did have more than one interface type, one business
local and one business remote for example, by default OpenEJB will reject
the app when it detects that it cannot bind the second interface.  This
strict behavior can be disabled by setting the
*openejb.jndiname.failoncollision* system property to _false_.	When this
property is set to false, we will simply log an error that the second proxy
cannot be bound to JNDI, tell you which ejb is using that name, and
continue loading your app.

Similarly optimistic settings would be:    
<pre>
 - {ejbName}    
 - {ejbClass}    
 - {ejbClass.simpleName}    
 - {moduleId}/{ejbClass.simpleName}    
 - {moduleId}/{ejbName}    
</pre>
<a name="JNDINames-AdvancedDetailsonEJB3.0BusinessProxies(thesimplepart)"></a>
### Advanced Details on EJB 3.0 Business Proxies (the simple part)

If you implement your business interfaces, your life is simple as your
proxies will also implement your business interfaces of the same type. 
Meaning any proxy OpenEJB creates for a business local interface will also
implement your other business local interfaces.  Similarly, any proxy
OpenEJB creates for a business remote interface will also implement your
other business remote interfaces.

<a name="JNDINames-AdvancedDetailsonEJB3.0BusinessProxies(thecomplicatedpart)"></a>
### Advanced Details on EJB 3.0 Business Proxies (the complicated part)

*Who should read?*    
Read this section of either of these two apply to you:    
 - You do not implement your business interfaces in your bean class    
 - One or more of your business remote interfaces extend from javax.rmi.Remote

If neither of these two items describe your apps, then there is no need to
read further.  Go have fun.

<a name="JNDINames-Notimplementingbusinessinterfaces"></a>
### Not implementing business interfaces

If you do not implement your business interfaces it may not be possible for
us to implement all your business interfaces in a single interface. 
Conflicts in the throws clauses and the return values can occur as detailed [here](multiple-business-interface-hazzards.html)
.  When creating a proxy for an interface we will detect and remove any
other business interfaces that would conflict with the main interface.

<a name="JNDINames-Businessinterfacesextendingjavax.rmi.Remote"></a>
### Business interfaces extending javax.rmi.Remote

Per spec rules many runtime exceptions (container or connection related)
are thrown from javax.rmi.Remote proxies as java.rmi.RemoteException which
is not a runtime exception and must be throwable via the proxy as a checked
exception. The issue is that conflicting throws clauses are actually
removed for two interfaces sharing the same method signature.  For example
two methods such as these:    
 - InterfaceA: void doIt() throws Foo;   
 - InterfaceB: void doIt() throws RemoteException;    

can be implemented by trimming out the conflicting throws clauses as
follows:    
  - Implementation: void doIt(){}    

This is fine for a bean class as it does not need to throw the RMI required
javax.rmi.RemoteException. However if we create a proxy from these two
interfaces it will also wind up with a 'doIt(){}' method that cannot throw
javax.rmi.RemoteException.  This is very bad as the container does need to
throw RemoteException to any business interfaces extending java.rmi.Remote
for any container related issues or connection issues.	If the container
attempts to throw a RemoteException from the proxies 'doIt(){}' method, it
will result in an UndeclaredThrowableException thrown by the VM.

The only way to guarantee the proxy has the 'doIt() throws RemoteException
{}' method of InterfaceB is to cut out InterfaceA when we create the proxy
dedicated to InterfaceB.
