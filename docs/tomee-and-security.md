index-group=Configuration
type=page
status=published
title=Apache TomEE and security
~~~~~~
Notice:    Licensed to the Apache Software Foundation (ASF) under one
           or more contributor license agreements.  See the NOTICE file
           distributed with this work for additional information
           regarding copyright ownership.  The ASF licenses this file
           to you under the Apache License, Version 2.0 (the
           "License"); you may not use this file except in compliance
           with the License.  You may obtain a copy of the License at
           .
             http://www.apache.org/licenses/LICENSE-2.0
           .
           Unless required by applicable law or agreed to in writing,
           software distributed under the License is distributed on an
           "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
           KIND, either express or implied.  See the License for the
           specific language governing permissions and limitations
           under the License.

Rather than providing its own security implementation, TomEE makes full use of the security features that are part of Tomcat. Any Catalina realm is supported or you can provide your own security module using the login.config file. 

For example, to add some simple security to the [moviefun application](http://tomee.apache.org/examples-trunk/webapps/moviefun/README.html) , all we would need to do is: 

1.    Add some users to the tomcat-users.xml file     
2.    Add the necessary @DefineRoles and @RolesAllowed annotations on MoviesImpl     
3.    Add some security config to do HTTP Basic authentication to web.xml Webservice security is also looked after – username/password based security (HTTP basic, or WS-Security) uses the same Tomcat security. Certificate based security is also available.

To put it short,

*    TomEE uses Tomcat's Security Realm

*     Extra TomEE layer adds support for JAAS JACC WS Security

*     Supports any org.apache.catalina.Realm implementation

*     E.g. add users to $CATALINA_BASE/conf/tomcat-users.xml

*     Alternatively use login.config to provide your own security module


####See Also:
[TomEE-and-JAAS](tomee-jaas.html) 
