# The Infinispan project #

Infinispan is an open source (under the [Apache License, v2.0](http://www.apache.org/licenses/LICENSE-2.0.html "The Apache License, v2.0")) data grid platform.  For more information on Infinispan,
including HOWTOs, getting started guides, build instructions and downloading binaries, visit the project's website on
[http://www.infinispan.org](http://www.infinispan.org "The Infinispan project page")

# Fork
We (Sector Labs) forked this repository to set up a pipeline that builds a Docker image with the PostgreSQL JDBC driver built-in. It also allows us to quickly apply patches and release the patched version across our servers. This fork contains no other changes at the time of writing.

The build pipeline is triggered when a Git tag is added. The pipeline will build a new Docker image with the tag and push it to our AWS ECR registry. Pull requests trigger a build, but does not push the Docker image.

The format of the tags should be `v[original version]-sl.[fork version]`. As an example, let's say we fork `v13.0.0`. The first tag after forking should be: `v13.0.0-sl.1`. The next patch would get `v13.0.0-sl.2`.

## Version

![Version](https://maven-badges.herokuapp.com/maven-central/org.infinispan/infinispan-core/badge.svg "Version")

## Contributing

For contributing guidelines please refer to this [document](CONTRIBUTING.md). All contributions are subject to [Developer Certificate of Origin (DCO)](https://developercertificate.org/).

*The Infinispan project team*
