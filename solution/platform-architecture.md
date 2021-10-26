# Platform Architecture

Following are the major components of the System:

1. Data Sourcing
2. Data Storage
3. User Facing Portals
4. Monitoring and Analysis

### User Facing Portals

This is the group of all systems which caters to userflows which are enduser facing. Following are some key identified systems:

* Data Catalog
* Stories and Blogs
* Community Forum
* Information Portal
* Data Management Platform
* System Moderation Control Panel

### Data Sourcing

The system would support sourcing of data from three different processes

1. Direct bulk upload by system maintainer
2. Data collected from primary data collection
3. Data periodically updated via automated processes

### Data Storage

The system contains various data storage capabilities at different levels of the platform. Each component in the system would have a temporary storage to enable faster data access and processing.

All datasets are stored pre and post processing to enable higher resilience against data loss. The central datastore manages the processing, indexing, caching and archival of data.

A knowledge graph of all the base truths in the system is maintained to enable information mapping against mutiple data sources.

### Monitoring and Analysis

The system would be equipped with central monitoring system to monitor workflows between all the components of the system. This system would also allow manual interventions and policy enforcement.

The processed data is also available to allow analysis of all the datasets present in the system.
