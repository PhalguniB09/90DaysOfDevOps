##Commands to deploy realtime webserver

#connect with remote machine ssh username@hostIPAddress
#sudo apt install nginx -y
#sudo systemctl nginx status
#sudo tail -n 20 /var/log/nginix/access.log
cp /var/log/nginx/access.log ~/nginx_logs/server_nginx.log


Nginx listens on port 80 by default HTTPS works on port 443 and needs SSL certificates.
