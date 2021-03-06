index-group=Unrevised
type=page
status=published
title=TomEE and Intellij
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

Intellij is the preferred editor of most of the developers on Apache TomEE.  It's fast and light and goes out of its way
to guess what you're thinking and act accordingly in efforts to save you time and increase your enjoyment.  In this regard
TomEE and Intellij have a lot in common.

While TomEE works with most IDEs via the Tomcat adapter and this covers WAR files, JetBrains has stepped up to the plate
with a TomEE specific adapter to allow deployment of the full range of archives that TomEE supports.  The evolving
TomEE/Intellij integration sets the pace for all other IDE integrations.
[Feature requests very welcome!](http://youtrack.jetbrains.com/issues/IDEA)  TomEE is to Intellij
what GlassFish is to NetBeans and your feedback is a critcal part of that.


# Getting Started

We will use one of the existing [examples][1] for this demo. Let's import it.
  ![alt text][2]
  ![alt text][3]
  ![alt text][4]

Give a minute while Intellij imports the dependencies.
  ![alt text][5]

It's time to run the application. Open "Edit Configurations".
  ![alt text][6]

Click the "+" icon and select "TomEE Server" and "Local".
  ![alt text][7]

If your server is still not configured, click the "Configure" button and point it to your local TomEE installation.
  ![alt text][8]

If you see a warning message like "No artifacts marked for deployment", click the "Fix" button and select one of the options.
  ![alt text][9]

You can change the "Application Context".
  ![alt text][10]

Now you can run it. Click the "play" button.
  ![alt text][11]
  ![alt text][12]

Your application is up and running.
  ![alt text][13]
  ![alt text][14]


  [1]: https://svn.apache.org/repos/asf/tomee/tomee/trunk/examples/
  [2]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_01.png
  [3]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_02.png
  [4]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_03.png
  [5]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_04.png
  [6]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_05.png
  [7]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_06.png
  [8]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_07.png
  [9]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_08.png
  [10]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_09.png
  [11]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_10.png
  [12]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_11.png
  [13]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_12.png
  [14]: http://people.apache.org/~tveronezi/tomee/tomee_site/intellij_integration/windows8_13.png
