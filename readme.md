Bash Script to Launch EC2

#!/bin/bash
yum update –y
yum install httpd -y
service httpd start
chkconfig httpd on
aws s3 cp s3://jit-s3/index.html /var/www/html
