index-group=Unrevised
type=page
status=published
title=TransactionManager Configuration
~~~~~~


A TransactionManager can be declared via xml in the `<tomee-home>/conf/tomee.xml` file or in a `WEB-INF/resources.xml` file using a declaration like the following.  All properties in the element body are optional.

    <TransactionManager id="myTransactionManager" type="TransactionManager">
        adler32Checksum = true
        bufferSizeKb = 32
        checksumEnabled = true
        defaultTransactionTimeout = 10 minutes
        flushSleepTime = 50 Milliseconds
        logFileDir = txlog
        logFileExt = log
        logFileName = howl
        maxBlocksPerFile = -1
        maxBuffers = 0
        maxLogFiles = 2
        minBuffers = 4
        threadsWaitingForceThreshold = -1
        txRecovery = false
    </TransactionManager>

Alternatively, a TransactionManager can be declared via properties in the `<tomee-home>/conf/system.properties` file or via Java VirtualMachine `-D` properties.  The properties can also be used when embedding TomEE via the `javax.ejb.embeddable.EJBContainer` API or `InitialContext`

    myTransactionManager = new://TransactionManager?type=TransactionManager
    myTransactionManager.adler32Checksum = true
    myTransactionManager.bufferSizeKb = 32
    myTransactionManager.checksumEnabled = true
    myTransactionManager.defaultTransactionTimeout = 10 minutes
    myTransactionManager.flushSleepTime = 50 Milliseconds
    myTransactionManager.logFileDir = txlog
    myTransactionManager.logFileExt = log
    myTransactionManager.logFileName = howl
    myTransactionManager.maxBlocksPerFile = -1
    myTransactionManager.maxBuffers = 0
    myTransactionManager.maxLogFiles = 2
    myTransactionManager.minBuffers = 4
    myTransactionManager.threadsWaitingForceThreshold = -1
    myTransactionManager.txRecovery = false

Properties and xml can be mixed.  Properties will override the xml allowing for easy configuration change without the need for ${} style variable substitution.  Properties are not case sensitive.  If a property is specified that is not supported by the declared TransactionManager a warning will be logged.  If a TransactionManager is needed by the application and one is not declared, TomEE will create one dynamically using default settings.  Multiple TransactionManager declarations are allowed.
# Supported Properties
<table class="mdtable">
<tr>
<th>Property</th>
<th>Type</th>
<th>Default</th>
<th>Description</th>
</tr>
<tr>
  <td>adler32Checksum</td>
  <td>boolean</td>
  <td>true</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>bufferSizeKb</td>
  <td>int</td>
  <td>32</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>checksumEnabled</td>
  <td>boolean</td>
  <td>true</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>defaultTransactionTimeout</td>
  <td><a href="configuring-durations.html">time</a></td>
  <td>10&nbsp;minutes</td>
  <td>

</td>
</tr>
<tr>
  <td>flushSleepTime</td>
  <td><a href="configuring-durations.html">time</a></td>
  <td>50&nbsp;Milliseconds</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>logFileDir</td>
  <td>String</td>
  <td>txlog</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>logFileExt</td>
  <td>String</td>
  <td>log</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>logFileName</td>
  <td>String</td>
  <td>howl</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>maxBlocksPerFile</td>
  <td>int</td>
  <td>-1</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>maxBuffers</td>
  <td>int</td>
  <td>0</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>maxLogFiles</td>
  <td>int</td>
  <td>2</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>minBuffers</td>
  <td>int</td>
  <td>4</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>threadsWaitingForceThreshold</td>
  <td>int</td>
  <td>-1</td>
  <td>
Requires TxRecovery
</td>
</tr>
<tr>
  <td>txRecovery</td>
  <td>boolean</td>
  <td>false</td>
  <td>
When set to true, Howl logging is enabled
</td>
</tr>
</table>
