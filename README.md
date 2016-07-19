HOW TO:
=======

Clone me:

    git clone git://github.com/aleksandra-tarkowska/dev omerodev
    cd omerodev
or

    git clone git://github.com/aleksandra-tarkowska/dev metadata52
    cd metadata52


Clone repository:
-----------------

- develop:

        git clone git://github.com/openmicroscopy/bioformats src/bf.git
        git clone git://github.com/openmicroscopy/openmicroscopy src/omero.git

- metadata:

        git clone -b metadata git://github.com/openmicroscopy/bioformats src/bf.git
        git clone -b metadata52 git://github.com/openmicroscopy/openmicroscopy src/omero.git


Build:
------

- BF:

        ./bf build|up|rm

- OMERO:

        BUILD_CMD=build-dev ./omero build|up|rm

Run:
----

Review .env file

- SERVER:

        ./server build|up -d|logs -f|stop|rm

- WEB:

        ./web build|up -d|logs -f|stop|rm


Limitations:
------------

PG container permission denied on mac. Use host.

    docker run --name mypostgres -p 5432:5432 -d -v ./pgdata:/var/lib/postgresql/data postgres

create omero user

    createuser  -h pg95 -U postgres omero --interactive
