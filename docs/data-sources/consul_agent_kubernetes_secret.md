---
page_title: "hcp_consul_agent_kubernetes_secret Data Source - terraform-provider-hcp"
subcategory: ""
description: |-
  The agent config Kubernetes secret data source provides Consul agents running in Kubernetes the configuration needed to connect to the Consul cluster.
---

# Data Source `hcp_consul_agent_kubernetes_secret`

The agent config Kubernetes secret data source provides Consul agents running in Kubernetes the configuration needed to connect to the Consul cluster.

## Example Usage

```terraform
data "hcp_consul_agent_kubernetes_secret" "test" {
  cluster_id = var.cluster_id
}
```

## Schema

### Required

- **cluster_id** (String) The ID of the HCP Consul cluster.

### Optional

- **id** (String) The ID of this resource.
- **timeouts** (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-only

- **secret** (String) The Consul agent configuration in the format of a Kubernetes secret (YAML).

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- **default** (String)

