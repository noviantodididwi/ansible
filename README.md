Introduction
===============

Ansible is a configuration management tool that system administrators use to automate infrastructure management activities.
Ansible uses only SSH to run commands remotely, and thus does not need an agent on the remote server. This makes Ansible preferable over other popular tools like Puppet or Chef when you don't want to install agents on the managed servers.
Moreover, it is much easier to get started with Ansible because it uses YAML (Yet Another Markup Language) which is simpler than the more powerful programming languages that other tools use.


Ansible / redis
-----

Ansible playbook to install and setup a Redis upstart service.



Usage
-----

Create an inventory file with the servers that you want to Node.js on or use `$ANSIBLE_HOSTS`.

if connecting with root:

    ansible-playbook -i hosts -u root main.yml

if sudoing:

    ansible-playbook -i hosts -K main.yml

It installs a `redis-local` script that is useful to use instead of `redis-cli` if you set a different port and password.



Ansible
-------

Not sure what Ansible is? Read the getting started here: http://procbits.com/2013/09/08/getting-started-with-ansible-digital-ocean


Redis
-----

Read docs here: http://redis.io/documentation



Todo
----

- make OS agnostic
- add `vm.overcommit_memory` setting, see: http://ubuntuforums.org/showthread.php?t=1150453, http://www.redhat.com/magazine/001nov04/features/vm/, http://redis.io/topics/faq


Directory structure should look like
----

??? ansible.cfg
??? CHANGELOG.md
??? hosts
??? main.yml
??? README.md
??? redis-version.yml
??? templates
?   ??? redis.conf
?   ??? redis-daemon
?   ??? redis.log
??? vars.yml

