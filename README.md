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

TO UPDATE THE USER LOGINS SSH AND DO THE FOLLOWING

   TOMCAT_USERS_FILE="/opt/tomcat/conf/tomcat-users.xml"
   # Edit tomcat-users.xml to add roles and users
if [ -f "$TOMCAT_USERS_FILE" ]; then
  echo "Updating $TOMCAT_USERS_FILE..."
  sudo sed -i '/<\/tomcat-users>/i \
  <role rolename="manager-gui"/>\n\
  <role rolename="manager-script"/>\n\
  <role rolename="manager-jmx"/>\n\
  <role rolename="manager-status"/>\n\
  <user username="admin" password="admin" roles="manager-gui,manager-script,manager-jmx,manager-status"/>\n\
  <user username="deployer" password="deployer" roles="manager-script"/>\n\
  <user username="tomcat" password="s3cret" roles="manager-gui"/>' "$TOMCAT_USERS_FILE"

  # Restart Tomcat service
echo "Restarting Tomcat service..."
sudo systemctl restart tomcat

echo "Configuration completed."




   

   
