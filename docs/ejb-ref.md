index-group=Unrevised
type=page
status=published
title=ejb-ref
~~~~~~
<a name="ejb-ref-Viaannotation"></a>
#  Via annotation

    package org.superbiz.refs;

    import javax.ejb.EJB;
    import javax.ejb.Stateless;
    import javax.naming.InitialContext;

    @Stateless
    @EJB(name = "myFooEjb", beanInterface = FooRemote.class)
    public class MyEjbRemoteRefBean implements MyBeanInterface {

        @EJB
        private BarRemote myBarEjb;

        public void someBusinessMethod() throws Exception {
            if (myBarEjb == null) throw new NullPointerException("myBarEjb not injected");

            // Both can be looked up from JNDI as well
            InitialContext context = new InitialContext();
            FooRemote fooRemote = (FooRemote) context.lookup("java:comp/env/myFooEjb");
            BarRemote barRemote = (BarRemote) context.lookup("java:comp/env/org.superbiz.refs.MyEjbRemoteRefBean/myBarEjb");
        }
    }


<a name="ejb-ref-Viaxml"></a>
# Via xml

The above @EJB annotation usage is 100% equivalent to the following xml.

    <ejb-ref>
        <ejb-ref-name>myFooEjb</ejb-ref-name>
        <remote>org.superbiz.refs.FooRemote</remote>
    </ejb-ref>
    <ejb-ref>

    <ejb-ref-name>org.superbiz.refs.MyEjbRemoteRefBean/myBarEjb</ejb-ref-name>
        <remote>org.superbiz.refs.BarRemote</remote>
        <injection-target>
          <injection-target-class>org.superbiz.refs.MyEjbRemoteRefBean</injection-target-class>
          <injection-target-name>myBarEjb</injection-target-name>
        </injection-target>
    </ejb-ref>
