# Provenance Framework

## Description
A framework for caputuring and querying provenance data.

### Architecture Diagram
![](https://github.com/Prov-Framework/.github/blob/3c3d860ff81864d2492d64a55c271194f0b03076/prov_framework_architecture.png)

### Why PROV-O?
Naming things is one of the two hard problems in computer science. Regardless of technology, the provenance ontology (https://www.w3.org/TR/prov-o/) provides a useful set of terms. 

### Why GQL?
To future proof the project and reduce the maintenance burden of supporting multiple query languages and thier libraries. Graph Query Language (GQL) is the second database query language after SQL to become an ISO standard (https://www.iso.org/standard/76120.html), which makes it a pretty big deal. Major players in the graph and cloud space are making moves to embrace the standard, to include Neo4j (https://neo4j.com/blog/cypher-and-gql/cypher-gql-world/), Amazon (https://aws.amazon.com/blogs/database/gql-the-iso-standard-for-graphs-has-arrived/), Microsoft (https://learn.microsoft.com/en-us/fabric/graph/gql-language-guide), and Google (https://docs.cloud.google.com/spanner/docs/graph/iso-standards).  Prior to GQL, there have been may graph languages to include openCypher, Gremlin, SPARQL, AQL, PGQL, and GSQL. 

### Why Property Graph instead of Semantic Graph?
Rule based reasoning and globally unique identifiers are not needed for this project. PROV-O is the only ontology being used, so prefixing class and predicate names to differentiate from terms in other ontologies is not needed. Additionally, when working with organizations that have existing enterprise licenses with database or cloud vendors, you often have to work with the most popular technologies, even if that was not your first choice. Using widely adopted technologies increases the usefulness of this project.

### Why Java?
Java has the best support for libraries in the graph community. Neo4j (https://github.com/neo4j/neo4j), Apache Tinkerpop (https://github.com/apache/tinkerpop), Apache Jena (https://github.com/apache/jena), JanusGraph (https://github.com/JanusGraph/janusgraph), and BlazeGraph (https://github.com/blazegraph/database), which Amazon hired key developers from to build Neptune, are all built mostly in Java. That means Java is the first language that gets library and driver support in many cases, it is often the best maintained and optimized language library, and likely has the best community support.