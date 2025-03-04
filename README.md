# terraform-modules-template
template for terraform modules
# Terraform Module: <Module Name>

[![Terraform Version](https://img.shields.io/badge/terraform-%3E%3D<Minimum Terraform Version>-blue.svg)](https://www.terraform.io/downloads.html)
[![License](https://img.shields.io/badge/license-<License Name>-blue.svg)](LICENSE)
[![Tests](https://github.com/<your-org>/<your-repo>/actions/workflows/test.yml/badge.svg)](https://github.com/<your-org>/<your-repo>/actions/workflows/test.yml)

**Description:**

A concise and clear description of what the Terraform module does. Explain its purpose, functionality, and the resources it manages.

**Key Features:**

* List the main features and capabilities of the module.
* Highlight any unique or notable aspects.
* Focus on what makes this module useful.

**Usage:**

Provide a basic example of how to use the module.

```terraform
module "<module_name>" {
  source  = "[github.com/](https://github.com/)<your-org>/<your-repo>"
  version = "<module_version>"

  <input_variable_name> = "<input_variable_value>"
  # ... other input variables
}
```

**Changelog:**
* List any significant changes to the module over its history.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| vpc_id | ID of the VPC where resources will be created | `string` | n/a | yes |
| subnet_ids | List of subnet IDs for resource placement | `list(string)` | n/a | yes |
| instance_type | EC2 instance type to use | `string` | `"t3.micro"` | no |
| tags | Map of tags to apply to all resources | `map(string)` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| instance_id | ID of the created EC2 instance |
| security_group_id | ID of the security group attached to the instance |
| public_ip | Public IP address assigned to the instance |