# 03 - Envoy Proxy and Sovereign Management Server

**Tags:** #envoy #proxy #load-balancing #fastapi #open-source

## Shifting from Enterprise to Cloud-Native
To replace expensive enterprise load balancers, the architectural decision was made to adopt **Envoy Proxy**, an open-source, cloud-native edge and service proxy.

## The Envoy Control Plane (Sovereign)
Envoy allows dynamic configuration reloads at runtime via an API. To manage this, a management server (Envoy Control Plane) was built.

- **Open Source:** This project was open-sourced on Bitbucket under the name **Sovereign**.
- **Architecture:** Built as a FastAPI application.
- **Mechanism:**
  - The app ingests templates (for Envoy resources like clusters, routes, and listeners) and dynamic context.
  - Context is pulled from various sources, including the Open Service Broker's database and S3 buckets.
  - As developers provision new services via the broker, Sovereign updates its context, renders new Envoy configuration templates, and pushes these dynamic updates over the wire to the running Envoy proxies.
