# Provenance Framework

## Description
A framework for caputuring and querying provenance data.

### Architecture Diagram
![](https://github.com/Prov-Framework/.github/blob/3c3d860ff81864d2492d64a55c271194f0b03076/prov_framework_architecture.png)

### Why PROV-O?
Naming things is one of the two hard problems in computer science. Regardless of technology, the provenance ontology (https://www.w3.org/TR/prov-o/) provides a useful set of terms and diagrams to facilitate communication and data structure. Using an existing and already agreed upon set of terms avoids re-hashing time consuming discussions that have already taken place in the W3C. 

### Why GQL?
Graph Query Language (GQL) has been formalized as the second data base language after SQL to become an ISO standard (https://www.iso.org/standard/76120.html) in 2024. Major players in the graph and cloud space are making moves to embrace the standard, to include Neo4j, Amazon, Microsoft, and Google. This is an indication of where industry is going, which will hopefully future proof this project. Many graph query languages existed before GQL, such as openCypher, Gremlin, SPARQL, AQL, PGQL, and GSQL. For this project, embracing a single standard means not having to support multiple languages, which means less long term maintenance effort to keep libraries up to date.

### Why not RDF and SPARQL?
Rule based reasoning and globally unique identifiers are not needed for this project. PROV-O is the only ontology being used, so prefixing class and predicate names to differentiate from terms in other ontologies is not required. Data processing speed is important. SPARQL endpoints typically support http REST POST calls, where as most GQL endpoints support the bolt protocol. The bolt protocol transfers data as binary and is stateful, where-as REST calls transfer plain text and are stateless. Binary is more compact, thus more effecient than transmitting plain text. Stateful connections keep the connection open for many back and forth communications, avoiding the overhead of establishing a connection and authenticating for every call to the database. RDF4J does support the application/x-binary-rdf type, but not all semantic graph knowledge bases support binary. Lastly, popularity is important if you find yourself in positions where larger corporate forces control database vendor selection. When looking at indicators like docker hub downloads, property graphs have much higher adoption rates than semantic graphs.       