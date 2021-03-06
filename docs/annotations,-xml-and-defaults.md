index-group=Unrevised
type=page
status=published
title=Annotations, XML and Defaults
~~~~~~



<div id="PageContent">
              <p>The following is a list of all annotations and their attributes, the xml tags that correspond to them (for overriding), and what the default values are when left unspecified.</p>

<div >
<table class="mdtable"> <tbody>
<tr>
<th > Annotation </th>
<th > xml element(s) </th>
<th > default value </th>
</tr>
<tr>
<td "> @Stateless </td>
<td "><ul>
	<li>&lt;session&gt;</li>
	<li>&lt;ejb-class&gt;</li>
	<li>&lt;session-type&gt;Stateless&lt;/session-type&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "> &lt;ejb-name&gt; </td>
<td "> The simple name of the bean class. For <em>org.acme.superfun.WidgetBean</em> the ejb-name will be <b>WidgetBean</b> </td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>description</li>
</ul>
</td>
<td "> &lt;description&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>mappedName</li>
</ul>
</td>
<td "> &lt;mapped-name&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @Stateful </td>
<td "><ul>
	<li>&lt;session&gt;</li>
	<li>&lt;ejb-class&gt;</li>
	<li>&lt;session-type&gt;Stateful&lt;/session-type&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "> &lt;ejb-name&gt; </td>
<td "> The simple name of the bean class. For <em>org.acme.superfun.WidgetBean</em> the ejb-name will be <b>WidgetBean</b> </td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>description</li>
</ul>
</td>
<td "> &lt;description&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>mappedName</li>
</ul>
</td>
<td "> &lt;mapped-name&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @MessageDriven </td>
<td "><ul>
	<li>&lt;message-driven&gt;</li>
	<li>&lt;ejb-class&gt;</li>
	<li>&lt;session-type&gt;Stateful&lt;/session-type&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "> &lt;ejb-name&gt; </td>
<td "> The simple name of the bean class. For <em>org.acme.superfun.WidgetBean</em> the ejb-name will be <b>WidgetBean</b> </td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>description</li>
</ul>
</td>
<td "> &lt;description&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>mappedName</li>
</ul>
</td>
<td "> &lt;mapped-name&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>messageListenerInterface</li>
</ul>
</td>
<td "> &lt;messaging-type&gt; </td>
<td "> The interface the bean class implements.  When relying upon the default is illegal for the bean to implement more than one interface </td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>activationConfig[]</li>
</ul>
</td>
<td "> &lt;activation-config&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @ActivationConfigProperty </td>
<td "> &lt;activation-config-property&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>propertyName</li>
</ul>
</td>
<td "> &lt;activation-config-property-name&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>propertyValue</li>
</ul>
</td>
<td "> &lt;activation-config-property-value&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @RemoteHome </td>
<td "><ul>
	<li>&lt;home&gt;</li>
	<li>&lt;remote&gt;</li>
</ul>
</td>
<td "> The home is inspected to determine the value of &lt;remote&gt;</td>
</tr>
<tr>
<td "> @LocalHome </td>
<td "><ul>
	<li>&lt;local-home&gt;</li>
	<li>&lt;local&gt;</li>
</ul>
</td>
<td "> The local-home is inspected to determine the value of &lt;local&gt; </td>
</tr>
<tr>
<td "> @TransactionManagement </td>
<td "> &lt;transaction-type&gt; </td>
<td "> TransactionManagementType.CONTAINER (xml value "Container") </td>
</tr>
<tr>
<td "> @TransactionAttribute </td>
<td "><ul>
	<li>&lt;container-transaction&gt;</li>
	<li>&lt;transaction-attribute&gt;</li>
</ul>
</td>
<td "> All method default to TransactionAttributeType.REQUIRED (xml value "Required") </td>
</tr>
<tr>
<td "> @RolesAllowed </td>
<td "><ul>
	<li>&lt;method-permission&gt;</li>
	<li>&lt;role-name&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @PermitAll </td>
<td "><ul>
	<li>&lt;method-permission&gt;</li>
	<li>&lt;unchecked&gt;</li>
</ul>
</td>
<td "> All methods default to unchecked </td>
</tr>
<tr>
<td "> @DenyAll </td>
<td "> &lt;exclude-list&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @RunAs </td>
<td "><ul>
	<li>&lt;security-identity&gt;</li>
	<li>&lt;run-as&gt;</li>
	<li>&lt;role-name&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @DeclareRoles </td>
<td "> &lt;security-role-ref&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @Interceptors </td>
<td "><ul>
	<li>&lt;interceptor&gt;</li>
	<li>&lt;interceptor-binding&gt;</li>
	<li>&lt;interceptor-class&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @ExcludeDefaultInterceptors </td>
<td "><ul>
	<li>&lt;interceptor-binding&gt;</li>
	<li>&lt;exclude-default-interceptors&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @ExcludeClassInterceptors </td>
<td "><ul>
	<li>&lt;interceptor-binding&gt;</li>
	<li>&lt;exclude-class-interceptors&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @AroundInvoke </td>
<td "> &lt;around-invoke&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @PostConstruct </td>
<td "> &lt;post-construct&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @PreDestroy </td>
<td "> &lt;pre-destroy&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @PrePassivate </td>
<td "> &lt;pre-passivate&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @PostActivate </td>
<td "> &lt;post-activate&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @Init </td>
<td "> &lt;init-method&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @Remove </td>
<td "> &lt;remove-method&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>retainIfException</li>
</ul>
</td>
<td "> &lt;retain-if-exception&gt; </td>
<td "> false </td>
</tr>
<tr>
<td "> @Timeout </td>
<td "> &lt;timeout-method&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @ApplicationException </td>
<td "><ul>
	<li>&lt;application-exception&gt;</li>
	<li>&lt;exception-class&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>rollback</li>
</ul>
</td>
<td "> &lt;rollback&gt; </td>
<td "> false </td>
</tr>
<tr>
<td "> @EJB </td>
<td "><ul>
	<li>&lt;ejb-ref&gt;</li>
	<li>&lt;ejb-local-ref&gt;</li>
	<li>&lt;injection-target&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "><ul>
	<li>&lt;ejb-ref-name&gt;</li>
</ul>
</td>
<td "><ul>
	<li>on class: illegal to leave undefined</li>
	<li>on field: {className}/{fieldName} as in <b>org.superbiz.Widget/myEjb</b></li>
	<li>on setter: {className}/{propertyName} as in setMyEjb() defaults to <b>org.superbiz.Widget/myEjb</b></li>
</ul>
</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>beanInterface</li>
</ul>
</td>
<td "><ul>
	<li>&lt;home&gt;</li>
	<li>&lt;local-home&gt;</li>
	<li>&lt;remote&gt;</li>
	<li>&lt;local&gt;</li>
</ul>
</td>
<td "><ul>
	<li>on class: illegal to leave undefined</li>
	<li>on field: the data type of the field</li>
	<li>on setter: the data type of the first method param</li>
</ul>
</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>beanName</li>
</ul>
</td>
<td "> &lt;ejb-link&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>description</li>
</ul>
</td>
<td "> &lt;description&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>mappedName</li>
</ul>
</td>
<td "> &lt;mapped-name&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @Resource </td>
<td "><ul>
	<li>&lt;env-entry&gt;</li>
	<li>&lt;resource-ref&gt;</li>
	<li>&lt;resource-env-ref&gt;</li>
	<li>&lt;injection-target&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "><ul>
	<li>&lt;env-entry-name&gt;</li>
	<li>&lt;res-ref-name&gt;</li>
	<li>&lt;resource-env-ref-name&gt;</li>
</ul>
</td>
<td "><ul>
	<li>on class: illegal to leave undefined</li>
	<li>on field: {className}/{fieldName} as in <b>org.superbiz.Widget/myDataSource</b></li>
	<li>on setter: {className}/{propertyName} as in setMyDataSource() defaults to <b>org.superbiz.Widget/myDataSource</b></li>
</ul>
</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>type</li>
</ul>
</td>
<td "><ul>
	<li>&lt;env-entry-type&gt;</li>
	<li>&lt;res-type&gt;</li>
	<li>&lt;resource-env-ref-type&gt;</li>
</ul>
</td>
<td "><ul>
	<li>on class: illegal to leave undefined</li>
	<li>on field: the data type of the field</li>
	<li>on setter: the data type of the first method param</li>
</ul>
</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>description</li>
</ul>
</td>
<td "> &lt;description&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>mappedName</li>
</ul>
</td>
<td "> &lt;mapped-name&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>shareable</li>
</ul>
</td>
<td "> &lt;res-sharing-scope&gt; </td>
<td "> true (xml value "Shareable") </td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>authenticationType</li>
</ul>
</td>
<td "> &lt;res-auth&gt; </td>
<td "> AuthenticationType.CONTAINER (xml value "Container") </td>
</tr>
<tr>
<td "> @PersistenceUnit </td>
<td "><ul>
	<li>&lt;persistence-unit-ref&gt;</li>
	<li>&lt;injection-target&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "> &lt;persistence-unit-ref-name&gt; </td>
<td ">on class: illegal to leave undefined
<ul>
	<li>on field: {className}/{fieldName} as in <b>org.superbiz.Widget/myUnit</b></li>
	<li>on setter: {className}/{propertyName} as in setMyUnit() defaults to <b>org.superbiz.Widget/myUnit</b></li>
</ul>
</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>unitName</li>
</ul>
</td>
<td "> &lt;persistence-unit-name&gt; </td>
<td "> vendor specific </td>
</tr>
<tr>
<td "> @PersistenceContext </td>
<td "><ul>
	<li>&lt;persistence-context-ref&gt;</li>
	<li>&lt;injection-target&gt;</li>
</ul>
</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "> &lt;persistence-context-ref-name&gt; </td>
<td ">on class: illegal to leave undefined
<ul>
	<li>on field: {className}/{fieldName} as in <b>org.superbiz.Widget/myContext</b></li>
	<li>on setter: {className}/{propertyName} as in setMyContext() defaults to <b>org.superbiz.Widget/myContext</b></li>
</ul>
</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>unitName</li>
</ul>
</td>
<td "> &lt;persistence-unit-name&gt; </td>
<td "> vendor specific </td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>type</li>
</ul>
</td>
<td "> &lt;persistence-context-type&gt; </td>
<td "> PersistenceContextType.TRANSACTION (xml value "Transaction") </td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>properties[]</li>
</ul>
</td>
<td ">&nbsp;</td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "> @PersistenceProperty </td>
<td "> &lt;persistence-property&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>name</li>
</ul>
</td>
<td "> &lt;name&gt; </td>
<td ">&nbsp;</td>
</tr>
<tr>
<td "><ul type="square" class="alternate">
	<li>value</li>
</ul>
</td>
<td "> &lt;value&gt; </td>
<td ">&nbsp;</td>
</tr>
</tbody></table>
</div>

            </div>
