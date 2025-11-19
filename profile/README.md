# Provenance Framework

## Description
A framework for caputuring and querying provenance data that is cloud and database vendor agnostic,  supporting both semantic and property graphs.

### Architecture Diagram
![](https://github.com/Prov-Framework/.github/blob/f6379d1afb0a8a987141ef12064f2e256f455a92/prov_framework_architecture.png)

### Why PROV-O?
Regardless of technology, the provenance ontology (https://www.w3.org/TR/prov-o/) provides a useful set of terms and diagrams to facilitate communication and data structure. 

### Why BFO?
Aligning with BFO can provide benefits ranging from interoperability to political goodwill. More information can be found in the github repo (https://github.com/BFO-Mappings/PROV-to-BFO?tab=readme-ov-file).

### Why Support Both Property and Semantic Graphs?
Often times forces out of our control dictate database and or cloud vendors. This project aims to jump start a team's data provenance journey by providing a provenance implementation in each of the major graph languages, SPARQL, Gremlin, and OpenCypher. Choose the docker images you need or fork the repos for a custom solution.

### Why Use an Agent/LLM based UI?
Engineers already have plently of tools to query and visualize graph databases, there is no reason to create another. End users typically won't know graph languages, so instead they can use any spoken or written lanugages that large language models support to query the graph. UIs are typically very custom to a customers needs, so this can serve as a starting point or easy way to provide a demo when pitching work. 

### Why Give the Agent/LLM DB Access Instead of API Access?
By allowing the agent to query using a graph language instead of having it interact with a predefined REST or GraphQL API, the agent will be able to answer a larger variety of questions. The agent will be provided the provenance ontology, which will help it build more successful queries. The MCP servers will enforce any needed constraints to include verifying queries are read only and have reasonable limits.