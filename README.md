# Switchport Provisioning API

## Overview

A simple switchport provisioning API


## Components

This project uses the following technologies

* [Swagger](https://swagger.io/) - Swagger is the world’s largest framework of API developer tools for the OpenAPI
  Specification(OAS), enabling development across the entire API lifecycle, from design and documentation,
  to test and deployment.
* [Connexion](http://connexion.readthedocs.io/en/latest/) - Connexion is a framework on top of
  Flask that automagically handles HTTP requests based on OpenAPI 2.0 Specification
  (formerly known as Swagger Spec)
* [MongoDB](https://www.mongodb.com/) - MongoDB 3.4 is the latest release of the leading database
  for modern applications, a culmination of native database features and enhancements that will
  allow you to easily evolve your solutions to address emerging challenges and use cases.
* [nginx](https://nginx.org/en/) - reverse proxy server, also used for ssl termination.
* [Docker](https://www.docker.com/) - ties a nice pretty bow around the project


## Requirements
Python 3.5.2+

## Docker Usage

Docker is the recommended  way to get started using this project.

To run the server, please execute the following from the root directory:

```
docker-compose up -d
```

and open your browser to here:

```
https://localhost/
```

Your Swagger definition lives here:

```
https://localhost/api/swagger.json
```

**NOTE:** in the docker version, we've included an SSL cert for convenience, however,
some REST clients do not like these self signed certificates at all, while others may allow
you to disable cert verification (python requests w/ verify=False)

If your client doesn't allow this, or you just dont want to mess with it you have two options

1. Install a valid certificate (preferred)
2. Use http



## Development / Testing
To launch the integration tests, use tox:
```
sudo pip install tox
tox
```
