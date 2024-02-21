# ec2_worker_demo

Example created by https://github.com/Daniellem97

<!-- BEGIN_TF_DOCS -->

## Requirements

The following requirements are needed by this module:

- <a name="requirement_aws"></a> [aws](#requirement_aws) (~> 4.57.0)

## Providers

No providers.

## Modules

The following Modules are called:

### <a name="module_my_workerpool"></a> [my_workerpool](#module_my_workerpool)

Source: github.com/spacelift-io/terraform-aws-spacelift-workerpool-on-ec2

Version: v2.3.1

## Resources

No resources.

## Required Inputs

The following input variables are required:

### <a name="input_spacelift_api_key_endpoint"></a> [spacelift_api_key_endpoint](#input_spacelift_api_key_endpoint)

Description: Full URL of the Spacelift API endpoint to use, eg. https://demo.app.spacelift.io

Type: `string`

### <a name="input_spacelift_api_key_id"></a> [spacelift_api_key_id](#input_spacelift_api_key_id)

Description: ID of the Spacelift API key to use

Type: `string`

### <a name="input_spacelift_api_key_secret"></a> [spacelift_api_key_secret](#input_spacelift_api_key_secret)

Description: Secret corresponding to the Spacelift API key to use

Type: `string`

### <a name="input_worker_pool_config"></a> [worker_pool_config](#input_worker_pool_config)

Description: Configuration for the worker pool

Type: `string`

### <a name="input_worker_pool_id"></a> [worker_pool_id](#input_worker_pool_id)

Description: ID of the worker pool

Type: `string`

### <a name="input_worker_pool_private_key"></a> [worker_pool_private_key](#input_worker_pool_private_key)

Description: Private key for the worker pool

Type: `string`

### <a name="input_worker_pool_security_groups"></a> [worker_pool_security_groups](#input_worker_pool_security_groups)

Description: The security groups to be used for the worker pool

Type: `list(string)`

### <a name="input_worker_pool_subnets"></a> [worker_pool_subnets](#input_worker_pool_subnets)

Description: The subnets to be used for the worker pool

Type: `list(string)`

## Optional Inputs

No optional inputs.

## Outputs

No outputs.

<!-- END_TF_DOCS -->
