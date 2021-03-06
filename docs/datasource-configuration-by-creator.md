Title: DataSource Creator

TomEE uses  `creator` to create the connection pool factory. In other terms it means you can
use any pool you want for DataSource in TomEE.

Default provided pools are DBCP (default in embedded mode) and Tomcat JDBC (default in TomEE to be aligned on Tomcat).

Depending which one you use the accept configuration are not 100% the same even if we try to 
align the most common entries to the historical configuration (ie DBCP).

Here are a more detailled list of accepted properties by creator.


## DBCP (TomEE 1.7.x)

Note: details are at http://tomee.apache.org/containers-and-resources.html
(note: http://commons.apache.org/proper/commons-dbcp/configuration.html uses the latest version of DBCP but TomEE 1.7.x is not using this version).

- AccessToUnderlyingConnectionAllowed
- ConnectionInitSqls
- ConnectionProperties
- DefaultAutoCommit
- DefaultCatalog
- DefaultReadOnly
- DefaultTransactionIsolation
- Delegate
- InitialSize
- JdbcDriver
- JdbcUrl
- LogAbandoned
- LogWriter
- LoginTimeout
- MaxActive
- MaxIdle
- MaxOpenPreparedStatements
- MaxWait
- MinEvictableIdleTimeMillis
- MinIdle
- Name
- NumTestsPerEvictionRun
- Password
- PasswordCipher
- PoolPreparedStatements
- RemoveAbandoned
- RemoveAbandonedTimeout
- TestOnBorrow
- TestOnReturn
- TestWhileIdle
- TimeBetweenEvictionRunsMillis
- UserName
- ValidationQuery
- ValidationQueryTimeout

## Tomcat JDBC

Note: details are at https://tomcat.apache.org/tomcat-7.0-doc/jdbc-pool.html

- AbandonWhenPercentageFull
- AccessToUnderlyingConnectionAllowed
- AlternateUsernameAllowed
- CommitOnReturn
- ConnectionProperties
- DataSource
- DataSourceJNDI
- DbProperties
- DefaultAutoCommit
- DefaultCatalog
- DefaultReadOnly
- DefaultTransactionIsolation
- DriverClassName
- FairQueue
- IgnoreExceptionOnPreLoad
- InitSQL
- InitialSize
- JdbcInterceptors
- JmxEnabled
- LogAbandoned
- LogValidationErrors
- LogWriter
- LoginTimeout
- MaxActive
- MaxAge
- MaxIdle
- MaxWait
- MinEvictableIdleTimeMillis
- MinIdle
- Name
- NumTestsPerEvictionRun
- Password
- PasswordCipher
- PoolProperties
- PropagateInterruptState
- RemoveAbandoned
- RemoveAbandonedTimeout
- RollbackOnReturn
- SuspectTimeout
- TestOnBorrow
- TestOnConnect
- TestOnReturn
- TestWhileIdle
- TimeBetweenEvictionRunsMillis
- Url
- UseDisposableConnectionFacade
- UseEquals
- UseLock
- Username
- ValidationInterval
- ValidationQuery
- ValidationQueryTimeout
- Validator
- ValidatorClassName

## DBCP2 (TomEE 7.x)

Note: details are at http://commons.apache.org/proper/commons-dbcp/configuration.html

- AccessToUnderlyingConnectionAllowed
- ConnectionInitSqls
- ConnectionProperties
- DefaultAutoCommit
- DefaultCatalog
- DefaultReadOnly
- DefaultTransactionIsolation
- Delegate
- InitialSize
- JdbcDriver
- JdbcUrl
- LogAbandoned
- LogWriter
- LoginTimeout
- MaxTotal
- MaxIdle
- MaxOpenPreparedStatements
- MaxWait
- MinEvictableIdleTimeMillis
- MinIdle
- Name
- NumTestsPerEvictionRun
- Password
- PasswordCipher
- PoolPreparedStatements
- RemoveAbandonedOnBorrow
- RemoveAbandonedOnMaintenance
- RemoveAbandonedTimeout
- TestOnBorrow
- TestOnReturn
- TestWhileIdle
- TimeBetweenEvictionRunsMillis
- UserName
- ValidationQuery
- ValidationQueryTimeout