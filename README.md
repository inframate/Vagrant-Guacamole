# vagrant-guacamole
Vagrantfile and script to set up a CentOS 7.1 VM on Virtualbox and provision it with guacamole

Vagrantfile: Uses "bento/ubuntu-16.04" Vagrant Box to set up an Ubuntu Xenial 16.04 Server with :

- 10246 MB RAM
- 1 CPU
- 1 NAT adapter
- 1 Host only adapter with IP address = "192.168.88.100"
- Hostname="GuacamoleVM"
- User/Password=vagrant/vagrant
- ssh key managed by vagrant ( to manage ssh keys uncomment the section (ssh key management) and change the path to your own key)
- Provisionning script (Provision-script.sh):
    *based on the following script http://pilotfiber.dl.sourceforge.net/project/guacamoleinstallscript/CentOS/guacamole-install-script.sh
