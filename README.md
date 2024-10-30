# TomcatUserData
TomcatUserData for Amazon Linux 2023


rolename="manager-gui"
rolename="manager-script"
rolename="manager-jmx"
rolename="manager-status"/
username="admin" password="admin" roles="manager-gui,manager-script,manager-jmx,manager-status"
username="deployer" password="deployer" roles="manager-script"
username="tomcat" password="s3cret" roles="manager-gui"/>' "$TOMCAT_USERS_FILE"
