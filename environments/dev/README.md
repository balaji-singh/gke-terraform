## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0 |
| <a name="requirement_google"></a> [google](#requirement\_google) | >= 4.0 |
| <a name="requirement_google-beta"></a> [google-beta](#requirement\_google-beta) | >= 4.0 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_gke"></a> [gke](#module\_gke) | ../../modules/gke | n/a |

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_cluster_name"></a> [cluster\_name](#input\_cluster\_name) | The name of the GKE cluster | `string` | `"dev-gke-cluster"` | no |
| <a name="input_cluster_secondary_range_name"></a> [cluster\_secondary\_range\_name](#input\_cluster\_secondary\_range\_name) | The name of the secondary range for pods | `string` | `"pods-range"` | no |
| <a name="input_disk_size_gb"></a> [disk\_size\_gb](#input\_disk\_size\_gb) | The disk size for the nodes | `number` | `100` | no |
| <a name="input_disk_type"></a> [disk\_type](#input\_disk\_type) | The disk type for the nodes | `string` | `"pd-standard"` | no |
| <a name="input_machine_type"></a> [machine\_type](#input\_machine\_type) | The machine type for the nodes | `string` | `"e2-standard-2"` | no |
| <a name="input_maintenance_end_time"></a> [maintenance\_end\_time](#input\_maintenance\_end\_time) | The end time for the maintenance window | `string` | `"2026-01-01T00:00:00Z"` | no |
| <a name="input_maintenance_recurrence"></a> [maintenance\_recurrence](#input\_maintenance\_recurrence) | The recurrence for the maintenance window | `string` | `"FREQ=WEEKLY;BYDAY=SA,SU"` | no |
| <a name="input_maintenance_start_time"></a> [maintenance\_start\_time](#input\_maintenance\_start\_time) | The start time for the maintenance window | `string` | `"2025-01-01T00:00:00Z"` | no |
| <a name="input_master_authorized_networks"></a> [master\_authorized\_networks](#input\_master\_authorized\_networks) | The authorized networks for the master | `list(map(string))` | <pre>[<br/>  {<br/>    "cidr_block": "0.0.0.0/0",<br/>    "display_name": "all"<br/>  }<br/>]</pre> | no |
| <a name="input_master_ipv4_cidr_block"></a> [master\_ipv4\_cidr\_block](#input\_master\_ipv4\_cidr\_block) | The CIDR block for the master | `string` | `"10.0.0.0/28"` | no |
| <a name="input_network"></a> [network](#input\_network) | The name of the VPC network | `string` | `"dev-network"` | no |
| <a name="input_node_count"></a> [node\_count](#input\_node\_count) | The number of nodes in the node pool | `number` | `3` | no |
| <a name="input_node_labels"></a> [node\_labels](#input\_node\_labels) | The labels for the nodes | `map(string)` | <pre>{<br/>  "env": "dev",<br/>  "team": "devops"<br/>}</pre> | no |
| <a name="input_node_metadata"></a> [node\_metadata](#input\_node\_metadata) | The metadata for the nodes | `map(string)` | <pre>{<br/>  "disable-legacy-endpoints": "true"<br/>}</pre> | no |
| <a name="input_node_tags"></a> [node\_tags](#input\_node\_tags) | The tags for the nodes | `list(string)` | <pre>[<br/>  "gke-node",<br/>  "production"<br/>]</pre> | no |
| <a name="input_project_id"></a> [project\_id](#input\_project\_id) | The ID of the GCP project | `string` | `""` | no |
| <a name="input_region"></a> [region](#input\_region) | The region where resources will be deployed | `string` | `"us-central1"` | no |
| <a name="input_services_secondary_range_name"></a> [services\_secondary\_range\_name](#input\_services\_secondary\_range\_name) | The name of the secondary range for services | `string` | `"services-range"` | no |
| <a name="input_subnetwork"></a> [subnetwork](#input\_subnetwork) | The name of the subnetwork | `string` | `"dev-subnetwork"` | no |

## Outputs

No outputs.
