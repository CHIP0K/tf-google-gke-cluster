# tf-google-gke-cluster
Terraform module to create GKE cluster with custom node pool

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_google"></a> [google](#requirement\_google) | 4.52.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_google"></a> [google](#provider\_google) | 4.52.0 |
| <a name="provider_local"></a> [local](#provider\_local) | n/a |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_gke_auth"></a> [gke\_auth](#module\_gke\_auth) | terraform-google-modules/kubernetes-engine/google//modules/auth | >= 24.0.0 |

## Resources

| Name | Type |
|------|------|
| [google_container_cluster.this](https://registry.terraform.io/providers/hashicorp/google/4.52.0/docs/resources/container_cluster) | resource |
| [google_container_node_pool.this](https://registry.terraform.io/providers/hashicorp/google/4.52.0/docs/resources/container_node_pool) | resource |
| [local_file.kubeconfig](https://registry.terraform.io/providers/hashicorp/local/latest/docs/resources/file) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_GOOGLE_PROJECT"></a> [GOOGLE\_PROJECT](#input\_GOOGLE\_PROJECT) | GCP project name | `string` | n/a | yes |
| <a name="input_GKE_CLUSTER_NAME"></a> [GKE\_CLUSTER\_NAME](#input\_GKE\_CLUSTER\_NAME) | GKE cluster name | `string` | `"main"` | no |
| <a name="input_GKE_MACHINE_TYPE"></a> [GKE\_MACHINE\_TYPE](#input\_GKE\_MACHINE\_TYPE) | Machine type | `string` | `"g1-small"` | no |
| <a name="input_GKE_NUM_NODES"></a> [GKE\_NUM\_NODES](#input\_GKE\_NUM\_NODES) | GKE nodes number | `number` | `2` | no |
| <a name="input_GKE_POOL_NAME"></a> [GKE\_POOL\_NAME](#input\_GKE\_POOL\_NAME) | GKE pool name | `string` | `"main"` | no |
| <a name="input_GOOGLE_REGION"></a> [GOOGLE\_REGION](#input\_GOOGLE\_REGION) | GCP region to use | `string` | `"us-central1-c"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_kubeconfig"></a> [kubeconfig](#output\_kubeconfig) | The path to the kubeconfig file |
<!-- END_TF_DOCS -->