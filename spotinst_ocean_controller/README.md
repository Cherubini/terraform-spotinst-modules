# spotinst_ocean_controller

This module will install the [Spotinst Kubernetes Controller][controller-api-url] for use when importing and managing clusters using Elastigroups with Spotinst Ocean. More information can be found in the offical [Spotinst Kubernetes Documentation][spotinst-k8s-api-url].

This module manages the following resources:
* kubernetes_config_map
* kubernetes_service_account
* kubernetes_cluster_role
* kubernetes_cluster_role_binding
* kubernetes_deployment

## Variables
* spotinst_account
* spotinst_token
* spotinst_cluster_identifier
* base_url
* proxy_url
* enable_csr_approval
* disable_auto_update

## Example
Fill in the following arguments in `example.tf`:
```
module "spotinst_ocean_controller" {
  source = "github.com/spotinst/terraform-spotinst-modules//spotinst_ocean_controller"

  spotinst_account            = ""
  spotinst_token              = ""
  spotinst_cluster_identifier = ""
}
```

From within `./example`, run the following commands:
```
terraform get
terraform init
terraform apply
```

You will see `Apply complete!` if your plan is applied successfully.


[controller-api-url]: https://api.spotinst.com/container-management/kubernetes/kubernetes-tutorials/spotinst-kubernetes-controller/
[spotinst-k8s-api-url]: https://api.spotinst.com/container-management/kubernetes/
