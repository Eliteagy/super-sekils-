# 05 - Edge Migrations and Sidecar Architecture

**Tags:** #migration #envoy #sidecar #rust #architecture

## Migrating the Giants
Once the baseline proxy infrastructure was solid, the next massive effort (spanning a couple of years) was migrating Atlassian's major products—Jira, Confluence, Bitbucket, and Statuspage—behind this new centralized edge platform. The platform team enforced that internal microservices could no longer expose themselves publicly without explicitly configuring via the new infrastructure.

## Solving Concerns at the Edge
By intercepting traffic at the edge proxy layer, common concerns were resolved before reaching thousands of backend services, saving massive amounts of compute and development time.
- **DDoS Protection:** Handled further upstream via CloudFront.
- **Access Logging:** Handled natively within Envoy's Network Filters (e.g., HTTP Connection Manager).

## The Sidecar Model
For more complex logic, a sidecar container model was implemented alongside the Envoy proxy. These sidecars received dynamic configuration locally.
- **Authentication:** Built by the author in **Rust**.
- **Authorization & Rate Limiting:** Contributed and maintained by other specialized internal teams.
