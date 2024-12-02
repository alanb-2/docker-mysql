docker-mysql
===

Contains a configuration to spin up a MySQL instance using Docker Compose

# Prerequisites

* docker
* docker-compose
* MySQL client

Note 1: Depending on the OS and installation configuration, it may be necessary to prefix docker commands with `sudo`.

Note 2: All commands are run from the root of this repository.

# Usage

1.  Start the MySQL docker instance.

    ```shell
    docker compose -f docker/docker-compose.yml up
    ```

2.  Open a separate terminal and connect to the MySQL container using the MySQL client.  The password can be found in [docker/docker-compose.yml](./docker/docker-compose.yml).

    ```shell
    mysql -u user -p -h localhost --protocol=tcp --port=3306
    ```

3.  To close the MySQL client enter `\q`.

4.  To terminate the MySQL docker container, use `CTRL+C`.
