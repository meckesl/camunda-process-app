Tomcat web.xml + CORS
---
    <filter>
      <filter-name>CorsFilter</filter-name>
      <filter-class>org.apache.catalina.filters.CorsFilter</filter-class>
      <init-param>
        <param-name>cors.allowed.origins</param-name>
        <param-value>*</param-value>
      </init-param>
      <init-param>
        <param-name>cors.allowed.methods</param-name>
        <param-value>GET,POST,HEAD,OPTIONS,PUT,DELETE</param-value>
      </init-param>
      <init-param>    
            <param-name>cors.allowed.headers</param-name>     
            <param-value>Content-Type,X-Requested-With,accept,Origin,Access-Control-Request-Method,Access-Control-Request-Headers,Authorization</param-value>     
        </init-param>    
        <init-param>    
            <param-name>cors.exposed.headers</param-name>     
            <param-value>Access-Control-Allow-Origin</param-value>      
        </init-param>    
    </filter>
    <filter-mapping>
      <filter-name>CorsFilter</filter-name>
      <url-pattern>/*</url-pattern>
    </filter-mapping>
    
