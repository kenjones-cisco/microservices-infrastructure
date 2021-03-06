Docker
======

.. versionadded:: 0.1

`Docker <https://www.docker.com/>`_ is a container manager and scheduler. In
their words, it "allows you to package an application with all of its
dependencies into a standardized unit for software development." Their site has
`more on what Docker is <https://www.docker.com/whatisdocker>`_. We use it in
microservices-infrastructure to ship units of work around the cluster, combined
with :doc:`marathon`'s scheduling.

Using a private Docker registry
-------------------------------

In addition to the open, official Docker registry at https://hub.docker.com,
one can use a private in-house docker registry for storing and pulling images.
Docker Hub also supports storing private images.

One must configure credentials in order to use private repositories. This is
done with the security-setup script, run it with the flag
``--use-private-docker-registry=true``. It will then ask you for username,
password and e-mail address for the registry user. You can also specify a custom
URL for an in-house Docker registry, or omit it, in which case it will default
to the official registry, https://index.docker.io/v1/.
