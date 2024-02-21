# ec2_worker_demo
<!-- BEGIN_TF_DOCS -->
## Requirements

The following requirements are needed by this module:

- <a name="requirement_aws"></a> [aws](#requirement\_aws) (~> 4.57.0)

## Providers

No providers.

## Modules

The following Modules are called:

### <a name="module_my_workerpool"></a> [my\_workerpool](#module\_my\_workerpool)

Source: github.com/spacelift-io/terraform-aws-spacelift-workerpool-on-ec2

Version: v2.3.1

## Resources

No resources.

## Required Inputs

The following input variables are required:

### <a name="input_spacelift_api_key_endpoint"></a> [spacelift\_api\_key\_endpoint](#input\_spacelift\_api\_key\_endpoint)

Description: Full URL of the Spacelift API endpoint to use, eg. https://demo.app.spacelift.io

Type: `string`

### <a name="input_spacelift_api_key_id"></a> [spacelift\_api\_key\_id](#input\_spacelift\_api\_key\_id)

Description: ID of the Spacelift API key to use

Type: `string`

### <a name="input_spacelift_api_key_secret"></a> [spacelift\_api\_key\_secret](#input\_spacelift\_api\_key\_secret)

Description: Secret corresponding to the Spacelift API key to use

Type: `string`

### <a name="input_worker_pool_config"></a> [worker\_pool\_config](#input\_worker\_pool\_config)

Description: Configuration for the worker pool

Type: `string`

### <a name="input_worker_pool_id"></a> [worker\_pool\_id](#input\_worker\_pool\_id)

Description: ID of the worker pool

Type: `string`

### <a name="input_worker_pool_private_key"></a> [worker\_pool\_private\_key](#input\_worker\_pool\_private\_key)

Description: Private key for the worker pool

Type: `string`

### <a name="input_worker_pool_security_groups"></a> [worker\_pool\_security\_groups](#input\_worker\_pool\_security\_groups)

Description: The security groups to be used for the worker pool

Type: `list(string)`

### <a name="input_worker_pool_subnets"></a> [worker\_pool\_subnets](#input\_worker\_pool\_subnets)

Description: The subnets to be used for the worker pool

Type: `list(string)`

## Optional Inputs

No optional inputs.

## Outputs

No outputs.
<!-- END_TF_DOCS -->