# Provenance Framework

## Description
A framework for caputuring and querying provenance data using a variety of graph technologies.

## Architecture Diagram
![](https://github.com/Prov-Framework/.github/blob/3c3d860ff81864d2492d64a55c271194f0b03076/prov_framework_architecture.png)

## Scope (Intended Use Case)
This is a starting point not a finished product. This is a deliberate choice.

Close source products often lead to problems when an organization has existing cloud or database licenses, internal authentication services, or hardened docker images that they require teams to utilize. This project prioritizes flexiblity, stopping short of those final productizing decisions because integration points to existing organizational systems and processes are where the most customization is needed. 

### Steps to start using the framework
1) Clone the repo.
2) Remove the graph libraries you don't need. If you are using Neo4j, no need to keep Apache Tinkerpop or Jena. More software libraries means more security vulnerabilities and code maintenance. 
3) Configure authentication specific to the database you are using. For example, connecting to AWS Neptune might require AWS IAM configuration, or your organization may have custom internal authentication services.
4) Choose and build a docker container that meets your needs. Different organizations have different security requirements, and may have internally hardened images they prefer to use.

## Q&A
### Why PROV-O?
Naming things is one of the two hard problems in computer science. The provenance ontology (https://www.w3.org/TR/prov-o/) provides a useful set of terms and structure. 

### Why Java?
Java has the best support for libraries in the graph community. Neo4j (https://github.com/neo4j/neo4j), Apache Tinkerpop (https://github.com/apache/tinkerpop), Apache Jena (https://github.com/apache/jena), JanusGraph (https://github.com/JanusGraph/janusgraph), and BlazeGraph (https://github.com/blazegraph/database), which influenced AWS Neptune, are all built mostly in Java. That means Java is the first language that gets library and driver support in many cases, it is often the best maintained and optimized language library, and likely has the best community support. Additionally, this project is meant to be cloned and modified, so the language needs to be relatively popular. Java provides a good balance of popularity and performance.

### What is BFO Inside?
Basic Formal Ontology (https://github.com/bfo-ontology) is an upper level ontology that some organization choose to extend from when creating domain specific ontologies. Work has already been done to map PROV to BFO (https://github.com/BFO-Mappings/PROV-to-BFO). This project simply bring attention to the BFO PROV-O mapping in the architecture diagram as a possible benefit to those opting for a semantic graph in an organization that already leverages BFO or is looking to start. 