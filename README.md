# hello-World

<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://java.sun.com/xml/ns/javaee" xmlns:web="http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd"
	xsi:schemaLocation="http://java.sun.com/xml/ns/javaee 
	http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd" id="FileCompareProject"
	version="2.5">
	<display-name>FileCompare</display-name>
	<context-param>
		<param-name>contextConfigLocation</param-name>
		<param-value>/WEB-INF/spring/applicationContext.xml</param-value>
	</context-param>
	<!-- Add Support for Spring -->
	<listener>
		<listener-class>org.springframework.web.context.ContextLoaderListener
		</listener-class>
	</listener>
	<listener>
		<listener-class>org.springframework.web.context.request.RequestContextListener
		</listener-class>
	</listener>
	<!-- Change to "Production" when you are ready to deploy -->
	<context-param>
		<param-name>javax.faces.PROJECT_STAGE</param-name>
		<param-value>Development</param-value>
	</context-param>
	<!-- Welcome page -->
	<welcome-file-list>
		<welcome-file>showRepositories.xhtml</welcome-file>
	</welcome-file-list>
	<!-- JSF Mapping -->
	<servlet>
		<servlet-name>facesServlet</servlet-name>
		<servlet-class>javax.faces.webapp.FacesServlet</servlet-class>
		<load-on-startup>1</load-on-startup>
	</servlet>
	<servlet-mapping>
		<servlet-name>facesServlet</servlet-name>
		<url-pattern>*.xhtml</url-pattern>
	</servlet-mapping>
</web-app>
