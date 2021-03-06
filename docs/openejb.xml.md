title=openejb.xml
type=page
status=published
~~~~~~

<a name="openejb.xml-Overview"></a>
# Overview

The openejb.xml is the main configuration file for the container system and
its services such as transaction, security, and data sources.
    
The format is a mix of xml and properties inspired by the format of the
httpd configuration file.  Basically:


    <tag id="">
      ...properties...
    </tag>

    
Such as:
    

    <Resource id="MyDataSource" type="DataSource">
      username foo
      password bar
    </Resource>


*Note the space*.  White space is a valid name/value pair separator in any
java properties file (along with semi-colon).  So the above is equivalent
to:

    <Resource id="MyDataSource" type="DataSource">
      username = foo
      password = bar
    </Resource>

You are free to use white space, ":", or "=" for your name/value pair
separator with no effect on OpenEJB.
    
<a name="openejb.xml-PropertyDefaultsandOverriding"></a>
## Property Defaults and Overriding
    
The openejb.xml file itself functions as an override, default values are
specified via other means (service-jar.xml files in the classpath),
therefore you only need to specify property values here for 2 reasons:<br/>
1. you wish to for documentation purposes<br/>
2. you need to change the default value

The default openejb.xml file has most of the useful properties for each
component explicitly listed with default values for documentation purposes.
 It is safe to delete them and be assured that no behavior will change if a
smaller config file is desired.

Overriding can also be done via the command line or plain Java system
properties.  See [System Properties](system-properties.html)
 for details.

<a name="openejb.xml-Whatpropertiesareavailable?"></a>
## What properties are available?
    
To know what properties can be overriden the './bin/openejb properties'
command is very useful: see [Properties Tool](properties-tool.html)
    
Its function is to connect to a running server and print a canonical list
of all properties OpenEJB can see via the various means of configuration. 
When sending requests for help to the users list or jira, it is highly
encouraged to send the output of this tool with your message.

<a name="openejb.xml-Notconfigurableviaopenejb.xml"></a>
## Not configurable via openejb.xml
    
The only thing not yet configurable via this file are ServerServices due to
OpenEJB's embeddable nature and resulting long standing tradition of
keeping the container system separate from the server layer.  This may
change someday, but untill then ServerServices are configurable via
conf/<service-id>.properties files such as conf/ejbd.properties to
configure the main protocol that services EJB client requests.

The format of those properties files is greatly adapted from the xinet.d style
of configuration and even shares similar functionality and properties such
as host-based authorization (HBA) via the 'only_from' property.

<a name="openejb.xml-Restoringopenejb.xmltothedefaults"></a>
## Restoring openejb.xml to the defaults

To restore this file to its original default state, you can simply delete
it or rename it and OpenEJB will see it's missing and unpack another
openejb.xml into the conf/ directory when it starts.

This is not only handy for recovering from a non-functional config, but
also for upgrading as OpenEJB will not overwrite your existing
configuration file should you choose to unpack an new distro over the top
of an old one -- this style of upgrade is safe provided you move your old
lib/ directory first.
