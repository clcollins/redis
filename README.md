#This repository is archived and will no longer receive updates.

Redis
=====

*Community Honey Network Redis service*

| branch | build status |
| ---    | ---          |
| master | [![Master Build Status](https://travis-ci.org/CommunityHoneyNetwork/redis.svg?branch=master)](https://travis-ci.org/CommunityHoneyNetwork/redis) |
| staging | [![Staging Build Status](https://travis-ci.org/CommunityHoneyNetwork/redis.svg?branch=staging)](https://travis-ci.org/CommunityHoneyNetwork/redis) |

Ansible playbook and Dockerfile for setting up a Redis instance, containerized or not, for use with CHN projects.

## Requirements

Containerized usage:

* docker
* docker-compose

Stand-alone:

* ansible

## Building and Running the container

Build:

    docker build -t redis .

Run with:

    docker run -p 6379:6379 \
               --name redis \
	       -v <host_logdir>:/var/log/redis \
	       -v <host_datadir>:/var/lib/redis \
	       -d <image-name>
