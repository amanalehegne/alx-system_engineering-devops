#!/usr/bin/env bash
# Script that configures HAproxy in a load balancer 
apt-get -y install software-properties-common
add-apt-repository -y ppa:vbernat/haproxy-2.0
apt-get -y update
apt-get -y install haproxy=2.0.\*
echo -e "\nfrontend http\n\tbind *:80\n\tmode http\n\tdefault_backend web-backend\n\nbackend web-backend\n\tbalance roundrobin\n\tserver 17682-web-01 18.208.132.93:80 check\n\tserver 17682-web-02 34.204.195.240:80 check" >> /etc/haproxy/haproxy.cfg
service haproxy restart