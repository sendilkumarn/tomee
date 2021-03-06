index-group=Testing Techniques
type=page
status=published
title=Configuring Containers in Tests
~~~~~~
Like Resources, Containers can also be declared via InitialContext
properties as well.  The most useful is to declare a Stateful SessionBean
container so that it's guaranteed to passivate and activate on each call to
the bean, allowing you to test your callbacks behave as you need them to.


    Properties p = new Properties();
    p.put(Context.INITIAL_CONTEXT_FACTORY, "org.apache.openejb.core.LocalInitialContextFactory");
    
    p.put("myStatefulContainer", "new://Container?type=STATEFUL");
    p.put("myStatefulContainer.PoolSize", "0");
    p.put("myStatefulContainer.BulkPassivate", "1");
    
    Context context = new InitialContext(p);


Note, this only works when using the LocalInitialContextFactory to embed
OpenEJB into the vm.  Once embedded, further configuration properties are
ignored.

See [Containers and Resources](containers-and-resources.html)
 for a full list of supported Resource types and their properties.
