[<img src="http://sling.apache.org/res/logos/sling.png"/>](http://sling.apache.org)

 [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![starter](https://sling.apache.org/badges/group-starter.svg)](https://github.com/apache/sling-aggregator/blob/master/docs/groups/starter.md)

About Sling
===

[Apache Sling](https://sling.apache.org) is a framework for RESTful web-applications based on an extensible content tree.

In a nutshell, Sling maps HTTP request URLs to content resources based on the request's path, extension and selectors. Using convention over configuration, requests are processed by scripts and servlets, dynamically selected based on the current resource. This fosters meaningful URLs and resource driven request processing, while the modular nature of Sling allows for specialized server instances that include only what is needed.

Sling serves as basis for a variety of applications ranging from blogging engines all the way to enterprise content management systems.

These docker images are convenience binaries for quickly getting started with Apache Sling. To learn more about Sling, see our [getting started](https://sling.apache.org/documentation/getting-started.html) and the [Sling website](https://sling.apache.org/) in general.


Supported tags
===

* `11, latest` - Apache Sling Starter 11 - ( [Dockerfile](https://github.com/apache/sling-org-apache-sling-starter-docker/blob/11/Dockerfile) )
* `10` - Apache Sling Starter 10 - ( [Dockerfile](https://github.com/apache/sling-org-apache-sling-starter-docker/blob/10/Dockerfile) )
* `9`- Apache Sling Launchpad 9 - ( [Dockerfile](https://github.com/apache/sling-org-apache-sling-starter-docker/blob/9/Dockerfile) )

Launching instructions
===

In order to run a container with our image, execute:

    docker run --name my-sling-container apache/sling

The image exposes port `8080` and mounts a volume at `/opt/sling/sling`. You can control the JVM parameters by setting the `JAVA_OPTS` environment variable and the options passed to Sling by setting the `SLING_OPTS` environment variable.

A more complex example would be

    docker run -d -p 8080:8080 -v /srv/docker/sling:/opt/sling/sling  -e JVM_OPTS=-Xm1g --name my-sling-container apache/sling
 

Support
===

For questions, please use [the Apache Sling user's mailing list](http://sling.apache.org/project-information.html#mailing-lists).

For bug reports, please use the [Apache Sling issue tracker](https://issues.apache.org/jira/browse/SLING).`

For Sling developers: how to deploy this image to DockerHub
====
See the [instructions on the Sling Wiki](https://cwiki.apache.org/confluence/display/SLING/Releasing+a+new+version+of+the+Sling+Starter#ReleasinganewversionoftheSlingStarter-DeploythedockerimageonDockerHub)
