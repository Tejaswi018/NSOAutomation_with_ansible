# NSOAutomation_with_ansible
The project is to implement a simple (flask)app.

I deployed 5 servers HAproxy, devA, devB, devC and Bastion in citycloud. HAproxy and Bastion has floating IP and all the dev srevers has private IP. HAproxy acts as a load balancer for devservers. Ansible-playbook is written to deploy HAproxy and Flask app and install SNMPd daemon onto the dev servers to monitor.
HAproxy cannot be handled with UDP therefore Nginx is used to load-balance. HAproxy takes care of the flask app while Nginx takes care of SNMP.

When I try to curl it replies by providing the time and hostname of the host that replied.
