docker-compose-gitea
=================

Ansible role to set up [gitea](https://github.com/go-gitea/gitea) with docker-compose, as in [this tutorial](https://docs.gitea.io/en-us/install-with-docker).
Nginx configured as a proxy pass to gitea container port, with https and crontab job to update [certificate](https://certbot.eff.org).

Initially I made an ansible script which works fine on my aws server, which later I made into galaxy role, so feel free to contact me if it is not works for you, or fork it, as it is raw and I did not test this version of script properly.


Role Variables
--------------
* ``gitea_container_name``: name of docker container for gitea
* ``gitea_db_container_name``: name of docker container for postgress
* ``gitea_postgress_password``: database password for gitea
* ``gitea_become_pass``: sudo pass on target server
* ``gitea_server_name``: the baseurl (your result server should be available at https://{{ gitea_server_name }})
* ``gitea_certbot_mail``: mail for letsencrypt certificate generation

License
-------
GPLv3

Author Information
------------------
Original : [ubermensh](https://github.com/ubermensh)
