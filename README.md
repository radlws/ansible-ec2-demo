# ansible-ec2-demo

Used to provision new amazon EC2 instances for use with Django / posgres / nginx. New volumes are created for /home and for postgres data. After the provision is done, fabric can be used to setup the web server and run deploys. In the future, can be tweaked to upgrade old ec2 servers to new ones.  It can also help with turning a server from a pet to cattle.

See install.md
