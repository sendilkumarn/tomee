index-group=Unrevised
type=page
status=published
~~~~~~
<div class="section">
<h2>tomee:run<a name="tomee:run"></a></h2>
      
<p><b>Full name</b>:</p>
      
<p>org.apache.openejb.maven:tomee-maven-plugin[:Current Version]:run</p>
      
<p><b>Description</b>:</p>
      
<div>Start and wait for TomEE.</div>
      
<p><b>Attributes</b>:</p>
      
<ul>
        
<li>Requires a Maven project to be executed.</li>
        
<li>Requires dependency resolution of artifacts in scope: <tt>runtime+system</tt>.</li>
        
<li>Requires dependency collection of artifacts in scope: <tt>runtime</tt>.</li>
      </ul>
      
<div class="section">
<h3>Optional Parameters<a name="Optional_Parameters"></a></h3>
        
<table class="mdtable">
          
<tr class="a">
            
<th>Name</th>
            
<th>Type</th>
            
<th>Since</th>
            
<th>Description</th>
          </tr>
          
<tr class="b">
            
<td><b><a href="#apacheRepos">apacheRepos</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>snapshots</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.apache-repos</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#appDir">appDir</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>relative to tomee.base.<br /><b>Default value is</b>: <tt>apps</tt>.<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#apps">apps</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /></td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#args">args</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>User property is</b>: <tt>tomee-plugin.args</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#bin">bin</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.basedir}/src/main/tomee/bin</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.bin</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#catalinaBase">catalinaBase</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.build.directory}/apache-tomee</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.catalina-base</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#checkStarted">checkStarted</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.check-started</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#classpaths">classpaths</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#config">config</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.basedir}/src/main/tomee/conf</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.conf</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#context">context</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>rename the current artifact<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#debug">debug</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.debug</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#debugPort">debugPort</a></b></td>
            
<td><tt>int</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>5005</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.debugPort</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#deployOpenEjbApplication">deployOpenEjbApplication</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.deploy-openejb-internal-application</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#docBases">docBases</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>for TomEE and wars only, which docBase to use for this war.<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#ejbRemote">ejbRemote</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>true</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.ejb-remote</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#externalRepositories">externalRepositories</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>for TomEE and wars only, add some external repositories to
classloader.<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#forceReloadable">forceReloadable</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>force webapp to be reloadable<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.force-reloadable</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#javaagents">javaagents</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#keepServerXmlAsthis">keepServerXmlAsthis</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(Removed since 7.0.0)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.keep-server-xml</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#lib">lib</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.basedir}/src/main/tomee/lib</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.lib</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#libDir">libDir</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>relative to tomee.base.<br /><b>Default value is</b>: <tt>lib</tt>.<br /></td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#libs">libs</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>supported formats: --&gt; groupId:artifactId:version... --&gt;
unzip:groupId:artifactId:version... --&gt; remove:prefix (often
prefix = artifactId)<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#mainDir">mainDir</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.basedir}/src/main</tt>.<br /></td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#password">password</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>User property is</b>: <tt>tomee-plugin.pwd</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#quickSession">quickSession</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>use a real random instead of secure random. saves few ms at
startup.<br /><b>Default value is</b>: <tt>true</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.quick-session</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#realm">realm</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>User property is</b>: <tt>tomee-plugin.realm</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#reloadOnUpdate">reloadOnUpdate</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.reload-on-update</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#removeDefaultWebapps">removeDefaultWebapps</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>true</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.remove-default-webapps</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#removeTomeeWebapp">removeTomeeWebapp</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>true</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.remove-tomee-webapps</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#simpleLog">simpleLog</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.simple-log</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#skipCurrentProject">skipCurrentProject</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.skipCurrentProject</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#skipWarResources">skipWarResources</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>when you set docBases to src/main/webapp setting it to true will
allow hot refresh.<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.skipWarResources</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#synchronization">synchronization</a></b></td>
            
<td><tt>Synchronization</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /></td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#synchronizations">synchronizations</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#systemVariables">systemVariables</a></b></td>
            
<td><tt>Map</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /></td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#target">target</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.build.directory}</tt>.<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#tomeeAjpPort">tomeeAjpPort</a></b></td>
            
<td><tt>int</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>8009</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.ajp</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#tomeeAlreadyInstalled">tomeeAlreadyInstalled</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.exiting</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#tomeeArtifactId">tomeeArtifactId</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>apache-tomee</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.artifactId</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#tomeeClassifier">tomeeClassifier</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>webprofile</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.classifier</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#tomeeGroupId">tomeeGroupId</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>org.apache.openejb</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.groupId</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#tomeeHost">tomeeHost</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>localhost</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.host</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#tomeeHttpPort">tomeeHttpPort</a></b></td>
            
<td><tt>int</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>8080</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.http</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#tomeeHttpsPort">tomeeHttpsPort</a></b></td>
            
<td><tt>Integer</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>User property is</b>: <tt>tomee-plugin.https</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#tomeeShutdownCommand">tomeeShutdownCommand</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>SHUTDOWN</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.shutdown-command</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#tomeeShutdownPort">tomeeShutdownPort</a></b></td>
            
<td><tt>int</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>8005</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.shutdown</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#tomeeVersion">tomeeVersion</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>-1</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.version</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#useConsole">useConsole</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>true</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.use-console</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#useOpenEJB">useOpenEJB</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>use openejb-standalone automatically instead of TomEE<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.openejb</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#user">user</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>User property is</b>: <tt>tomee-plugin.user</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#warFile">warFile</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.build.directory}/${project.build.finalName}.${project.packaging}</tt>.<br /></td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#webappClasses">webappClasses</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.build.outputDirectory}</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.webappClasses</tt>.</td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#webappDefaultConfig">webappDefaultConfig</a></b></td>
            
<td><tt>boolean</tt></td>
            
<td><tt>-</tt></td>
            
<td>forcing nice default for war development (WEB-INF/classes and web
resources)<br /><b>Default value is</b>: <tt>false</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.webappDefaultConfig</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#webappDir">webappDir</a></b></td>
            
<td><tt>String</tt></td>
            
<td><tt>-</tt></td>
            
<td>relative to tomee.base.<br /><b>Default value is</b>: <tt>webapps</tt>.<br /></td>
          </tr>
          
<tr class="b">
            
<td><b><a href="#webappResources">webappResources</a></b></td>
            
<td><tt>File</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /><b>Default value is</b>: <tt>${project.basedir}/src/main/webapp</tt>.<br /><b>User property is</b>: <tt>tomee-plugin.webappResources</tt>.</td>
          </tr>
          
<tr class="a">
            
<td><b><a href="#webapps">webapps</a></b></td>
            
<td><tt>List</tt></td>
            
<td><tt>-</tt></td>
            
<td>(no description)<br /></td>
          </tr>
        </table>
      </div>
      
<div class="section">
<h3>Parameter Details<a name="Parameter_Details"></a></h3>
        
<p><b><a name="apacheRepos">apacheRepos</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.apache-repos</tt></li>
          
<li><b>Default</b>: <tt>snapshots</tt></li>
        </ul><hr />
<p><b><a name="appDir">appDir</a>:</b></p>
        
<div>relative to tomee.base.</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>Default</b>: <tt>apps</tt></li>
        </ul><hr />
<p><b><a name="apps">apps</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="args">args</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.args</tt></li>
        </ul><hr />
<p><b><a name="bin">bin</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.bin</tt></li>
          
<li><b>Default</b>: <tt>${project.basedir}/src/main/tomee/bin</tt></li>
        </ul><hr />
<p><b><a name="catalinaBase">catalinaBase</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.catalina-base</tt></li>
          
<li><b>Default</b>: <tt>${project.build.directory}/apache-tomee</tt></li>
        </ul><hr />
<p><b><a name="checkStarted">checkStarted</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.check-started</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="classpaths">classpaths</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="config">config</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.conf</tt></li>
          
<li><b>Default</b>: <tt>${project.basedir}/src/main/tomee/conf</tt></li>
        </ul><hr />
<p><b><a name="context">context</a>:</b></p>
        
<div>rename the current artifact</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="debug">debug</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.debug</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="debugPort">debugPort</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>int</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.debugPort</tt></li>
          
<li><b>Default</b>: <tt>5005</tt></li>
        </ul><hr />
<p><b><a name="deployOpenEjbApplication">deployOpenEjbApplication</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.deploy-openejb-internal-application</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="docBases">docBases</a>:</b></p>
        
<div>for TomEE and wars only, which docBase to use for this war.</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="ejbRemote">ejbRemote</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.ejb-remote</tt></li>
          
<li><b>Default</b>: <tt>true</tt></li>
        </ul><hr />
<p><b><a name="externalRepositories">externalRepositories</a>:</b></p>
        
<div>for TomEE and wars only, add some external repositories to
classloader.</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="forceReloadable">forceReloadable</a>:</b></p>
        
<div>force webapp to be reloadable</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.force-reloadable</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="javaagents">javaagents</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="keepServerXmlAsthis">keepServerXmlAsthis</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.keep-server-xml</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="lib">lib</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.lib</tt></li>
          
<li><b>Default</b>: <tt>${project.basedir}/src/main/tomee/lib</tt></li>
        </ul><hr />
<p><b><a name="libDir">libDir</a>:</b></p>
        
<div>relative to tomee.base.</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>Default</b>: <tt>lib</tt></li>
        </ul><hr />
<p><b><a name="libs">libs</a>:</b></p>
        
<div>supported formats: --&gt; groupId:artifactId:version... --&gt;
unzip:groupId:artifactId:version... --&gt; remove:prefix (often
prefix = artifactId)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="mainDir">mainDir</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>Default</b>: <tt>${project.basedir}/src/main</tt></li>
        </ul><hr />
<p><b><a name="password">password</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.pwd</tt></li>
        </ul><hr />
<p><b><a name="quickSession">quickSession</a>:</b></p>
        
<div>use a real random instead of secure random. saves few ms at
startup.</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.quick-session</tt></li>
          
<li><b>Default</b>: <tt>true</tt></li>
        </ul><hr />
<p><b><a name="realm">realm</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.realm</tt></li>
        </ul><hr />
<p><b><a name="reloadOnUpdate">reloadOnUpdate</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.reload-on-update</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="removeDefaultWebapps">removeDefaultWebapps</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.remove-default-webapps</tt></li>
          
<li><b>Default</b>: <tt>true</tt></li>
        </ul><hr />
<p><b><a name="removeTomeeWebapp">removeTomeeWebapp</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.remove-tomee-webapps</tt></li>
          
<li><b>Default</b>: <tt>true</tt></li>
        </ul><hr />
<p><b><a name="simpleLog">simpleLog</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.simple-log</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="skipCurrentProject">skipCurrentProject</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.skipCurrentProject</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="skipWarResources">skipWarResources</a>:</b></p>
        
<div>when you set docBases to src/main/webapp setting it to true will
allow hot refresh.</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.skipWarResources</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="synchronization">synchronization</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>org.apache.openejb.maven.plugin.Synchronization</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="synchronizations">synchronizations</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="systemVariables">systemVariables</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.Map</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul><hr />
<p><b><a name="target">target</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>Default</b>: <tt>${project.build.directory}</tt></li>
        </ul><hr />
<p><b><a name="tomeeAjpPort">tomeeAjpPort</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>int</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.ajp</tt></li>
          
<li><b>Default</b>: <tt>8009</tt></li>
        </ul><hr />
<p><b><a name="tomeeAlreadyInstalled">tomeeAlreadyInstalled</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.exiting</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="tomeeArtifactId">tomeeArtifactId</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.artifactId</tt></li>
          
<li><b>Default</b>: <tt>apache-tomee</tt></li>
        </ul><hr />
<p><b><a name="tomeeClassifier">tomeeClassifier</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.classifier</tt></li>
          
<li><b>Default</b>: <tt>webprofile</tt></li>
        </ul><hr />
<p><b><a name="tomeeGroupId">tomeeGroupId</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.groupId</tt></li>
          
<li><b>Default</b>: <tt>org.apache.openejb</tt></li>
        </ul><hr />
<p><b><a name="tomeeHost">tomeeHost</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.host</tt></li>
          
<li><b>Default</b>: <tt>localhost</tt></li>
        </ul><hr />
<p><b><a name="tomeeHttpPort">tomeeHttpPort</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>int</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.http</tt></li>
          
<li><b>Default</b>: <tt>8080</tt></li>
        </ul><hr />
<p><b><a name="tomeeHttpsPort">tomeeHttpsPort</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.Integer</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.https</tt></li>
        </ul><hr />
<p><b><a name="tomeeShutdownCommand">tomeeShutdownCommand</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.shutdown-command</tt></li>
          
<li><b>Default</b>: <tt>SHUTDOWN</tt></li>
        </ul><hr />
<p><b><a name="tomeeShutdownPort">tomeeShutdownPort</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>int</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.shutdown</tt></li>
          
<li><b>Default</b>: <tt>8005</tt></li>
        </ul><hr />
<p><b><a name="tomeeVersion">tomeeVersion</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.version</tt></li>
          
<li><b>Default</b>: <tt>-1</tt></li>
        </ul><hr />
<p><b><a name="useConsole">useConsole</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.use-console</tt></li>
          
<li><b>Default</b>: <tt>true</tt></li>
        </ul><hr />
<p><b><a name="useOpenEJB">useOpenEJB</a>:</b></p>
        
<div>use openejb-standalone automatically instead of TomEE</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.openejb</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="user">user</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.user</tt></li>
        </ul><hr />
<p><b><a name="warFile">warFile</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>Default</b>: <tt>${project.build.directory}/${project.build.finalName}.${project.packaging}</tt></li>
        </ul><hr />
<p><b><a name="webappClasses">webappClasses</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.webappClasses</tt></li>
          
<li><b>Default</b>: <tt>${project.build.outputDirectory}</tt></li>
        </ul><hr />
<p><b><a name="webappDefaultConfig">webappDefaultConfig</a>:</b></p>
        
<div>forcing nice default for war development (WEB-INF/classes and web
resources)</div>
        
<ul>
          
<li><b>Type</b>: <tt>boolean</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.webappDefaultConfig</tt></li>
          
<li><b>Default</b>: <tt>false</tt></li>
        </ul><hr />
<p><b><a name="webappDir">webappDir</a>:</b></p>
        
<div>relative to tomee.base.</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.lang.String</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>Default</b>: <tt>webapps</tt></li>
        </ul><hr />
<p><b><a name="webappResources">webappResources</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.io.File</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
          
<li><b>User Property</b>: <tt>tomee-plugin.webappResources</tt></li>
          
<li><b>Default</b>: <tt>${project.basedir}/src/main/webapp</tt></li>
        </ul><hr />
<p><b><a name="webapps">webapps</a>:</b></p>
        
<div>(no description)</div>
        
<ul>
          
<li><b>Type</b>: <tt>java.util.List</tt></li>
          
<li><b>Required</b>: <tt>No</tt></li>
        </ul>
      </div>
    </div>
