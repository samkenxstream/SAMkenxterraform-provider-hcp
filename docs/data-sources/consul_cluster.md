---
page_title: "hcp_consul_cluster Data Source - terraform-provider-hcp"
subcategory: ""
description: |-
  The cluster data source provides information about an existing HCP Consul cluster
---

# Data Source `hcp_consul_cluster`

The cluster data source provides information about an existing HCP Consul cluster



## Schema

### Required

- **cluster_id** (String) The ID of the HCP Consul cluster.

### Optional

- **id** (String) The ID of this resource.
- **timeouts** (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

### Read-only

- **cloud_provider** (String) The provider where the HCP Consul cluster is located. Only 'aws' is available at this time.
- **connect_enabled** (Boolean) Denotes the Consul connect feature should be enabled for this cluster.  Default to true.
- **consul_automatic_upgrades** (Boolean) Denotes that automatic Consul upgrades are enabled.
- **consul_ca_file** (String) The cluster CA file encoded as a Base64 string.
- **consul_config_file** (String) The cluster config encoded as a Base64 string.
- **consul_private_endpoint_url** (String) The private URL for the Consul UI.
- **consul_public_endpoint_url** (String) The public URL for the Consul UI. This will be empty if `public_endpoint` is `false`.
- **consul_snapshot_interval** (String) The Consul snapshot interval.
- **consul_snapshot_retention** (String) The retention policy for Consul snapshots.
- **consul_version** (String) The Consul version of the cluster.
- **datacenter** (String) The Consul data center name of the cluster. If not specified, it is defaulted to the value of `cluster_id`.
- **hvn_id** (String) The ID of the HVN this HCP Consul cluster is associated to.
- **num_servers** (Number) The the number of Consul server nodes in the cluster.
- **organization_id** (String) The ID of the organization the project for this HCP Consul cluster is located.
- **project_id** (String) The ID of the project this HCP Consul cluster is located.
- **public_endpoint** (Boolean) Denotes that the cluster has a public endpoint for the Consul UI. Defaults to false.
- **region** (String) The region where the HCP Consul cluster is located.
- **tier** (String) The feature tier that the HCP Consul cluster will be provisioned as.  Only 'dev' and 'standard' are available at this time.

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- **default** (String)

