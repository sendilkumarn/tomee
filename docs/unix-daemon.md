index-group=Unrevised
type=page
status=published
title=Unix Daemon
~~~~~~

Apache TomEE can be run as a daemon using the [jsvc](http://commons.apache.org/daemon/jsvc.html) tool from the [Apache Commons Daemon](http://commons.apache.org/daemon) project.

Source tarballs for `jsvc` are included with Tomcat and therefore can be found in TomEE as well.  These need to be compiled before jsvc can be used. 

# Building jsvc

First, we'll need to locate and unpack the `commons-daemon-native.tar.gz`

    cd $TOMEE_HOME/bin
    tar xzvf commons-daemon-native.tar.gz
    cd commons-daemon-1.0.7-native-src/unix/

Note that the `commons-daemon-1.0.7-native-src` directory may have a slightly different version number.

Second, we'll need to build the `jsvc` binary.  Under a UNIX operating system you will need:

 - An ANSI-C compliant compiler (GCC is good)
 - GNU Make
 - A Java Platform 2 compliant SDK

You have to specify the `JAVA_HOME` of the SDK either with the `--with-java=<dir>` parameter or set the `JAVA_HOME` environment to 
point to your SDK installation. For example:

    ./configure --with-java=/usr/java

or

    export JAVA_HOME
    ./configure

If your operating system is supported, configure will go through cleanly, otherwise it will report an error (please send us the details of your 
OS/JDK, or a patch against the sources). To build the binaries and libraries simply do:

    make

This will generate the executable file `jsvc`.

Finally, we'll want to set the execution bits and move the `jsvc` binary

    chmod 755 jsvc
    mv jsvc $TOMEE_HOME/bin

Done!

As one script, the above might look like:

    cd $TOMEE_HOME/bin
    tar xzvf commons-daemon-native.tar.gz
    cd commons-daemon-1.0.7-native-src/unix/
    ./configure
    make
    chmod 755 jsvc
    mv jsvc ../..

# Starting (unix)

    sudo "$TOMEE_HOME/bin/jsvc" -cp "$TOMEE_HOME/bin/bootstrap.jar:$TOMEE_HOME/bin/tomcat-juli.jar" \
        "-javaagent:$TOMEE_HOME/lib/openejb-javaagent.jar" -outfile "$TOMEE_HOME/logs/catalina.out" \
        -errfile "$TOMEE_HOME/logs/catalina.err" org.apache.catalina.startup.Bootstrap

# Starting (osx)

For a 64-bit JVM such as OSX Lion

    sudo arch -arch x86_64 "$TOMEE_HOME/bin/jsvc" -jvm server -cp "$TOMEE_HOME/bin/bootstrap.jar:$TOMEE_HOME/bin/tomcat-juli.jar" \
        "-javaagent:$TOMEE_HOME/lib/openejb-javaagent.jar" -outfile "$TOMEE_HOME/logs/catalina.out" \
        -errfile "$TOMEE_HOME/logs/catalina.err" org.apache.catalina.startup.Bootstrap

For a 32-bit JVM

    sudo arch -arch i386 "$TOMEE_HOME/bin/jsvc" -jvm server -cp "$TOMEE_HOME/bin/bootstrap.jar:$TOMEE_HOME/bin/tomcat-juli.jar" \
        "-javaagent:$TOMEE_HOME/lib/openejb-javaagent.jar" -outfile "$TOMEE_HOME/logs/catalina.out" \
        -errfile "$TOMEE_HOME/logs/catalina.err" org.apache.catalina.startup.Bootstrap

## Note on formatting

Note that `\` at the end of each line is unix syntax to keep everything effectively as one line and one command.  The command is simply too long to show as one line on a fixed width html page.  The `\` can be removed as long as the resulting command is one long line.

# Common Issues

Ensure your `$TOME_HOME` and `$JAVA_HOME` variables are set correctly.  You should see similar output with the following two commands

    mingus:~ 01:51:37
    $ ls $TOMEE_HOME
    LICENSE		RELEASE-NOTES	bin		endorsed	logs		webapps
    NOTICE		RUNNING.txt	conf		lib		temp		work

    mingus:~ 01:51:46
    $ ls $JAVA_HOME
    bin	bundle	lib	man

The `jsvc -debug` option can also show useful information for troubleshooting:

    $TOMEE_HOME/bin/jsvc -debug

Note on OSX, `$JAVA_HOME` should be set to `/System/Library/Frameworks/JavaVM.framework/Home`

# Further documentation

See also the full Apache Commons Daemon documentation for jsvc.

  - [http://commons.apache.org/daemon/jsvc.html](http://commons.apache.org/daemon/jsvc.html)
