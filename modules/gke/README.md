Copyright 2024 Google LLC

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.

## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_google"></a> [google](#provider\_google) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [google_container_cluster.primary](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/container_cluster) | resource |
| [google_container_node_pool.primary_nodes](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/container_node_pool) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_cluster_name"></a> [cluster\_name](#input\_cluster\_name) | The name of the cluster | `string` | n/a | yes |
| <a name="input_cluster_secondary_range_name"></a> [cluster\_secondary\_range\_name](#input\_cluster\_secondary\_range\_name) | The name of the secondary range to use for pods | `string` | n/a | yes |
| <a name="input_deletion_protection"></a> [deletion\_protection](#input\_deletion\_protection) | Whether deletion protection is enabled for the cluster | `bool` | `false` | no |
| <a name="input_disk_size_gb"></a> [disk\_size\_gb](#input\_disk\_size\_gb) | Size of the disk attached to each node | `number` | `100` | no |
| <a name="input_disk_type"></a> [disk\_type](#input\_disk\_type) | Type of the disk attached to each node | `string` | `"pd-standard"` | no |
| <a name="input_enable_private_endpoint"></a> [enable\_private\_endpoint](#input\_enable\_private\_endpoint) | Enable private endpoint | `bool` | `false` | no |
| <a name="input_enable_private_nodes"></a> [enable\_private\_nodes](#input\_enable\_private\_nodes) | Enable private nodes | `bool` | `true` | no |
| <a name="input_location"></a> [location](#input\_location) | The location (region or zone) of the cluster | `string` | n/a | yes |
| <a name="input_machine_type"></a> [machine\_type](#input\_machine\_type) | The name of a Google Compute Engine machine type | `string` | `"e2-medium"` | no |
| <a name="input_maintenance_end_time"></a> [maintenance\_end\_time](#input\_maintenance\_end\_time) | Time window specified for daily or recurring maintenance operations end time | `string` | `"09:00"` | no |
| <a name="input_maintenance_recurrence"></a> [maintenance\_recurrence](#input\_maintenance\_recurrence) | Frequency of the recurring maintenance window | `string` | `"FREQ=WEEKLY;BYDAY=SA,SU"` | no |
| <a name="input_maintenance_start_time"></a> [maintenance\_start\_time](#input\_maintenance\_start\_time) | Time window specified for daily or recurring maintenance operations start time | `string` | `"05:00"` | no |
| <a name="input_master_authorized_networks"></a> [master\_authorized\_networks](#input\_master\_authorized\_networks) | List of master authorized networks | <pre>list(object({<br/>    cidr_block   = string<br/>    display_name = string<br/>  }))</pre> | `[]` | no |
| <a name="input_master_ipv4_cidr_block"></a> [master\_ipv4\_cidr\_block](#input\_master\_ipv4\_cidr\_block) | The IP range in CIDR notation to use for the hosted master network | `string` | `"172.16.0.0/28"` | no |
| <a name="input_max_surge"></a> [max\_surge](#input\_max\_surge) | The maximum number of nodes that can be created beyond the desired number of nodes during an upgrade | `number` | `1` | no |
| <a name="input_max_unavailable"></a> [max\_unavailable](#input\_max\_unavailable) | The maximum number of nodes that can be unavailable during an upgrade | `number` | `0` | no |
| <a name="input_network"></a> [network](#input\_network) | The VPC network to host the cluster in | `string` | n/a | yes |
| <a name="input_node_count"></a> [node\_count](#input\_node\_count) | Number of nodes in the node pool | `number` | `3` | no |
| <a name="input_node_labels"></a> [node\_labels](#input\_node\_labels) | The Kubernetes labels (key/value pairs) to be applied to each node | `map(string)` | `{}` | no |
| <a name="input_node_tags"></a> [node\_tags](#input\_node\_tags) | The network tags to be applied to each node | `list(string)` | `[]` | no |
| <a name="input_project_id"></a> [project\_id](#input\_project\_id) | The project ID to host the cluster in | `string` | n/a | yes |
| <a name="input_remove_default_node_pool"></a> [remove\_default\_node\_pool](#input\_remove\_default\_node\_pool) | Whether to remove the default node pool | `bool` | `true` | no |
| <a name="input_services_secondary_range_name"></a> [services\_secondary\_range\_name](#input\_services\_secondary\_range\_name) | The name of the secondary range to use for services | `string` | n/a | yes |
| <a name="input_subnetwork"></a> [subnetwork](#input\_subnetwork) | The subnetwork to host the cluster in | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_cluster_ca_certificate"></a> [cluster\_ca\_certificate](#output\_cluster\_ca\_certificate) | The public certificate that is the root of trust for the cluster |
| <a name="output_cluster_endpoint"></a> [cluster\_endpoint](#output\_cluster\_endpoint) | The IP address of the cluster master |
| <a name="output_cluster_id"></a> [cluster\_id](#output\_cluster\_id) | The unique identifier of the cluster |
| <a name="output_cluster_name"></a> [cluster\_name](#output\_cluster\_name) | The name of the cluster |
| <a name="output_location"></a> [location](#output\_location) | The location of the cluster |
| <a name="output_node_pools"></a> [node\_pools](#output\_node\_pools) | List of node pools associated with this cluster |
