index-group=Unrevised
type=page
status=published
title=Basics - Security
~~~~~~
This section is under construction, please check back later.

<a name="Basics-Security-RelatedDocuments"></a>
## Related Documents

[Security](security.html)
 \- login module configuration
[Security Annotations](security-annotations.html)
 \- EJB3 related annotation based security.

<a name="Basics-Security-ServerSideSecurity"></a>
## Server Side Security

There's a few things that should be noted about security from the server
side perspective.

<a name="Basics-Security-SecurityPropagation"></a>
### Security Propagation
Note, this is partially documented in the EJB 3 spec section 14.8.1.1.

1. Once a remote bean has been instantiated, from within the container, it
inherits the entire security context, and all roles will be inherited the
same as the method where the bean is being looked up.
1. Looking up a bean via an `InitialContext`, or via injection, will inherit
the security context (user, roles, etc), thereby propagating the security
through to any container bean in the chain of method calls.
1. No properties are allowed for the `InitialContext`, and you *MUST* be
calling the no args constructor only.  There are documents elsewhere that
describe using the OpenEJB initial context factories and such, with
usernames and passwords, etc; it should be noted that this method of using
the factories is OpenEJB specific, to facilitate non-standard clients not
running in an EJB container, etc.

For example, here is an EJB that returns another bean, through a remote
method call.  In this case, the *OtherBean* instance, will have the same
security as *MyBean*, including the principal (username), roles, etc.


    import javax.ejb.EJB;
    import javax.naming.InitialContext;
    
    @EJB(name = "otherBean", beanInterface = IOtherBean.class)
    public class MyBean
    {
        public IOtherBean getOtherBean()
        {
    	InitialContext context = new InitialContext();
    	return (IOtherBean) context.lookup("java:comp/env/otherBean");
        }
    }
