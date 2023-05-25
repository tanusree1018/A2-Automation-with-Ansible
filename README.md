# A2-Automation-with-Ansible

For this A2.2, I'm using a straightforward Python-Flask application called application.py, which I've hidden behind the HAproxy, a load balancer between the three development servers devA, devB, and devC. A bastion host is made with the intention of serving as the network's main SSH entry point. 

Using city cloud, a total of 5 servers have been deployed. While Dev servers only have private IP addresses, BastionNSO host and HAproxy are given floating IP addresses.

Our flask application is deployed to development servers using ansible-playbook "site.yaml," and we deploy the haproxy load balancing configuration file to perform load balancing among them.

For testing, all we need to do is curl to the haproxy IP address, and it should respond with the time and hostname of the responding host.
Additionally, I used Nginx to perform UDP load balancing.
