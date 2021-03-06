# StreamFlow&trade;

## Overview

StreamFlow&trade; is a stream processing tool designed to help build and monitor processing 
workflows.  The ultimate goal of StreamFlow is to make working with stream processing frameworks 
such as Apache Storm easier, faster, and with "enterprise" like management functionality.  
StreamFlow also provides a mechanism for non-developers such as data scientists, analysts, or 
operational users to rapidly build scalable data flows and analytics.

StreamFlow provides the following capabilites: 

1. A **responsive web interface** for building and monitoring Storm topologies.
2. An interactive **drag and drop topology builder** for authoring new topologies
3. A **dashboard** for monitoring the status and performance of topologies as well as viewing aggregated topology logs.
4. A speciaized **topology engine** which solves some Storm complexities such as ClassLoader isolation and serialization and provides a mechanism for dependency injection.
5. A **modular framework** for publishing and organizing new capabilities in the form of Spouts and Bolts.


## How it works

The following is a simple depiction of the StreamFlow stack. The web interface is built using open 
source web frameworks and is backed by a series of reusable web services. StreamFlow is capable of 
authoring and managing topologies dynamically using a series of reusable Frameworks.  These 
Frameworks are simply JAR files comprised of standard Storm Spouts and Bolts with a metadata 
configuration file which exposes the frameworks.  StreamFlow utilizes a custom topology driver 
which is used to bootstrap and execute a topology along with StreamFlow specific configuration logic.


## Concepts

The following is a description of some core StreamFlow concepts and terminology.

##### Component
A component is either Storm Spout or a Storm Bolt

##### Framework
A grouping of related *Components* and their associated metadata. Ideally elements of a framework 
should all be compatible when wired together on a topology as they share the same protocol. 
Frameworks might be organized around a set of technologies or domains. An analogy would be a 
Java Library or Objective C Framework. Topologies have frameworks as dependencies.

##### Resource
A resource is an object used by spouts/bolts in order to externalize common state. For example, an 
object which represents a technical asset in the environment/cluster such as a database or Kafka 
queue. Alternatively, a resource might provide an uploaded file or container of global state. 
Resources should be used to encapsulate functionality outside of a bolt/spout if that information 
is used in several places in a topology or within multiple topologies. Resources also provide a 
useful mechanism for injecting parameters, connections, or state into a bolt/spout making the spout 
or bolt simpler, easier to write, and more testable.

##### Serialization

##### Topology


## Find out more

The StreamFlow [Wiki](https://github.com/lmco/streamflow/wiki) is the best place to go to learn more 
about the StreamFlow architecture and how to install and configure a StreamFlow server in your 
environment.

[https://github.com/lmco/streamflow/wiki](https://github.com/lmco/streamflow/wiki);

Here are some quick links to help get you started with StreamFlow:

* [Getting Started with StreamFlow](https://github.com/lmco/streamflow/wiki/Getting-Started)
* [Installing and Running StreamFlow](https://github.com/lmco/streamflow/wiki/Getting-Started#startup)
* [Configuring StreamFlow](https://github.com/lmco/streamflow/wiki/Configuration)
* [How Does StreamFlow Work?](https://github.com/lmco/streamflow/wiki/How-It-Works)
* [Developing StreamFlow Frameworks](https://github.com/lmco/streamflow/wiki/Developing-Frameworks)


## Questions or need help?
Coming soon...


## License

StreamFlow is copyright 2014 Lockheed Martin Corporation. 

Licensed under the **[Apache License, Version 2.0] [license]** (the "License");
you may not use this software except in compliance with the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

This product incorporates open source software components covered by the terms 
of third party license agreements contained are contained in the /Licenses 
folder of this project.

## Documentation Version

*Last Updated: 11/16/2014*


[license]: http://www.apache.org/licenses/LICENSE-2.0
