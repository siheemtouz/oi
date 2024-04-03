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
<properties>
    <property name="javax.persistence.jdbc.url" value="jdbc:h2:mem:testdb" />
    <property name="javax.persistence.jdbc.user" value="sa" />
    <property name="javax.persistence.jdbc.password" value="" />
    <property name="javax.persistence.jdbc.driver" value="org.h2.Driver" />
    <property name="hibernate.show_sql" value="true" />
    <property name="hibernate.format_sql" value="true" />
    <property name="hibernate.dialect" value="org.hibernate.dialect.H2Dialect"/>
</properties>



<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:context="http://www.springframework.org/schema/context"
    xsi:schemaLocation="
        http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context.xsd">

    <!-- Bean configurations go here -->

    <!-- Component scanning for Spring components -->
    <context:component-scan base-package="com.example"/>

</beans>
État HTTP 500 – Erreur interne du serveur
Type Rapport d'exception

message "Servlet.init()" pour la servlet [DispatcherServlet] a généré une exception

description Le serveur a rencontré une erreur interne qui l'a empêché de satisfaire la requête.

exception

javax.servlet.ServletException: "Servlet.init()" pour la servlet [DispatcherServlet] a généré une exception
	org.apache.catalina.authenticator.AuthenticatorBase.invoke(AuthenticatorBase.java:483)
	org.apache.catalina.valves.ErrorReportValve.invoke(ErrorReportValve.java:93)
	org.apache.catalina.valves.AbstractAccessLogValve.invoke(AbstractAccessLogValve.java:679)
	org.apache.catalina.connector.CoyoteAdapter.service(CoyoteAdapter.java:346)
	org.apache.coyote.http11.Http11Processor.service(Http11Processor.java:617)
	org.apache.coyote.AbstractProcessorLight.process(AbstractProcessorLight.java:63)
	org.apache.coyote.AbstractProtocol$ConnectionHandler.process(AbstractProtocol.java:934)
	org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1690)
	org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:52)
	org.apache.tomcat.util.threads.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1191)
	org.apache.tomcat.util.threads.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:659)
	org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:63)
	java.lang.Thread.run(Thread.java:745)
cause mère

org.springframework.beans.factory.BeanDefinitionStoreException: IOException parsing XML document from class path resource [contextFront.xml]; nested exception is java.io.FileNotFoundException: class path resource [contextFront.xml] cannot be opened because it does not exist
	org.springframework.beans.factory.xml.XmlBeanDefinitionReader.loadBeanDefinitions(XmlBeanDefinitionReader.java:344)
	org.springframework.beans.factory.xml.XmlBeanDefinitionReader.loadBeanDefinitions(XmlBeanDefinitionReader.java:304)
	org.springframework.beans.factory.support.AbstractBeanDefinitionReader.loadBeanDefinitions(AbstractBeanDefinitionReader.java:181)
	org.springframework.beans.factory.support.AbstractBeanDefinitionReader.loadBeanDefinitions(AbstractBeanDefinitionReader.java:217)
	org.springframework.beans.factory.support.AbstractBeanDefinitionReader.loadBeanDefinitions(AbstractBeanDefinitionReader.java:188)
	org.springframework.web.context.support.XmlWebApplicationContext.loadBeanDefinitions(XmlWebApplicationContext.java:125)
	org.springframework.web.context.support.XmlWebApplicationContext.loadBeanDefinitions(XmlWebApplicationContext.java:94)
	org.springframework.context.support.AbstractRefreshableApplicationContext.refreshBeanFactory(AbstractRefreshableApplicationContext.java:129)
	org.springframework.context.support.AbstractApplicationContext.obtainFreshBeanFactory(AbstractApplicationContext.java:613)
	org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:514)
	org.springframework.web.servlet.FrameworkServlet.configureAndRefreshWebApplicationContext(FrameworkServlet.java:668)
	org.springframework.web.servlet.FrameworkServlet.createWebApplicationContext(FrameworkServlet.java:634)
	org.springframework.web.servlet.FrameworkServlet.createWebApplicationContext(FrameworkServlet.java:682)
	org.springframework.web.servlet.FrameworkServlet.initWebApplicationContext(FrameworkServlet.java:553)
	org.springframework.web.servlet.FrameworkServlet.initServletBean(FrameworkServlet.java:494)
	org.springframework.web.servlet.HttpServletBean.init(HttpServletBean.java:136)
	javax.servlet.GenericServlet.init(GenericServlet.java:143)
	org.apache.catalina.authenticator.AuthenticatorBase.invoke(AuthenticatorBase.java:483)
	org.apache.catalina.valves.ErrorReportValve.invoke(ErrorReportValve.java:93)
	org.apache.catalina.valves.AbstractAccessLogValve.invoke(AbstractAccessLogValve.java:679)
	org.apache.catalina.connector.CoyoteAdapter.service(CoyoteAdapter.java:346)
	org.apache.coyote.http11.Http11Processor.service(Http11Processor.java:617)
	org.apache.coyote.AbstractProcessorLight.process(AbstractProcessorLight.java:63)
	org.apache.coyote.AbstractProtocol$ConnectionHandler.process(AbstractProtocol.java:934)
	org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1690)
	org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:52)
	org.apache.tomcat.util.threads.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1191)
	org.apache.tomcat.util.threads.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:659)
	org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:63)
	java.lang.Thread.run(Thread.java:745)
cause mère

java.io.FileNotFoundException: class path resource [contextFront.xml] cannot be opened because it does not exist
	org.springframework.core.io.ClassPathResource.getInputStream(ClassPathResource.java:172)
	org.springframework.beans.factory.xml.XmlBeanDefinitionReader.loadBeanDefinitions(XmlBeanDefinitionReader.java:330)
	org.springframework.beans.factory.xml.XmlBeanDefinitionReader.loadBeanDefinitions(XmlBeanDefinitionReader.java:304)
	org.springframework.beans.factory.support.AbstractBeanDefinitionReader.loadBeanDefinitions(AbstractBeanDefinitionReader.java:181)
	org.springframework.beans.factory.support.AbstractBeanDefinitionReader.loadBeanDefinitions(AbstractBeanDefinitionReader.java:217)
	org.springframework.beans.factory.support.AbstractBeanDefinitionReader.loadBeanDefinitions(AbstractBeanDefinitionReader.java:188)
	org.springframework.web.context.support.XmlWebApplicationContext.loadBeanDefinitions(XmlWebApplicationContext.java:125)
	org.springframework.web.context.support.XmlWebApplicationContext.loadBeanDefinitions(XmlWebApplicationContext.java:94)
	org.springframework.context.support.AbstractRefreshableApplicationContext.refreshBeanFactory(AbstractRefreshableApplicationContext.java:129)
	org.springframework.context.support.AbstractApplicationContext.obtainFreshBeanFactory(AbstractApplicationContext.java:613)
	org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:514)
	org.springframework.web.servlet.FrameworkServlet.configureAndRefreshWebApplicationContext(FrameworkServlet.java:668)
	org.springframework.web.servlet.FrameworkServlet.createWebApplicationContext(FrameworkServlet.java:634)
	org.springframework.web.servlet.FrameworkServlet.createWebApplicationContext(FrameworkServlet.java:682)
	org.springframework.web.servlet.FrameworkServlet.initWebApplicationContext(FrameworkServlet.java:553)
	org.springframework.web.servlet.FrameworkServlet.initServletBean(FrameworkServlet.java:494)
	org.springframework.web.servlet.HttpServletBean.init(HttpServletBean.java:136)
	javax.servlet.GenericServlet.init(GenericServlet.java:143)
	org.apache.catalina.authenticator.AuthenticatorBase.invoke(AuthenticatorBase.java:483)
	org.apache.catalina.valves.ErrorReportValve.invoke(ErrorReportValve.java:93)
	org.apache.catalina.valves.AbstractAccessLogValve.invoke(AbstractAccessLogValve.java:679)
	org.apache.catalina.connector.CoyoteAdapter.service(CoyoteAdapter.java:346)
	org.apache.coyote.http11.Http11Processor.service(Http11Processor.java:617)
	org.apache.coyote.AbstractProcessorLight.process(AbstractProcessorLight.java:63)
	org.apache.coyote.AbstractProtocol$ConnectionHandler.process(AbstractProtocol.java:934)
	org.apache.tomcat.util.net.NioEndpoint$SocketProcessor.doRun(NioEndpoint.java:1690)
	org.apache.tomcat.util.net.SocketProcessorBase.run(SocketProcessorBase.java:52)
	org.apache.tomcat.util.threads.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1191)
	org.apache.tomcat.util.threads.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:659)
	org.apache.tomcat.util.threads.TaskThread$WrappingRunnable.run(TaskThread.java:63)
	java.lang.Thread.run(Thread.java:745)
note La trace complète de la cause mère de cette erreur est disponible dans les fichiers journaux de ce serveur.

Apache Tomcat/8.5.100
