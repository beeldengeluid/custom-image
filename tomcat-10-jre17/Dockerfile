# Use the official Tomcat 10 image with Java 17 as a parent image
FROM tomcat:10-jre17

# Copy the CORS snippet first
COPY common/cors-snippet.xml /tmp/cors-snippet.xml

# Inject the CORS filter after the marker line in web.xml
RUN sed -i '/<!-- ==================== Built In Filter Mappings ====================== -->/r /tmp/cors-snippet.xml' /usr/local/tomcat/conf/web.xml

