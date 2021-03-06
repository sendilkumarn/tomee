index-group=Unrevised
type=page
status=published
title=SecurityService Configuration
~~~~~~


A SecurityService can be declared via xml in the `<tomee-home>/conf/tomee.xml` file or in a `WEB-INF/resources.xml` file using a declaration like the following.  All properties in the element body are optional.

    <SecurityService id="mySecurityService" type="SecurityService">
        defaultUser = guest         
    </SecurityService>

Alternatively, a SecurityService can be declared via properties in the `<tomee-home>/conf/system.properties` file or via Java VirtualMachine `-D` properties.  The properties can also be used when embedding TomEE via the `javax.ejb.embeddable.EJBContainer` API or `InitialContext`

    mySecurityService = new://SecurityService?type=SecurityService
    mySecurityService.defaultUser = guest         

Properties and xml can be mixed.  Properties will override the xml allowing for easy configuration change without the need for ${} style variable substitution.  Properties are not case sensitive.  If a property is specified that is not supported by the declared SecurityService a warning will be logged.  If a SecurityService is needed by the application and one is not declared, TomEE will create one dynamically using default settings.  Multiple SecurityService declarations are allowed.
# Supported Properties
<table class="mdtable">
<tr>
<th>Property</th>
<th>Type</th>
<th>Default</th>
<th>Description</th>
</tr>
<tr>
  <td>defaultUser</td>
  <td>String</td>
  <td>guest&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</td>
  <td>

</td>
</tr>
</table>
