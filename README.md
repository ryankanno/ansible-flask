# ansible-flask

This is a role to deploy a nginx - uwsgi - flask application.


## Install

* `pip install -r requirements.txt`

### Vagrant

To test the role w/ Vagrant, run the following command:

* `FLASK_APPLICATION_PATH=/path/to/flask/application vagrant up`

To provision the server, make sure the following is set in the Vagrantfile:

`ansible.playbook = "provisioning/ansible/deploy.yml"`

To deploy new versions of the code, make sure the following is set in the
Vagrantfile:

`ansible.playbook = "provisioning/ansible/site.yml"`
