# TomcatUserData
TomcatUserData for Amazon Linux 2023


rolename="manager-gui"

rolename="manager-script"

rolename="manager-jmx"

rolename="manager-status"/

username="admin" password="admin" roles="manager-gui,manager-script,manager-jmx,manager-status"

username="deployer" password="deployer" roles="manager-script"

username="tomcat" password="s3cret" roles="manager-gui"


1. Tomcat Default Home Page
   http://<your-ec2-public-dns>:8080/

2. Tomcat Manager (Application Management)
   http://<your-ec2-public-dns>:8080/manager/html

3. Host Manager (Virtual Host Management)
   http://<your-ec2-public-dns>:8080/host-manager/html

4. Admin Console (If Enabled Separately)
   http://<your-ec2-public-dns>:8080/admin

5. JMX Proxy Servlet (JMX Monitoring)
   http://<your-ec2-public-dns>:8080/manager/jmxproxy

6. Documentation
   http://<your-ec2-public-dns>:8080/docs/

7. Examples (Servlet/JSP Examples)
   http://<your-ec2-public-dns>:8080/examples/



   

   
