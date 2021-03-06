index-group=Unrevised
type=page
status=published
title=TomEE and Java 7
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

If you compile your applications on JDK7 you have to run Apache TomEE 1.0 on jdk7

Configuring TomEE to use JDK7
-------
If you have multiple JDK installed on your system you should set JAVA_HOME in your stratup scripts.
For example if your `JAVA_HOME` is `/usr/local/java/current` edit `catalina.sh`
and add a line

`JAVA_HOME=/usr/local/java/current/bin`

Alternatively, set `JAVA_HOME` as an environment variable prior to calling `<tomee-home>/bin/startup.sh`

Endorsed libraries directory
-------
TomEE 1.0 package comes with and "endorsed" direcotry which contains updates for core JDK6 libraries.
If you are running JDK7 you should remove al files in this directory.

TomEE 1.1  will detect JDK7 and will not load those files
