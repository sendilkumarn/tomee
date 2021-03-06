index-group=Unrevised
type=page
status=published
title=SingletonContainer Configuration
~~~~~~


A SingletonContainer can be declared via xml in the `<tomee-home>/conf/tomee.xml` file or in a `WEB-INF/resources.xml` file using a declaration like the following.  All properties in the element body are optional.

    <Container id="mySingletonContainer" type="SINGLETON">
        accessTimeout = 30 seconds
    </Container>

Alternatively, a SingletonContainer can be declared via properties in the `<tomee-home>/conf/system.properties` file or via Java VirtualMachine `-D` properties.  The properties can also be used when embedding TomEE via the `javax.ejb.embeddable.EJBContainer` API or `InitialContext`

    mySingletonContainer = new://Container?type=SINGLETON
    mySingletonContainer.accessTimeout = 30 seconds

Properties and xml can be mixed.  Properties will override the xml allowing for easy configuration change without the need for ${} style variable substitution.  Properties are not case sensitive.  If a property is specified that is not supported by the declared SingletonContainer a warning will be logged.  If a SingletonContainer is needed by the application and one is not declared, TomEE will create one dynamically using default settings.  Multiple SingletonContainer declarations are allowed.
# Supported Properties
<table class="mdtable">
<tr>
<th>Property</th>
<th>Type</th>
<th>Default</th>
<th>Description</th>
</tr>
<tr>
  <td><a href="#accessTimeout">accessTimeout</a></td>
  <td><a href="configuring-durations.html">time</a></td>
  <td>30&nbsp;seconds</td>
  <td>
Specifies the maximum time an invocation could wait for the
`@Singleton` bean instance to become available before giving up.
</td>
</tr>
</table>



<a name="accessTimeout"></a>
## accessTimeout

Specifies the maximum time an invocation could wait for the
`@Singleton` bean instance to become available before giving up.

After the timeout is reached a `javax.ejb.ConcurrentAccessTimeoutException`
will be thrown.

Usable time units: nanoseconds, microsecons, milliseconds,
seconds, minutes, hours, days.  Or any combination such as
`1 hour and 27 minutes and 10 seconds`

Any usage of the `javax.ejb.AccessTimeout` annotation will
override this setting for the bean or method where the
annotation is used.
