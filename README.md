# postgres, mysql - docker-compose

## Setup

To persist data between docker sessions, postgres and mysql use external volumes

Create them,

    mkdir -p /srv/docker/postgresql/data
    mkdir -p /srv/docker/mysql

The mappings can be changed in docker-compose.yml

## Usage

Set up the images,

    docker-compose build

Run the images,

    docker-compose up

This will run service on the local interface - mysql on 3306, postgres on 5432, these mappings are found in docker-compose.yml.

If these ports already have services running on them docker-compose _will fail_, so make sure local dbs etc are stopped or change the mapping in docker-compose.yml.




