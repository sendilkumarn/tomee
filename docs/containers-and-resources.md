index-group=Configuration
type=page
status=published
title=Containers and Resources
~~~~~~

<div id="PageContent">
              <p><a name="ContainersandResources-containers"></a></p>
<p><a name="ContainersandResources-DefaultCMPContainercontainer"></a></p>
<h2><a name="ContainersandResources-CMPENTITY"></a>CMP_ENTITY</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Container id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"CMP_ENTITY"</span>&gt;</span>
<span class="code-tag">&lt;/Container&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Container?type=CMP_ENTITY</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > CmpEngineFactory </td>
<td > Default value is <em>org.apache.openejb.core.cmp.jpa.JpaCmpEngineFactory</em>.</td>
</tr>
</tbody></table>
</div>

<p><a name="ContainersandResources-TransactionManager"></a></p>
<h2><a name="ContainersandResources-TxMgr"></a>TransactionManager</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;TransactionManager type=<span class="code-quote">"javax.transaction.TransactionManager"</span>&gt;</span>
<span class="code-tag">&lt;/TransactionManager&gt;</span>
</pre>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > defaultTransactionTimeoutSeconds </td>
<td > Default value is <em>10 minutes</em>.</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultBMPContainercontainer"></a></p>
<h2><a name="ContainersandResources-BMPENTITY"></a>BMP_ENTITY</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Container id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"BMP_ENTITY"</span>&gt;</span>
<span class="code-tag">&lt;/Container&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Container?type=BMP_ENTITY</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > PoolSize </td>
<td > Specifies the size of the bean pools for this<br class="atl-forced-newline"> bmp entity container.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>10</em>.</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultStatelessContainercontainer"></a></p>
<h2><a name="ContainersandResources-STATELESS"></a>STATELESS</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Container id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"STATELESS"</span>&gt;</span>
<span class="code-tag">&lt;/Container&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Container?type=STATELESS</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > TimeOut </td>
<td > Specifies the time to wait between invocations. This<br class="atl-forced-newline"> value is measured in milliseconds. A value of 5 would<br class="atl-forced-newline"> result in a time-out of 5 milliseconds between invocations.<br class="atl-forced-newline"> A value of zero would mean no timeout.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>0</em>.</td>
</tr>
<tr>
<td > PoolSize </td>
<td > Specifies the size of the bean pools for this<br class="atl-forced-newline"> stateless SessionBean container.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>10</em>.</td>
</tr>
<tr>
<td > StrictPooling </td>
<td > StrictPooling tells the container what to do when the pool<br class="atl-forced-newline"> reaches it's maximum size and there are incoming requests<br class="atl-forced-newline"> that need instances.<br class="atl-forced-newline"> <br class="atl-forced-newline"> With strict pooling, requests will have to wait for instances<br class="atl-forced-newline"> to become available. The pool size will never grow beyond the<br class="atl-forced-newline"> the set PoolSize value.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Without strict pooling, the container will create temporary<br class="atl-forced-newline"> instances to meet demand. The instances will last for just one<br class="atl-forced-newline"> method invocation and then are removed.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>true</em>.</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultStatefulContainercontainer"></a></p>
<h2><a name="ContainersandResources-STATEFUL"></a>STATEFUL</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Container id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"STATEFUL"</span>&gt;</span>
<span class="code-tag">&lt;/Container&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Container?type=STATEFUL</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > Passivator </td>
<td > The passivator is responsible for writing beans to disk<br class="atl-forced-newline"> at passivation time. Different passivators can be used<br class="atl-forced-newline"> by setting this property to the fully qualified class name<br class="atl-forced-newline"> of the PassivationStrategy implementation. The passivator<br class="atl-forced-newline"> is not responsible for invoking any callbacks or other<br class="atl-forced-newline"> processing, its only responsibly is to write the bean state<br class="atl-forced-newline"> to disk.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Known implementations:<br class="atl-forced-newline"> org.apache.openejb.core.stateful.RAFPassivater<br class="atl-forced-newline"> org.apache.openejb.core.stateful.SimplePassivater<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>org.apache.openejb.core.stateful.SimplePassivater</em>.</td>
</tr>
<tr>
<td > TimeOut </td>
<td > Specifies the time to wait between invocations. This<br class="atl-forced-newline"> value is measured in minutes. A value of 5 would<br class="atl-forced-newline"> result in a time-out of 5 minutes between invocations.<br class="atl-forced-newline"> A value of zero would mean no timeout.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>20</em>.</td>
</tr>
<tr>
<td > PoolSize </td>
<td > Specifies the size of the bean pools for this<br class="atl-forced-newline"> stateful SessionBean container.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>1000</em>.</td>
</tr>
<tr>
<td > BulkPassivate </td>
<td > Property name that specifies the number of instances<br class="atl-forced-newline"> to passivate at one time when doing bulk passivation.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>100</em>.</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultMDBContainercontainer"></a></p>
<h2><a name="ContainersandResources-MESSAGE"></a>MESSAGE</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Container id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"MESSAGE"</span>&gt;</span>
<span class="code-tag">&lt;/Container&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Container?type=MESSAGE</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > ResourceAdapter </td>
<td > The resource adapter delivers messages to the container<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>Default JMS Resource Adapter</em>.</td>
</tr>
<tr>
<td > MessageListenerInterface </td>
<td > Specifies the message listener interface handled by this container<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>javax.jms.MessageListener</em>.</td>
</tr>
<tr>
<td > ActivationSpecClass </td>
<td > Specifies the activation spec class<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>org.apache.activemq.ra.ActiveMQActivationSpec</em>.</td>
</tr>
<tr>
<td > InstanceLimit </td>
<td > Specifies the maximum number of bean instances that are<br class="atl-forced-newline"> allowed to exist for each MDB deployment.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>10</em>.</td>
</tr>
</tbody></table>
</div>



<p><a name="ContainersandResources-resources"></a></p>
<h1><a name="ContainersandResources-Resources"></a>Resources</h1>
<p><a name="ContainersandResources-DefaultJDBCDatabaseresource"></a></p>
<h2><a name="ContainersandResources-javax.sql.DataSource"></a>javax.sql.DataSource</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Resource id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"javax.sql.DataSource"</span>&gt;</span>
<span class="code-tag">&lt;/Resource&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Resource?type=javax.sql.DataSource</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > JtaManaged </td>
<td > Determines wether or not this data source should be JTA managed<br class="atl-forced-newline"> or user managed.&nbsp;&nbsp;If set to 'true' it will automatically be enrolled<br class="atl-forced-newline"> in any ongoing transactions.&nbsp;&nbsp;Calling begin/commit/rollback or setAutoCommit<br class="atl-forced-newline"> on the datasource or connection will not be allowed.&nbsp;&nbsp;If you need to perform<br class="atl-forced-newline"> these functions yourself, set JtaManaged to 'false'<br class="atl-forced-newline"> <br class="atl-forced-newline"> In terms of JPA persistence.xml:<br class="atl-forced-newline"> "JtaManaged=true" can be used as a 'jta-data-source'<br class="atl-forced-newline"> "JtaManaged=false" can be used as a 'non-jta-data-source'<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>true</em>.</td>
</tr>
<tr>
<td > JdbcDriver </td>
<td > Driver class name<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>org.hsqldb.jdbcDriver</em>.</td>
</tr>
<tr>
<td > JdbcUrl </td>
<td > Url for creating connections<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>jdbc:hsqldb:file:data/hsqldb/hsqldb</em>.</td>
</tr>
<tr>
<td > UserName </td>
<td > Default user name<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>sa</em>.</td>
</tr>
<tr>
<td > Password </td>
<td > Default password</td>
</tr>
<tr>
<td > ConnectionProperties </td>
<td > The connection properties that will be sent to the JDBC<br class="atl-forced-newline"> driver when establishing new connections<br class="atl-forced-newline"> <br class="atl-forced-newline"> Format of the string must be [propertyName=property;]*<br class="atl-forced-newline"> <br class="atl-forced-newline"> NOTE - The "user" and "password" properties will be passed<br class="atl-forced-newline"> explicitly, so they do not need to be included here.</td>
</tr>
<tr>
<td > DefaultAutoCommit </td>
<td > The default auto-commit state of new connections<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>true</em>.</td>
</tr>
<tr>
<td > DefaultReadOnly </td>
<td > The default read-only state of new connections<br class="atl-forced-newline"> If not set then the setReadOnly method will not be called.<br class="atl-forced-newline"> (Some drivers don't support read only mode, ex: Informix)</td>
</tr>
<tr>
<td > DefaultTransactionIsolation </td>
<td > The default TransactionIsolation state of new connections<br class="atl-forced-newline"> If not set then the setTransactionIsolation method will not<br class="atl-forced-newline"> be called. The allowed values for this property are:<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; NONE<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; READ_COMMITTED<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; READ_UNCOMMITTED<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; REPEATABLE_READ<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; SERIALIZABLE<br class="atl-forced-newline"> <br class="atl-forced-newline"> Note: Most JDBC drivers do not support all isolation levels</td>
</tr>
<tr>
<td > InitialSize </td>
<td > The initial number of connections that are created when the<br class="atl-forced-newline"> pool is started<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>0</em>.</td>
</tr>
<tr>
<td > MaxActive </td>
<td > The maximum number of active connections that can be<br class="atl-forced-newline"> allocated from this pool at the same time, or a negative<br class="atl-forced-newline"> number for no limit.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>20</em>.</td>
</tr>
<tr>
<td > MaxIdle </td>
<td > The maximum number of connections that can remain idle in<br class="atl-forced-newline"> the pool, without extra ones being released, or a negative<br class="atl-forced-newline"> number for no limit.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>20</em>.</td>
</tr>
<tr>
<td > MinIdle </td>
<td > The minimum number of connections that can remain idle in<br class="atl-forced-newline"> the pool, without extra ones being created, or zero to<br class="atl-forced-newline"> create none.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>0</em>.</td>
</tr>
<tr>
<td > MaxWait </td>
<td > The maximum number of milliseconds that the pool will wait<br class="atl-forced-newline"> (when there are no available connections) for a connection<br class="atl-forced-newline"> to be returned before throwing an exception, or -1 to wait<br class="atl-forced-newline"> indefinitely.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>-1</em>.</td>
</tr>
<tr>
<td > ValidationQuery </td>
<td > The SQL query that will be used to validate connections from<br class="atl-forced-newline"> this pool before returning them to the caller. If specified,<br class="atl-forced-newline"> this query MUST be an SQL SELECT statement that returns at<br class="atl-forced-newline"> least one row.</td>
</tr>
<tr>
<td > TestOnBorrow </td>
<td > If true connections will be validated before being borrowed<br class="atl-forced-newline"> from the pool. If the validation fails, the connection is<br class="atl-forced-newline"> destroyed, and a new conection will be retrieved from the<br class="atl-forced-newline"> pool (and validated).<br class="atl-forced-newline"> <br class="atl-forced-newline"> NOTE - for a true value to have any effect, the<br class="atl-forced-newline"> ValidationQuery parameter must be set.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>true</em>.</td>
</tr>
<tr>
<td > TestOnReturn </td>
<td > If true connections will be validated before being returned<br class="atl-forced-newline"> to the pool.&nbsp;&nbsp;If the validation fails, the connection is<br class="atl-forced-newline"> destroyed instead of being returned to the pool.<br class="atl-forced-newline"> <br class="atl-forced-newline"> NOTE - for a true value to have any effect, the<br class="atl-forced-newline"> ValidationQuery parameter must be set.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>false</em>.</td>
</tr>
<tr>
<td > TestWhileIdle </td>
<td > If true connections will be validated by the idle connection<br class="atl-forced-newline"> evictor (if any). If the validation fails, the connection is<br class="atl-forced-newline"> destroyed and removed from the pool<br class="atl-forced-newline"> <br class="atl-forced-newline"> NOTE - for a true value to have any effect, the<br class="atl-forced-newline"> timeBetweenEvictionRunsMillis property must be a positive<br class="atl-forced-newline"> number and the ValidationQuery parameter must be set.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>false</em>.</td>
</tr>
<tr>
<td > TimeBetweenEvictionRunsMillis </td>
<td > The number of milliseconds to sleep between runs of the idle<br class="atl-forced-newline"> connection evictor thread. When set to a negative number, no<br class="atl-forced-newline"> idle connection evictor thread will be run.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>-1</em>.</td>
</tr>
<tr>
<td > NumTestsPerEvictionRun </td>
<td > The number of connectionss to examine during each run of the<br class="atl-forced-newline"> idle connection evictor thread (if any).<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>3</em>.</td>
</tr>
<tr>
<td > MinEvictableIdleTimeMillis </td>
<td > The minimum amount of time a connection may sit idle in the<br class="atl-forced-newline"> pool before it is eligable for eviction by the idle<br class="atl-forced-newline"> connection evictor (if any).<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>1800000</em>.</td>
</tr>
<tr>
<td > PoolPreparedStatements </td>
<td > If true, a statement pool is created for each Connection and<br class="atl-forced-newline"> PreparedStatements created by one of the following methods are<br class="atl-forced-newline"> pooled:<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp;public PreparedStatement prepareStatement(String sql);<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp;public PreparedStatement prepareStatement(String sql,<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;int resultSetType,<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;int resultSetConcurrency)<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>false</em>.</td>
</tr>
<tr>
<td > MaxOpenPreparedStatements </td>
<td > The maximum number of open statements that can be allocated<br class="atl-forced-newline"> from the statement pool at the same time, or zero for no<br class="atl-forced-newline"> limit.<br class="atl-forced-newline"> <br class="atl-forced-newline"> NOTE - Some drivers have limits on the number of open<br class="atl-forced-newline"> statements, so make sure there are some resources left<br class="atl-forced-newline"> for the other (non-prepared) statements.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>0</em>.</td>
</tr>
<tr>
<td > AccessToUnderlyingConnectionAllowed </td>
<td > If true the raw physical connection to the database can be<br class="atl-forced-newline"> accessed using the following construct:<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; Connection conn = ds.getConnection();<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; Connection rawConn = ((DelegatingConnection) conn).getInnermostDelegate();<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; ...<br class="atl-forced-newline">&nbsp;&nbsp;&nbsp;&nbsp; conn.close()<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default is false, because misbehaving programs can do harmfull<br class="atl-forced-newline"> things to the raw connection shuch as closing the raw<br class="atl-forced-newline"> connection or continuing to use the raw connection after it<br class="atl-forced-newline"> has been assigned to another logical connection.&nbsp;&nbsp;Be carefull<br class="atl-forced-newline"> and only use when you need direct access to driver specific<br class="atl-forced-newline"> extentions.<br class="atl-forced-newline"> <br class="atl-forced-newline"> NOTE: Do NOT close the underlying connection, only the<br class="atl-forced-newline"> original logical connection wrapper.<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>false</em>.</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultJMSResourceAdapterresource"></a></p>
<h2><a name="ContainersandResources-ActiveMQResourceAdapter"></a>ActiveMQResourceAdapter</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Resource id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"ActiveMQResourceAdapter"</span>&gt;</span>
<span class="code-tag">&lt;/Resource&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Resource?type=ActiveMQResourceAdapter</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > BrokerXmlConfig </td>
<td > Broker configuration<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>broker:(tcp://localhost:61616)?useJmx=false</em>.</td>
</tr>
<tr>
<td > ServerUrl </td>
<td > Broker address<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>vm://localhost?async=true</em>.</td>
</tr>
<tr>
<td > DataSource </td>
<td > DataSource for persistence messages<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>Default Unmanaged JDBC Database</em>.</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultJMSConnectionFactoryresource"></a></p>
<h2><a name="ContainersandResources-javax.jms.ConnectionFactory"></a>javax.jms.ConnectionFactory</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Resource id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"javax.jms.ConnectionFactory"</span>&gt;</span>
<span class="code-tag">&lt;/Resource&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Resource?type=javax.jms.ConnectionFactory</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > ResourceAdapter </td>
<td > Default value is <em>Default JMS Resource Adapter</em>.</td>
</tr>
<tr>
<td > TransactionSupport </td>
<td > Specifies if the connection is enrolled in global transaction<br class="atl-forced-newline"> allowed values: xa, local or none<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>xa</em>.</td>
</tr>
<tr>
<td > PoolMaxSize </td>
<td > Maximum number of physical connection to the ActiveMQ broker<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>10</em>.</td>
</tr>
<tr>
<td > PoolMinSize </td>
<td > Minimum number of physical connection to the ActiveMQ broker<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>0</em>.</td>
</tr>
<tr>
<td > ConnectionMaxWaitMilliseconds </td>
<td > Maximum amount of time to wait for a connection<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>5000</em>.</td>
</tr>
<tr>
<td > ConnectionMaxIdleMinutes </td>
<td > Maximum amount of time a connection can be idle before being reclaimed<br class="atl-forced-newline"> <br class="atl-forced-newline"> Default value is <em>15</em>.</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultQueueresource"></a></p>
<h2><a name="ContainersandResources-javax.jms.Queue"></a>javax.jms.Queue</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Resource id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"javax.jms.Queue"</span>&gt;</span>
<span class="code-tag">&lt;/Resource&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Resource?type=javax.jms.Queue</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > destination </td>
<td > Specifies the name of the queue</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultTopicresource"></a></p>
<h2><a name="ContainersandResources-javax.jms.Topic"></a>javax.jms.Topic</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Resource id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"javax.jms.Topic"</span>&gt;</span>
<span class="code-tag">&lt;/Resource&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Resource?type=javax.jms.Topic</p>
</div></div>
<p>Supports the following properties</p>
<div class="table-wrap">
<table class="mdtable"> <tbody>
<tr>
<th > Property Name </th>
<th > Description </th>
</tr>
<tr>
<td > destination </td>
<td > Specifies the name of the topic</td>
</tr>
</tbody></table>
</div>


<p><a name="ContainersandResources-DefaultORBresource"></a></p>
<h2><a name="ContainersandResources-org.omg.CORBA.ORB"></a>org.omg.CORBA.ORB</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Resource id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"org.omg.CORBA.ORB"</span>&gt;</span>
<span class="code-tag">&lt;/Resource&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Resource?type=org.omg.CORBA.ORB</p>
</div></div>
<p>No properties.</p>

<p><a name="ContainersandResources-DefaultMailSessionresource"></a></p>
<h2><a name="ContainersandResources-javax.mail.Session"></a>javax.mail.Session</h2>
<p>Declarable in tomee.xml via</p>
<div style="border-width: 1px;" class="code panel"><div class="codeContent panelContent">
<pre class="code-xml"><span class="code-tag">&lt;Resource id=<span class="code-quote">"Foo"</span> type=<span class="code-quote">"javax.mail.Session"</span>&gt;</span>
<span class="code-tag">&lt;/Resource&gt;</span>
</pre>
</div></div>
<p>Declarable in properties via</p>
<div style="border-width: 1px;" class="panel"><div class="panelContent">
<p>Foo = new://Resource?type=javax.mail.Session</p>
</div></div>
<p>No properties.</p>
            
