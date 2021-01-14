# FOSDEM21 terraform-docs Demo

This is a demo project to show how to automatically generate documentations of
Terraform modules with [terraform-docs] using [terraform-docs/gh-actions].

<!--- BEGIN_TF_DOCS --->
## Prerequisites

- [Terraform](https://www.terraform.io) v0.12+
- [terraform-docs](https://github.com/terraform-docs/terraform-docs) v0.10+
- [terraform-docs/gh-actions](https://github.com/terraform-docs/gh-actions) v0.4+

## Requirements

| Name | Version |
|------|---------|
| aws | ~> 2.20.0 |
| consul | >= 2.4.0 |

## Providers

| Name | Version |
|------|---------|
| aws | ~> 2.20.0 |
| consul | >= 2.4.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| subnet\_ids | A list of subnet ids to use | `list(string)` | n/a | yes |
| vpc\_id | The id of the vpc | `string` | n/a | yes |
| extra\_environment | List of additional environment variables | <pre>list(object({<br>    name  = string<br>    value = string<br>  }))</pre> | `[]` | no |
| extra\_tags | Additional tags | `map(string)` | `{}` | no |
| instance\_count | Number of instances to create | `number` | `1` | no |
| instance\_name | Instance name prefix | `string` | `"test-"` | no |

## Outputs

| Name | Description |
|------|-------------|
| vpc\_id | The Id of the VPC |

<!--- END_TF_DOCS --->

[terraform-docs]: https://github.com/terraform-docs/terraform-docs
[terraform-docs/gh-actions]: https://github.com/terraform-docs/gh-actions
