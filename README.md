# ansible-flask

This is a role to deploy a nginx - uwsgi - flask application. To see how it
works, the example below requires a clone of [flask-skeleton](https://github.com/ryankanno/flask-skeleton).
With that said, once you see how it works, you should be able to use it to
deploy any flask application.

## Install

* `pip install -r requirements.txt`
* clone of [https://github.com/ryankanno/flask-skeleton](https://github.com/ryankanno/flask-skeleton)

### Vagrant

To test the role w/ Vagrant, run the following command:

* `FLASK_APPLICATION_PATH=/path/to/clone/of/flask_skeleton vagrant up`

To provision the server, make sure the following is set in the Vagrantfile:

`ansible.playbook = "provisioning/ansible/site.yml"`

To deploy new versions of the code, make sure the following is set in the
Vagrantfile:

`ansible.playbook = "provisioning/ansible/deploy.yml"`

After things are deployed, you'll need to execute the following:

* `vagrant ssh`
* `sudo supervisord -c /etc/supervisor/supervisord.conf`

## Running

To see the fruits of your labor, you should be able to execute the following:

`curl http://localhost:50060` or `open http://localhost:50060`

## Tips

If you ever receive a Bad Gateway error after either curling or opening a
browser, you'll want to make sure that supervisor is started within the Vagrant
instance.

If you curl/open the site and there aren't any styles, make sure to go into the
[flask-skeleton](https://github.com/ryankanno/flask-skeleton) clone and run the
following: `bower install`. This will bring down all the css assets.
