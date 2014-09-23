Dockerized Islandora
========================

Not working yet! SCRIPT needs some cleaning and parameterization too

A [dockerized](http://docker.io) development instance [Islandora](http://islandora.ca), an open-source software framework designed to help institutions and organizations and their audiences collaboratively manage, and discover digital assets using a best-practices framework. Built on a base of [Drupal](http://drupal.org/), [Fedora Commons](http://www.fedora-commons.org/), and [Solr](http://lucene.apache.org/solr/), Islandora releases solution packs which empower users to work with data types (such as image, video, and pdf) and knowledge domains (such as Chemistry and the Digital Humanities). Solution packs also often provide integration with additional viewers, editors, and data processing applications.

Installation
------------

1. Install [Docker](http://www.docker.io/gettingstarted/)
1. Clone this repository
1. Change into the source directory: `cd docker-islandora`
1. Build the container: `docker build -rm --tag=islandora .`
1. Run ScholarSphere: `docker run -t -i -p 80:80 -p 8080:8080 islandora /bin/bash`
1. Browse to http://localhost:<THE_PORT>/
1. CTRL+P and CTRL+Q to exit the container shell
1. View open ports via `docker ps -a`
1. To get a back the docker container: `docker attach [CONTAINER ID]`
1. To stop an instance: `docker stop [CONTAINER ID]`
1. To stop all images: `docker ps -a | grep '<none>' | awk '{print $1}' | xargs docker rm`
1. To remove all the images: `docker images | grep "<none>" | awk '{print $3}' | xargs docker rmi`

