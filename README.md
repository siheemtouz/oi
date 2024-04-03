<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:p="http://www.springframework.org/schema/p"
    xmlns:context="http://www.springframework.org/schema/context"
    xsi:schemaLocation="
        http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context.xsd">

	<!-- this file is parsed when the spring DispatcherServlet is launched by the web server -->

	<!-- Beans discovery -->
    <context:component-scan base-package="com.openclassrooms"/>

	<!-- 	JSP templates discovery -->
	<bean id="viewResolver"
    	class="org.springframework.web.servlet.view.InternalResourceViewResolver" >
        <property name="prefix">
            <value>/WEB-INF/templates/</value>
        </property>
        <property name="suffix">
            <value>.jsp</value>
        </property>
    </bean>

</beans>

Description	Resource	Path	Location	Type
cvc-elt.1.a: Cannot find the declaration of element 'beans'.	contextFront.xml	/crud-demo/src/main/resources	line 2	Language Servers
Description	Resource	Path	Location	Type
Downloading external resources is disabled.	contextFront.xml	/crud-demo/src/main/resources	line 8	Language Servers
Description	Resource	Path	Location	Type
Referenced file contains errors (http://www.springframework.org/schema/context/spring-context.xsd).  For more information, right click on the message in the Problems View and select "Show Details..."	contextFront.xml	/crud-demo/src/main/resources	line 1	XML Problem


corrected:
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:context="http://www.springframework.org/schema/context"
    xsi:schemaLocation="
        http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context.xsd">

    <!-- Beans discovery -->
    <context:component-scan base-package="com.openclassrooms"/>

    <!-- JSP templates discovery -->
    <bean id="viewResolver"
        class="org.springframework.web.servlet.view.InternalResourceViewResolver" >
        <property name="prefix">
            <value>/WEB-INF/templates/</value>
        </property>
        <property name="suffix">
            <value>.jsp</value>
        </property>
    </bean>

</beans>
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:context="http://www.springframework.org/schema/context"
    xsi:schemaLocation="
        http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/context
        classpath:spring-context.xsd">

    <!-- Your bean definitions here -->

</beans>

