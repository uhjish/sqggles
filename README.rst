sqggles
=======

dashboarding

Getting Started
---------------

To start developing on this project simply bring up the Docker setup:

.. code-block:: bash

    docker-compose up --build

Open your web browser at http://localhost (on a Linux host) or
http://<docker-machine-ip-address> (on OS X and Windows), usually the
IP address of the VirtualBox VM called ``default``, to see the application
you're developing.  Log output will be displayed in the terminal, as usual.

Working with Docker
^^^^^^^^^^^^^^^^^^^

Create/destroy development environment:

.. code-block:: bash

    docker-compose up -d    # create and start; omit -d to see log output
    docker-compose down     # docker-compose kill && docker-compose rm -af

Start/stop development environment:

.. code-block:: bash

    docker-compose start    # resume after 'stop'
    docker-compose stop     # stop containers, but keep them intact

Other useful commands:

.. code-block:: bash

    docker-compose ps       # list running containers
    docker-compose logs -f  # view (and follow) container logs

See the `docker-compose CLI reference`_ for other commands.

.. _docker-compose CLI reference: https://docs.docker.com/compose/reference/overview/

Docker Run Commands
^^^^^^^^^^^^^^^^^^^

Development tools supported out-of-the-box: (see `docker-compose.override.yml`_)


None yet. Sorry.

Source `.envrc`_ to activate natural aliases for those commands:

.. code-block:: bash

    . .envrc  # or `source .envrc` in bash

.. note::

    **Optional but recommended:**

    Install and configure `direnv`_ to make this automatic for all projects
    you work on.  See `.envrc`_ for setup instructions.

Alternatively, you can run those commands the classic way, i.e.

.. code-block:: bash

    docker-compose run <toolname>

.. _docker-compose.override.yml: docker-compose.override.yml
.. _direnv: https://direnv.net/
.. _.envrc: .envrc
