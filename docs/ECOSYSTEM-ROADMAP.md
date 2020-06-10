# Fresh API ecosystem roadmap

Fresh API is all about friendship with developers. Developers love gRPC, dynamic documentation
and easy to use concepts. So we're trying to start from a bunch of independent projects.

## Protopub
*(Actually we're good with just ORAS for now)*

* Based on ORAS
* A simple tool for pushing and pulling protobuf descriptors to OCI compatible registries
* BC checks based on descriptors previously pushed to the registry
* Compilers and tools integration (protopub build)
* Go package with easy access to FileDescriptors
* Server Reflection implementation

## gRPC discovery gateway

* Dynamic service discovery based on Kubernetes service or other configuration providers
* Single entry point for gRPC clients. gRPC service fully-qualified name as a routing key
* Load balancing and schema updates awareness
* Server Reflection support (without SourceCodeInfo due to lack of this info in proto descriptors)
* Support FileDescriptors from OCI registries
* gRPC web portal with all information gathered either from Server Reflection of OCI registry
* REST API and OpenAPI document for it

## API Gateway

* Much like KrakenD but with Kubernetes CRD configuration
* KrakenD operator?
* OpenAPI documentation based on downstream OpenAPI with applied transformations from KrakenD endpoint configuration

