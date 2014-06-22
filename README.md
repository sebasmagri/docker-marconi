## OpenStack Marconi on Docker ##

Each Dockerfile in this repo implements an instance of [Marconi](https://wiki.openstack.org/wiki/Marconi) Queues intended for development and testing. Thus, the setup is kept as simple as possible; no sharding, no auth, no memcached, runs on gunicorn with gevent.

You will find several directories. Each of these are intended to hold the files to build a release of Marconi.

You can find these images in the docker index and use them directly. For example, to run Marconi 2014.1:

    $ MARCONI=$(docker run -d -p 0.0.0.0:8080:80 sebasmagri/docker-marconi:2014.1)

Check if everything started:

    $ docker logs $MARCONI

Forks, patches and different setups are completely welcome.
