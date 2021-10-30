---
coverY: 0
---

# 🔩 Platform Architecture

The techology arrchitecture of the platform has been driven by the understanding through the following threads:

* Intention and Objective of the suggested new platform and how it's functionalities have been inspired by the landscape of existing tools.
* Possible journeys various stakeholders might take through the platform and how they will engage with various pieces of the solution.

{% content-ref url="personas-and-journeys.md" %}
[personas-and-journeys.md](personas-and-journeys.md)
{% endcontent-ref %}

* The features of individual pages of the platforms, the challenges they are addressing and the ways a user can manouver through the information.

{% content-ref url="wireframes/" %}
[wireframes](wireframes/)
{% endcontent-ref %}

Based on these inputs, the architecture has four basic components:

* Data Sourcing
* Data Storage
* User Facing Portals
* Monitoring and Analysis

![Architecture](../.gitbook/assets/platform-architecture.png)

> **`Suggested Stack`**

|                             |                                                                                                                  |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Processors and Transformers | [Rust](https://www.rust-lang.org)                                                                                |
| Infrastructure              | [AWS](https://aws.amazon.com)                                                                                    |
| Scripts                     | <p><a href="https://aws.amazon.com/lambda/">AWS Lambda</a></p><p><a href="https://www.python.org">Python</a></p> |

### Components

#### Data Sourcing

![Data Sourcing](../.gitbook/assets/data-source.png)

Based on the requirments of the stakeholders from a new and the possible datasets in scope identified by the University of Strathclyde through their research, the system would support sourcing of data from three different processes:

1. Direct bulk upload of datasets by system maintainers.
2. Data collected on ground through primary data collection methods.
3. Data periodically updated via automated processes through APIs.

#### Data Storage

![Central Data Storage](../.gitbook/assets/central-data-storage.png)

To support the various sources of data, the system contains various data storage capabilities at different levels of the platform.

* Each component in the system would have a temporary storage to enable faster data access and processing.
* All datasets are stored pre and post processing to enable higher resilience against data loss.&#x20;
* The central datastore manages the processing, indexing, caching and archival of data.
* A knowledge graph of all the base truths in the system is maintained to enable information mapping against mutiple data sources.

> **`Suggested Stack`**

| Function                | Technology                                   |
| ----------------------- | -------------------------------------------- |
| Realtime Storage        | [Redis](https://redis.io)                    |
| Relational Database     | [PostgreSQL](https://www.postgresql.org)     |
| Non-Relational Database | [Apache CouchDB](https://couchdb.apache.org) |
| Object Store            | [AWS S3](https://aws.amazon.com/s3/)         |
| Cache                   | [Redis](https://redis.io)                    |

#### User Facing Portals

![User Facing Portal](../.gitbook/assets/user-facing.png)

Catering to the requirements of the key stakeholders, these are some of the components of the user facing portal:

* **Information Portal **: Pre-set of landing pages, visualisations and more catered to the requirements of each of the key stakeholder buckets.
* **Data Catalog** : Repository of the all datasets available on the plaform to various users based on their access rights to explore, visualise, share and more.
* **Data Stories** : Capability to use existing data and visualisations, and stitch naratives around the same which can be published on the platform.
* **Community Portal** : A central portal for variopus stakeholders of the communicy to come together, share relevant information and support each other in build capacity.
* **System Moderation Control Panel** : Management of various system components of the platofrm like analytics, access, usage patterns and more.
* **Data Management Platform** : Access platform available to key data fiduciaries to provide access to relevant datasets based on requirements and eligibility of the users.

#### Monitoring and Analysis

The system would be equipped with central monitoring system to monitor workflows between all the components of the system.&#x20;

* This system would allow manual interventions and policy enforcement for platform use.&#x20;
* The processed data will also be available to analyse all the datasets present in the system.

> **`Suggested Stack`**

| Function         | Technology                                                                                                                                                                                                              |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Dashboard        | <p><a href="https://reactjs.org">React</a><br><a href="https://nextjs.org">Next.js</a><br><a href="https://echarts.apache.org/en/index.html">ECharts</a><br><a href="https://www.typescriptlang.org">Typescript</a></p> |
| Identity Manager | [Keycloak](https://www.keycloak.org)                                                                                                                                                                                    |
| Access Manager   | [Python](https://www.python.org)                                                                                                                                                                                        |
| Analytics        | [Grafana](https://grafana.com)                                                                                                                                                                                          |
| Monitoring       | [Elastic Stack](https://www.elastic.co/what-is/elk-stack)                                                                                                                                                               |
| Administration   | [Strapi](https://strapi.io)                                                                                                                                                                                             |

### Methodology

The key thread across the entire solution architecture is that none the technologies suggested to achieve this solution are proprietory in nature. All the code, tools and technologies produced will be open sourced by default and available under on licenses in public repositories.
