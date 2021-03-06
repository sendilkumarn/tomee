index-group=General Informations
type=page
status=published
title=
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

#TomEE Directory Layout:

TomEE directory layout is the same as that of Tomcat, with a few changes as described below.

Considering this root to be the $tomee-install-dir>

<pre>
/bin
  Added tomee.sh (Access all TomEE tools: cipher, deploy, properties, undeploy)
  Added TomEE.*.exe (Windows service binaries)
  Added service*.bat (Windows service installer - uses binaries above)
  Modified catalina.(sh|bat) (Optional - add the OpenJPA javaagent to enhance JPA entities. Only necessary if you use both JPA and the OpenJPA implementation and you did not enhance bytecode at build time)

/conf
  Added system.properties (Easy way to configure whatever you want on TomEE. Check it out and look into, you will discover so many interesting properties)
  Added tomee.xml (The place where you can declare/configure resources, containers, Transaction manager, etc)
  Modified server.xml (As in tomcat with one extra listener - can configure ports, hosts, engines, threadpools etc)    
  Modified tomcat-users.xml (optional - only changed to define tomee user to secure the webapp/tomee GUI)

/endorsed
  Added annotation-api.jar (Override Tomcat default jar, because not compliant with the current JEE 6 specification)
  Added jaxb-(api|impl).jar (Override JDK 1.6 default implementation cause too old for the JEE 6 specification)
  
/lib
  That's where all the magic is. This directory will receive a set of new jars. First, it gets all openejb-* and tomee-* jars. It also contains dependencies (Specification implementations: openjpa-*, openwebbeans-*, etc).
  Removed annotation-api.jar (Non compliant with JEE 6 specification. See endorsed/)
  Removed el-api.jar (Already contained in javaee-api.jar provided by TomEE in that same directory)
 
/webapps    
  Works the same way as it does for Tomcat. Drop your directories/wars in here!
  Removed examples (Just because most of people does not care)
  
/apps (does not exist by default)
  Can receive WARs of course, but also JAR and EAR files. Optionally add your resources.xml file here.
     
/webapps/tomee (added but optional)
  The TomEE graphical user interface. That's the administration interface.
  ** This webapp is mandatory if you need EJBs remote invocation
</pre>
