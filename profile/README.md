# Provenance Framework

## Description
A framework for caputuring and querying provenance data that is cloud and database vendor agnostic,  supporting both semantic and property graphs.

### Why use this?
Often times forces out of our control dictate database vendors. This project aims to make it easy to switch between databases by providing a translation layer between PROV-O Java objects and the major graph languages, SPARQL, Gremlin, and OpenCypher.

### How is this intended to be used?
The goal of this project is to provide a jumping off point for developers to choose which database language they need, include the corresponding database driver jar, and build their own docker images. While forking and customizing is encouraged, customizing around a single graph language or database driver will begin to deviate from the original goal of this project (being able to switch).

### Architecture Diagram
![](https://github.com/Prov-Framework/.github/blob/9464f6fba5fc9cbcb4350c079e9839d11c4b7775/prov_framework_architecture.png)


