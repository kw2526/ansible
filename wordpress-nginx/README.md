
## Spin up a Docker instance 

docker run -i -t  --name wordpressV1.0 centos:ansiclient /bin/bash 
Note down it's ipv4 address and add it on the hosts file 

#cat hosts  
[wordpress]
172.17.0.8


## WordPress+Nginx+PHP-FPM Deployment

- Requires Ansible 1.2 or newer
- Expects CentOS/RHEL 6.x hosts

These playbooks deploy a simple all-in-one configuration of the popular
WordPress blogging platform and CMS, frontend by the Nginx web server and the
PHP-FPM process manager. 

Then run the playbook, like this:

	ansible-playbook -i hosts site.yml

The playbooks will configure MySQL, WordPress, Nginx, and PHP-FPM. When the run
is complete, you can hit access server to begin the WordPress configuration.

### Ideas for Improvement

Here are some ideas for ways that these playbooks could be extended:

- Parameterize the WordPress deployment to handle multi-site configurations.
- Separate the components (PHP-FPM, MySQL, Nginx) onto separate hosts and 
handle the configuration appropriately.
- Handle WordPress upgrades automatically.

We would love to see contributions and improvements, so please fork this
repository on GitHub and send us your changes via pull requests.
